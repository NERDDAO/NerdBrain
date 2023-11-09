[](/)

[API Access](/access/clients)

[Documentation](/documentation)

[Forums](https://us.forums.blizzard.com/en/blizzard/c/api-discussion)

[My Account](#)

[Log In](/nav/login?ref=https%3A%2F%2Fdevelop.battle.net%2Fdocumentation%2Fguides%2Fusing-oauth%2Fclient-credentials-flow) [Account Settings](https://account.battle.net) [Create a Free Account](https://account.battle.net/creation/)

[API Access](/access/clients) [Documentation](/documentation) [Forums](https://us.forums.blizzard.com/en/blizzard/c/api-discussion)

[Log In](/nav/login?ref=https%3A%2F%2Fdevelop.battle.net%2Fdocumentation%2Fguides%2Fusing-oauth%2Fclient-credentials-flow) [Account Settings](https://account.battle.net) [Create a Free Account](https://account.battle.net/creation/)

[Documentation](/documentation) Client Credentials Flow Scroll to Top

[Battle.net Developer Portal](/) [Documentation](/documentation) Client Credentials Flow

[Using APIs](/documentation/guides) [Getting Started](/documentation/guides/getting-started) [Using OAuth](/documentation/guides/using-oauth) [Client Credentials Flow](/documentation/guides/using-oauth/client-credentials-flow) [Authorization Code Flow](/documentation/guides/using-oauth/authorization-code-flow) [OpenID Connect](/documentation/guides/using-oauth/oidc-endpoints) [Example Applications](/documentation/guides/using-oauth/example-applications) [Game Data APIs](/documentation/guides/game-data-apis) [Community APIs](/documentation/guides/community-apis) [Regionality and APIs](/documentation/guides/regionality-and-apis) [Battle.net](/documentation/battle-net) [Diablo III](/documentation/diablo-3) [Hearthstone](/documentation/hearthstone) [Overwatch League](/documentation/owl) [StarCraft II](/documentation/starcraft-2) [World of Warcraft](/documentation/world-of-warcraft) [ World of Warcraft Classic](/documentation/world-of-warcraft-classic)

# Client Credentials Flow

The OAuth client credentials flow is used to exchange a pair of client credentials (**client_id** and **client_secret**) for an access token.

See the [OAuth RFC](https://tools.ietf.org/html/rfc6749#section-1.3.4) for detailed information about the client credentials flow.

The client credentials flow is used for most API requests, with the exception of those listed on the [OAuth authorization code flow](/documentation/guides/using-oauth/authorization-code-flow) page.

## Retrieving an access token

To request access tokens, an application must make a POST request with the following multipart form data to the token URI: **grant_type=client_credentials**

The application must pass basic HTTP auth credentials using the **client_id** as the user and **client_secret** as the password.

#### Example CURL request

```bash
curl -u {client_id}:{client_secret} -d grant_type=client_credentials https://oauth.battle.net/token
```

Copy

#### Expected response

```json
{"access_token": "USVb1nGO9kwQlhNRRnI4iWVy2UV5j7M6h7", "token_type": "bearer", "expires_in": 86399, "scope": "example.scope"}
```

Copy

## Using an access token

After an application retrieves an access token, it provides that token when making requests to API resources. This is done via an authorization header:

#### Example CURL reqest

```bash
curl --header "Authorization: Bearer <access_token>" <REST API URL>
```

Copy

#### Example use

**Authorization: Bearer {token}**

---

[Careers](https://careers.blizzard.com/)

[About](https://www.blizzard.com/company/about/)

[Support](https://support.blizzard.com/)

[Contact Us](http://us.blizzard.com/company/about/contact.html)

[Press](https://blizzard.gamespress.com/)

[API](https://develop.battle.net/)

©2023 Blizzard Entertainment, Inc. All rights reserved.

All [trademarks](https://www.blizzard.com/legal/b04001c4-dc81-480d-a475-5e276e241e4f/) referenced herein are the properties of their respective owners.

CA Residents only: [Do not sell my personal information](https://www.blizzard.com/legal/a97631bf-2b21-4755-a740-5934bd5cb632/)

[Privacy](https://www.blizzard.com/en-us/legal/a4380ee5-5c8d-4e3b-83b7-ea26d01a9918/)

[Terms](https://www.blizzard.com/legal/)

[Cookies](/cookies)