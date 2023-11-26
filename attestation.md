```typescript

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


```