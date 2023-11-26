```html
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

```