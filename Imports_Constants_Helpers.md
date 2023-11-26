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
};

export default Home;

```