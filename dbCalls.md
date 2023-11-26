```typescript

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
```