```typescript
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
```