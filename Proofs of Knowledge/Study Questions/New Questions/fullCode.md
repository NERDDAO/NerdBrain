```typescript
import { useEffect, useRef, useState } from "react";
import React from "react";
import Image from "next/image";
import { useEthersProvider, useEthersSigner } from "../utils/wagmi-utils";
import {
  EAS,
  Offchain,
  SchemaEncoder,
  SchemaRegistry,
  SignedOffchainAttestation,
} from "@ethereum-attestation-service/eas-sdk";
import type { NextPage } from "next";
import toast from "react-hot-toast";
import Slider from "react-slick";
import "slick-carousel/slick/slick-theme.css";
import "slick-carousel/slick/slick.css";
import { useAccount } from "wagmi";
import { RainbowKitCustomConnectButton } from "~~/components/scaffold-eth";

type Character = {
  id: number;
  name: string;
  level: number;
  owner: string;
  gender: string;
  class: string;
  race: string;
  faction: string;
  is_ghost: boolean;
  equipped_items: [unknown];
  Attestation?: string | undefined;
  media?: string;
};

const Home: NextPage = () => {
  const [user, setUser] = useState<any>(null);
  const [players, setPlayers] = useState<any[]>();
  const [dead, setDead] = useState<Character[]>([]);
  const [alive, setAlive] = useState<Character[]>([]);
  const [database, setDatabase] = useState<any[]>([]);
  const [player, setPlayer] = useState<Character | undefined>();
  const [mmToggle, setMmToggle] = useState<boolean>(true);
  const [infoToggle, setInfoToggle] = useState<boolean>(false);
  const [tutoggle, setTutoggle] = useState<boolean>(true);
  const [attestation, setOffchain] = useState<string | undefined>(undefined);

  // Renderer
  //
  //

  const provider = useEthersProvider();

  const signer = useEthersSigner();

  const EASContractAddress = "0xA1207F3BBa224E2c9c3c6D5aF63D0eb1582Ce587"; //

  // Initialize the sdk with the address of the EAS Schema contract address
  const eas = new EAS(EASContractAddress);

  // Gets a default provider (in production use something else like infura/alchemy)
  eas.connect(provider);

  // Initialize the sdk with the Provider
  const account = useAccount();

  const address = account?.address;

  // LOGIN METHODS
  let popup: Window | null = null;

  const login = () => {
    popup = window.open(
      "https://backend.nerddao.xyz/oauth/battlenet",
      "targetWindow",
      `toolbar=no,
       location=no,
       status=no,
       menubar=no,
       scrollbars=yes,
       resizable=yes,
       width=620,
       height=700`,
    );
    // Once the popup is closed
    window.addEventListener(
      "message",
      event => {
        if (event.origin !== "https://backend.nerddao.xyz") return;
        console.log("event", event);

        if (event.data) {
          setUser(event.data);
          popup?.close();
        }
      },
      false,
    );
  };

  const logout = async () => {
    try {
      const response = await fetch("https://backend.nerddao.xyz/oauth/logout", {
        method: "POST",
        credentials: "include",
      });

      if (response.ok) {
        setUser(null);
        toast.success("Logging out successful");
      } else {
        console.error("Failed to logout", response);
        toast.error("Failed to logout");
      }
    } catch (e) {
      console.log(e);
    }
  };

  const fetchDb = async () => {
    try {
      const response = await fetch("https://backend.nerddao.xyz/api/database"); // assume the same host
      const data = await response.json();
      console.log(data, "Player data from DB");
      setDatabase(data.players);
    } catch (e: any) {
      toast.error("error posting dead players to db");
      console.log(e.message);
    }
  };

  const postDb = async (players: Character) => {
    try {
      const response = await fetch("https://backend.nerddao.xyz/api/db", {
        method: "POST",
        credentials: "include",
        headers: {
          "Content-Type": "application/json",
        },

        body: JSON.stringify(players),
      });

      const data = await response.json();
      console.log(data, "POST Player data response");
    } catch (e: any) {
      toast.error("error posting dead players to db");
      console.log(e.message);
    }
  };

  const fecthAttestation = async () => {
    const offchain = await eas.getOffchain();

    //
    const uid = "0x633a741c3514c35e4fea835f5a1e4f4e6eb4b049e73c381080e7bd2923158571";

    // Initialize SchemaEncoder with the schema string
    const schemaEncoder = new SchemaEncoder(
      "address Owner,uint32 PlayerId,string Name,string Race,string Class,string Level,string[] EquippedItems",
    );

    if (!player) return console.log("No player available.");

    const encodedData = schemaEncoder.encodeData([
      { name: "Owner", value: address ? address : "0x0000000000000000", type: "address" },
      { name: "PlayerId", value: player.id, type: "uint32" },
      { name: "Name", value: player.name, type: "string" },
      { name: "Race", value: player.race, type: "string" },
      { name: "Class", value: player.class, type: "string" },
      { name: "Level", value: player.level, type: "string" },
      { name: "EquippedItems", value: player.equipped_items, type: "string[]" },
    ]);

    if (!signer) {
      console.log("No signer available.");
      return;
    }

    const offchainAttestation = await offchain.signOffchainAttestation(
      {
        version: 1,
        recipient: address ? address : "0x0000000000000000",
        expirationTime: BigInt(0),
        time: BigInt(123),
        revocable: true,
        refUID: "0x0000000000000000000000000000000000000000000000000000000000000000",
        // Be aware that if your schema is not revocable, this MUST be false
        schema: uid,
        data: encodedData,
      },
      signer,
    );

    const updatedData = JSON.stringify(
      offchainAttestation,
      (key, value) => (typeof value === "bigint" ? value.toString() : value), // return everything else unchanged
    );

    setOffchain(updatedData);
    console.log("New attestation UID:", attestation);
  };

  const fetchCharacter = async () => {
    try {
      const response = await fetch(
        `https://us.api.blizzard.com/profile/user/wow?namespace=profile-classic1x-us&access_token=${user.token}`,
      );
      const data = await response.json();
      const wowAccount = data.wow_accounts[0].characters;
      setPlayers(wowAccount);
    } catch (e) {
      toast.error("error getting characters");
      console.log(e);
    }
  };

  const fetchCharData = async (url: string) => {
    try {
      const response = await fetch(`${url}&access_token=${user.token}`);
      const data = await response.json();

      const index0 = alive?.findIndex(x => x.id === data.id);
      const index1 = dead?.findIndex(x => x.id === data.id);
      const index2 = database.findIndex(x => x.id === data._id);

      const profile: Character = {
        id: data.id,
        name: data.name,
        level: data.level,
        owner: address ? address : "no data",
        faction: data.faction.type,
        race: data.race.name.en_US,
        class: data.character_class.name.en_US,
        gender: data.gender.type,
        is_ghost: data.is_ghost,
        media: data.equipment.href,
        equipped_items: [{}],
      };
      console.log(data, index1, index2, "data");
      if (data.is_ghost == true && index1 == -1) {
        // maybe update database here
        setDead(prevState => [...prevState, profile]);

        return console.log(data.name, "dead", data.level);
      } else {
        if (index0 != -1 || data.level < 10) return console.log(data.name, "already in db", data.level);
        console.log(profile, "profile");
        setAlive(prevState => [...prevState, profile]);

        return console.log(data.name, "not dead", data.level);
      }
    } catch (e) {
      return console.log(e);
    }
  };

  const fetchCharMedia = async (index: number): Promise<void> => {
    if (!user?.token) {
      console.log("No token available.");
      return;
    }
    return new Promise(async (resolve, reject) => {
      try {
        // Ensure the dead array has elements and the index is valid
        if (dead.length === 0 || index < 0 || index >= dead.length) {
          console.log("Invalid index or empty dead array.");
          return;
        }

        const characterMedia = dead[index];

        if (!characterMedia?.media) {
          console.log(`No media URL found for character at index ${index}.`);
          return;
        }

        const url = `${characterMedia.media}&access_token=${user.token}`;
        const response = await fetch(url);
        const data = await response.json();

        const dindex = dead.findIndex(x => x.id === data.character.id);

        if (dindex === -1) {
          console.log("Character not found in dead array.");
          reject(); // reject the promise if not found
          return;
        }
        setDead(prevState => {
          const newState = [...prevState];
          newState[index].equipped_items = data.equipped_items;
          return newState;
        });
        resolve(); // resolve the promise after successfully updating state
      } catch (e: any) {
        toast.error("Error getting equipment: " + e.message);
        console.log(e);
        reject(e); // reject the promise in case of error
      }
    });
  }; /*
    const playerSelector = async (index: number) => {
      await fetchCharMedia(index);
      await fecthAttestation();
      if (!player) return;
      player.Attestation = attestation;
      await postDb(player);
  
      toast.success("Fetching player data for" + index);
    };
  */

  const fetchCharMediaAndAttestation = async (index: number): Promise<Character | null> => {
    try {
      // Finished state update before assigning player
      await fetchCharMedia(index);
      const player = dead[index];

      // Fetch Attestation
      await fecthAttestation();

      return player;
    } catch (e: any) {
      console.error(e);
      return null;
    }
  };

  const playerSelector = async (index: number) => {
    const playerData = await fetchCharMediaAndAttestation(index);

    if (!playerData) return;

    playerData.Attestation = attestation;

    // Update player state here
    setPlayer(playerData);

    // then post to the database
    await postDb(playerData);

    toast.success("Fetching player data for" + index);
  };

  useEffect(() => {
    fetchDb();
  }, []);

  useEffect(() => {
    fetchDb();
  }, []);

  useEffect(() => {
    if (user === null) return;
    fetchCharacter();
    console.log(players, "players");

    players?.map((character: any) => {
      if (character.level < 10)
        return console.log(character.character.name, "too low level", character.character.level);
      fetchCharData(character.character.href);
    });

    console.log("dead", dead, "alive", alive);
  }, [user]);

  const settings = {
    dots: true,
    infinite: false,
    speed: 500,
    slidesToShow: 1,
    slidesToScroll: 1,
  };
  // Once the popup is closed
  //
  const playerColor = (character: Character) => {
    if (character.class == "Druid") {
      return "text-orange-500";
    } else if (character.class == "Priest") {
      return "text-gray-500";
    } else if (character.class == "Warlock") {
      return "text-purple-500";
    } else if (character.class == "Warrior") {
      return "text-brown-500";
    } else if (character.class == "Paladin") {
      return "text-pink-500";
    } else if (character.class == "Rogue") {
      return "text-yellow-500";
    } else if (character.class == "Mage") {
      return "text-blue-50";
    } else if (character.class == "Shaman") {
      return "text-blue-500";
    } else {
      return "text-green-500";
    }
  };

  function MyComponent(props: any) {
    const { index } = props;
    const componentRef = useRef(null); // Reference to the component

    useEffect(() => {
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            // Component is visible, add event listener
            document.addEventListener("keydown", handleKeyPress);
          } else {
            // Component is not visible, remove event listener
            document.removeEventListener("keydown", handleKeyPress);
          }
        });
      });

      const handleKeyPress = (event: any) => {
        if (event.key === "F" || event.key === "f") {
          playerSelector(index);
        }
      };

      if (componentRef.current) {
        observer.observe(componentRef.current); // Start observing
      }

      return () => {
        if (componentRef.current) {
          observer.unobserve(componentRef.current); // Clean up
        }
        document.removeEventListener("keydown", handleKeyPress);
      };
    }, [index]);

    return <div ref={componentRef}>Press F to pay Respects</div>;
  }
  return (
    <>
      <div className="fixed w-full h-full">
        <Image
          src="/mmoriball3.png"
          fill
          alt="mmoriball"
          className="-mt-12 transform -translate-y-1/6 scale-75 scale-y-125 scale-x-90"
        />
        <div
          className="overflow-hidden rounded-full fixed h-1/2 w-1/4 top-2 left-1/2 transform scale-150 -translate-x-1/2 translate-y-1/3 z-10 shadow-xl shadow-black"
          style={{
            opacity: "1",
            scale: "1",
            backgroundImage: "url('/mmoriball.png')",
            backgroundSize: "cover",
            backgroundRepeat: "no-repeat",
            backgroundPosition: "center",
          }}
        >
          <Image
            src="/mmoriball2.png"
            fill
            alt="mmoriball"
            object-fit="cover"
            style={{
              animation: "pulse 1s infinite alternate",
              opacity: "0.65",
              position: "absolute",
              zIndex: 1,
              scale: "1.05",
            }}
          />
          {/* this is the text in the background */}
          <div className="mt-24 h-full relative flex overflow-hidden font-mono z-50">
            {database?.map((character: any, index: number) => (
              <>
                <div className="mt-0 -translate-y-1/2 animate-marquee whitespace-nowrap text-black h-full w-max ">
                  {" "}
                  <div
                    key={Math.floor(Math.random() * database.length)}
                    className="text-2xl  drop-shadow-lg shadow-inherit"
                  >
                    <span className={playerColor(character)}>
                      {" "}
                      {character?.name} <br />
                      <span className="text-black"> Level {character?.level} </span>
                      {character?.race} {character.class}
                    </span>
                  </div>
                </div>
                <div className="mt-4  animate-marquee whitespace-nowrap text-black h-full w-max ">
                  {" "}
                  <div key={Math.floor(Math.random() * database.length)} className="text-3xl">
                    <span className={playerColor(character)}>
                      {" "}
                      {character?.name} <br />
                      <span className="text-black"> Lvl {character?.level} </span>
                      {character?.race} {character.class}
                    </span>
                  </div>
                </div>
                <div className="mt-12 animate-marquee whitespace-nowrap text-black h-full w-max ">
                  {" "}
                  <div key={Math.floor(Math.random() * database.length)} className="text-3xl">
                    <span className={playerColor(character)}>
                      {" "}
                      {character?.name} <br />
                      <span className="text-black"> Lvl {character?.level} </span>
                      {character?.race} {character.class}
                    </span>

                    <br />
                  </div>
                </div>
                <div className="mt-16 -translate-y-1/2 animate-marquee whitespace-nowrap text-black h-full w-max ">
                  {" "}
                  <div key={Math.floor(Math.random() * database.length)} className="text-xl">
                    <span className={playerColor(character)}>
                      {" "}
                      {character?.name} <br />
                      <span className="text-black"> Lvl {character?.level} </span>
                      {character?.race} {character.class}
                    </span>
                    <br />
                  </div>
                </div>
                <div className="mt-24 animate-marquee whitespace-nowrap text-black h-full w-max ">
                  {" "}
                  <div key={Math.floor(Math.random() * database.length)} className="text-l">
                    <span className={playerColor(character)}>
                      {" "}
                      {character?.name} <br />
                      <span className="text-black"> Lvl {character?.level} </span>
                      {character?.race} {character.class}
                    </span>
                  </div>
                </div>
                <div className=" animate-marquee whitespace-nowrap text-black h-full w-max ">
                  {" "}
                  <div key={Math.floor(Math.random() * database.length)} className="text-l">
                    <span className={playerColor(character)}>
                      {" "}
                      {character?.name} <br />
                      <span className="text-black"> Lvl {character?.level} </span>
                      {character?.race} {character.class}
                    </span>
                  </div>
                </div>
              </>
            ))}
          </div>
        </div>
      </div>
      {mmToggle == true ? (
        <div className="flex flex-col items-center justify-center bg-transparent text-black pt-4 -mt-16">
          <div style={{ zIndex: 10 }} className="text-center max-w-xl bg-transparent overflow-hidden rounded-md p-8">
            {dead && dead.length > 0 ? (
              <Slider {...settings}>
                {dead.map((deadCharacter, index) => (
                  <div key={index} className="p-4">
                    {deadCharacter?.name == player?.name ? (
                      <>
                        <div className="border-2 border-gray-500 card mt-4 ml-10 mr-10 text-center text-white font-mono text-xl">
                          <br />
                          <span className="font-bold text-2xl">{player?.name}</span> <br />
                          <span className="font-bold">
                            Level {player?.level} <span>{player?.race}</span>
                            <span> {player?.class}</span>{" "}
                          </span>
                          <br />
                          ---------------------
                          <br />
                          <span className="text-lg text-left">
                            {player?.equipped_items?.map((item: any) => (
                              <div key={item.slot.type}>
                                {item.quality.type == "POOR" ? (
                                  <span className="text-gray-500"> {item.name.en_US}</span>
                                ) : (
                                  <>
                                    {item.quality.type == "COMMON" ? (
                                      <span className="text-white"> {item.name.en_US}</span>
                                    ) : (
                                      <>
                                        {item.quality.type == "UNCOMMON" ? (
                                          <span className="text-green-500"> {item.name.en_US}</span>
                                        ) : (
                                          <>
                                            {item.quality.type == "RARE" ? (
                                              <span className="text-blue-500"> {item.name.en_US}</span>
                                            ) : (
                                              <>
                                                {item.quality.type == "EPIC" ? (
                                                  <span className="text-purple-500"> {item.name.en_US}</span>
                                                ) : (
                                                  <span className="text-orange-500"> {item.name.en_US}</span>
                                                )}
                                              </>
                                            )}
                                          </>
                                        )}
                                      </>
                                    )}
                                  </>
                                )}
                              </div>
                            ))}
                          </span>
                        </div>
                        <br />
                      </>
                    ) : (
                      <div className="card mr-3 mt-4">
                        <div className="font-mono text-xl">
                          In Memoriam to: <br /> {deadCharacter.name}
                        </div>
                        <div>
                          <br />

                          <button
                            className="border-2 border-white text-center rounded-md p-2"
                            onClick={() => playerSelector(index)}
                          >
                            Memento Mori
                          </button>
                          <br />
                        </div>
                        <MyComponent index={index} />
                      </div>
                    )}
                  </div>
                ))}
              </Slider>
            ) : (
              <div className="card mt-60 pr-2 z-50 font-mono">
                {!address ? (
                  <RainbowKitCustomConnectButton />
                ) : (
                  <>
                    {!user ? (
                      <button
                        className="border-2 border-black rounded-md"
                        onClick={() => {
                          login();
                        }}
                      >
                        LOGIN WITH BNET
                      </button>
                    ) : (
                      <div>Logged in as {user.battletag}</div>
                    )}
                  </>
                )}
              </div>
            )}

            <br />
          </div>
        </div>
      ) : (
        <div></div>
      )}
      {/*login logo pulse portion and ? thing*/}
      <div className="card fixed right-20 top-2/3 mt-24 pr-2 z-50 font-mono">
        {!address ? (
          <RainbowKitCustomConnectButton />
        ) : (
          <>
            {!user ? (
              <button
                className="border-2 border-black rounded-md"
                onClick={() => {
                  login();
                }}
              >
                LOGIN WITH BNET
              </button>
            ) : (
              <div>Logged in as {user.battletag}</div>
            )}
          </>
        )}

        <div>Address: {address || "no data"}</div>
        <div>User: {user ? user.battletag : "no data"}</div>
        <button
          onClick={() => {
            logout();
            toast.success("Successfully logged out");
          }}
        >
          Logout
        </button>
      </div>

      <div
        className="fixed top-2/3 left-1/2 w-1/4 h-1/3 z-50 transform -translate-x-1/2 scale-105 hover:scale-110"
        onClick={() => {
          mmToggle ? setMmToggle(false) : setMmToggle(true);
        }}
      >
        <Image src="/logo.png" alt="Logo" fill />
      </div>

      {infoToggle == true ? (
        <div className="fixed z-50 border-gray-500 font-mono p-4 w-40 h-40 left-96 mr-60 top-96">
          <div
            className="animate-bounce absolute right-20 -left-6 h-80 w-60 scale-x-110 scale-y-110"
            onClick={() => setInfoToggle(!infoToggle)}
          >
            <Image fill className="fixed hover:scale-110" src="/question.png" alt="?" />
          </div>
        </div>
      ) : (
        <div className="fixed z-50 bg-black border-2  border-gray-500 font-mono p-4 w-1/2 right-60 mr-60 top-20">
          <span className="absolute right-5" onClick={() => setInfoToggle(!infoToggle)}>
            {"| X |"}{" "}
          </span>
          <span className="font-bold justify-center pl-96" onClick={() => setTutoggle(!tutoggle)}>
            💀 Memento Mori 💀
            <br />
            <br />
          </span>
          {tutoggle == true ? (
            <>
              Once upon a time, in a distant digital universe, countless adventurers thrived. They faced endless battles
              and overcame numerous dangers until they each met their inevitable end. <br /> <br />
              Just like in our reality, death is irreversible. However, the actions of these heroes leave lasting marks
              that resonate beyond their lifespan and reverberate throughout the Multiverse.
              <br />
              <br />
              <span className="font-bold">💀 Memento Mori 💀</span> is an onChain memorial to fallen hardcore
              adventurers which records their unique journey through their gear, their name, race and level at their
              time of death and stores it for use throughout the Metaverse. Stats, images, and other functionality are
              intentionally omitted for others to interpret. Feel free to use MementoMori in any way you want.
              <br />
              <br />
              Connect with us: <br />
              <span className="text-blue-500">
                {" "}
                <a href="https://discord.gg/yGuUY8ZsFr" target="_blank" rel="noreferrer">
                  Discord
                </a>
              </span>
              <br />
              <span className="text-blue-500">
                {" "}
                <a href="https://t.me/+N_-pUunbjHw3Y2Vh" target="_blank" rel="noreferrer">
                  Telegram
                </a>
              </span>
              <br />
              <span className="text-blue-500">
                {" "}
                <a href="https://twitter.com/MMoriOnChain" target="_blank" rel="noreferrer">
                  Twitter
                </a>
              </span>
              <br />
              <span className="text-blue-500">
                {" "}
                <a href="https://github.com/Ataxia123/MementoMori" target="_blank" rel="noreferrer">
                  Github
                </a>
              </span>
              <br />
              <br />
              Made with {"<3"} by At0x.eth and the NERDS
              <br />
            </>
          ) : (
            <div className="p-40 text-center">
              <span className="font-bold">
                This project is dedicated to the memory of my dog 🐶 Tuto.
                <br />
              </span>
            </div>
          )}
        </div>
      )}
    </>
  );
};

export default Home;

```