```typescript

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

  const fetchCharMedia = async (index: number) => {
    if (!user?.token) {
      console.log("No token available.");
      return;
    }

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
        return;
      }
      setDead(prevState => {
        const newState = [...prevState];
        newState[index].equipped_items = data.equipped_items;
        return newState;
      });
    } catch (e: any) {
      toast.error("Error getting equipment: " + e.message);
      console.log(e);
    }
    setPlayer(dead[index]);
  };

  const playerSelector = (index: number) => {
    fetchCharMedia(index).then(() => {
      fecthAttestation().then(() => {
        if (!player) return;
        player.Attestation = attestation;
        postDb(player);
      });
    });

    toast.success("Fetching player data for" + index);
  };
```