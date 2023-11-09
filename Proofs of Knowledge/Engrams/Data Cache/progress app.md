```typescript
import { useEffect, useState } from "react";
import type { AppProps } from "next/app";
import { RainbowKitProvider, darkTheme, lightTheme } from "@rainbow-me/rainbowkit";
import "@rainbow-me/rainbowkit/styles.css";
import "dotenv/config";
import NextNProgress from "nextjs-progressbar";
import { Toaster } from "react-hot-toast";
import { useDarkMode } from "usehooks-ts";
import { WagmiConfig } from "wagmi";
import { Footer } from "~~/components/Footer";
import { Header } from "~~/components/Header";
import OAuthClient from "~~/components/blizzard/OClient";
import { BlockieAvatar } from "~~/components/scaffold-eth";
import { useNativeCurrencyPrice } from "~~/hooks/scaffold-eth";
import scaffoldConfig from "~~/scaffold.config";
import { useGlobalState } from "~~/services/store/store";
import { wagmiConfig } from "~~/services/web3/wagmiConfig";
import { appChains } from "~~/services/web3/wagmiConnectors";
import "~~/styles/globals.css";

const ScaffoldEthApp = ({ Component, pageProps }: AppProps) => {
  interface OAuthOptions {
    config: {
      client: {
        id: string;
        secret: string;
      };
      auth: {
        tokenHost: string;
      };
    };
  }

  const price = useNativeCurrencyPrice();
  const setNativeCurrencyPrice = useGlobalState(state => state.setNativeCurrencyPrice);
  // This variable is required for initial client side rendering of correct theme for RainbowKit
  const [isDarkTheme, setIsDarkTheme] = useState(true);
  const { isDarkMode } = useDarkMode();
  const [oauthClient, setOauthClient] = useState<OAuthClient | null>(null);
  const [token, setToken] = useState<string | undefined>("");

  useEffect(() => {
    const oauthOptions = {
      config: {
        client: {
          id: scaffoldConfig.blizzardId,
          secret: scaffoldConfig.blizzardSecret,
        },
        auth: {
          tokenHost: scaffoldConfig.tokenHost || "https://us.battle.net",
        },
      },
    } as OAuthOptions;
    const client = new OAuthClient(oauthOptions);
    setOauthClient(client);
  }, []); // Empty dependency array ensures thi

  useEffect(() => {
    if (oauthClient) {
      const fetchToken = async () => {
        try {
          const fetchedToken = await oauthClient.getToken();
          setToken(fetchedToken);
        } catch (error: any) {
          console.error(`Failed to retrieve token: ${error.message}`);
        }
      }
      fetchToken();
      console.log(token, "token");
    }
  }, [oauthClient]);


  // Empty dependency array ensures this effect runs only once on component mount
  useEffect(() => {
    if (price > 0) {
      setNativeCurrencyPrice(price);
    }
  }, [setNativeCurrencyPrice, price]);

  useEffect(() => {
    setIsDarkTheme(isDarkMode);
  }, [isDarkMode]);
  console.log(oauthClient);
  console.log(scaffoldConfig.blizzardId);
  console.log(scaffoldConfig.blizzardSecret);
  return (
    <WagmiConfig config={wagmiConfig}>
      <NextNProgress />
      <RainbowKitProvider
        chains={appChains.chains}
        avatar={BlockieAvatar}
        theme={isDarkTheme ? darkTheme() : lightTheme()}
      >
        <div className="flex flex-col min-h-screen">
          <Header />
          <main className="relative flex flex-col flex-1">
            <Component {...pageProps} />
          </main>
          <Footer />
        </div>
        <Toaster />
      </RainbowKitProvider>
    </WagmiConfig>
  );
};

export default ScaffoldEthApp;

```