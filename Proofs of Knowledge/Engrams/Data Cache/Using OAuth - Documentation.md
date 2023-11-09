[](/)

[API Access](/access/clients)

[Documentation](/documentation)

[Forums](https://us.forums.blizzard.com/en/blizzard/c/api-discussion)

[My Account](#)

[Log In](/nav/login?ref=https%3A%2F%2Fdevelop.battle.net%2Fdocumentation%2Fguides%2Fusing-oauth) [Account Settings](https://account.battle.net) [Create a Free Account](https://account.battle.net/creation/)

[API Access](/access/clients) [Documentation](/documentation) [Forums](https://us.forums.blizzard.com/en/blizzard/c/api-discussion)

[Log In](/nav/login?ref=https%3A%2F%2Fdevelop.battle.net%2Fdocumentation%2Fguides%2Fusing-oauth) [Account Settings](https://account.battle.net) [Create a Free Account](https://account.battle.net/creation/)

[Documentation](/documentation) Using OAuth Scroll to Top

[Battle.net Developer Portal](/) [Documentation](/documentation) Using OAuth

[Using APIs](/documentation/guides) [Getting Started](/documentation/guides/getting-started) [Using OAuth](/documentation/guides/using-oauth) [Client Credentials Flow](/documentation/guides/using-oauth/client-credentials-flow) [Authorization Code Flow](/documentation/guides/using-oauth/authorization-code-flow) [OpenID Connect](/documentation/guides/using-oauth/oidc-endpoints) [Example Applications](/documentation/guides/using-oauth/example-applications) [Game Data APIs](/documentation/guides/game-data-apis) [Community APIs](/documentation/guides/community-apis) [Regionality and APIs](/documentation/guides/regionality-and-apis) [Battle.net](/documentation/battle-net) [Diablo III](/documentation/diablo-3) [Hearthstone](/documentation/hearthstone) [Overwatch League](/documentation/owl) [StarCraft II](/documentation/starcraft-2) [World of Warcraft](/documentation/world-of-warcraft) [ World of Warcraft Classic](/documentation/world-of-warcraft-classic)

# Using OAuth

Battle.net uses OAuth 2.0 to secure the APIs that we provide. By using OAuth, developers allow Battle.net to handle authentication and receive a unique user ID, then use an access token for allowed resources like World of Warcraft characters, StarCraft II profile data, or other information as appropriate.

Due to the sensitive nature of storing user data, it is **HIGHLY RECOMMENDED** that developers use stable libraries for performing the OAuth process instead of implementing their own.

See the [Blizzard Developer API Terms of Use](https://www.blizzard.com/en-us/legal/a2989b50-5f16-43b1-abec-2ae17cc09dd6/blizzard-developer-api-terms-of-use) for details about how we handle third-party sites suspected of being compromised or when suspicious activity regarding a project is detected.

### Sample libraries

For many OAuth 2.0 libraries, developers only need the OAuth URIs below and their client ID and client secret from the API Access tool. Some platforms also make use of plugins that come preset with both the URLs and ability to get some user profile information. Currently, there are two sample libraries for Ruby and Node web apps:

- [Ruby Gem](https://rubygems.org/gems/omniauth-bnet) - [Github Repo](https://github.com/Blizzard/omniauth-bnet)
- [Node NPM Package](https://www.npmjs.org/package/passport-bnet) - [Github Repo](https://github.com/Blizzard/passport-bnet)

## Library quick start

When using a library, developers typically need four items to get started: their **client_id**, **client_secret**, **authorize_uri** , and **token_uri**.

### Client ID and secret

The first step in using OAuth is getting a **client_id** and **client_secret** via the API Access tool:

1. Log in to the Developer Portal.
2. Click **Create New Client**.
3. Enter a client name. The client name is used to identify the client in the list view. Client names may be visible to your site users and globally unique across all developer accounts.
4. Enter any redirect URIs needed (see below for details). **Note:** the Developer Portal does not validate redirect URIs entered by developers.
5. Enter the URL for the client application your are building and a description of your intended use for the APIs.
6. Click **Create**.

When using a library, developers should be able to plug in their client ID and client secret to begin working.

### Redirect URL

Developers registering an application can specify a redirect URI to use with their client ID. This must be a valid HTTPS (SSL-enabled) URL. After a user authorizes on Battle.net's login page they are redirected back to this URI.

Enter your redirect URL on the API Access page in the **Redirect URIs** field.

### OAuth URIs

OAuth requires two commonly-used URIs to work properly. The **authorize_uri** gets player authorization to allow applications to access certain information, such as a list of their Diablo III characters. The **token_uri** submits items, such as authorization codes, to request access tokens applications can use with Battle.net APIs.

  
|Region|Authorize URI|Token URI|
|---|---|---|
|US, EU, APAC|**https://oauth.battle.net/authorize**|**https://oauth.battle.net/token**|
|CN|**https://oauth.battlenet.com.cn/authorize**|**https://oauth.battlenet.com.cn/token**|

**{region}** is one of the following: **us**, **eu**, or **apac**. APAC is short for Asia-Pacific and replaces the previously-used **kr** and **tw** regions. There is also a **check_token** endpoint available to check the details of a token. It is available in all regions at **/oauth/check_token?token={token}**. Applications can use this endpoint to verify that an access token was actually generated for a given client.

## Scopes and OAuth enabled APIs

Scopes are used to request specific information from a site user. Applications do not require any additional scopes to use Battle.net login. Without scopes, applications can only gain access to a user's account ID and BattleTag. To get any more specific user information, an application needs to request permission from the user with scopes.

Currently, applications can request the following scopes:

  
|Scope|Description|Example API URL|
|---|---|---|
|**wow.profile**|Access to a user's World of Warcraft characters.|https://us.api.blizzard.com/profile/user/wow|
|**sc2.profile**|Access to a user's StarCraft II profile.|https://us.api.blizzard.com/sc2/profile/user|
|**d3.profile**|Access to a user's Diablo III profile.|https://us.api.blizzard.com/d3/profile/user|
|**openid**|Access details about a currently logged in user using OpenID Connect (OIDC).|https://oauth.battle.net/userinfo|

## Access tokens and OAuth flows

Battle.net APIs require access tokens granted by either the [OAuth client credentials flow](/documentation/guides/using-oauth/client-credentials-flow) or the [OAuth authorization code flow](/documentation/guides/using-oauth/authorization-code-flow).

### Access tokens

Access tokens last for 24 hours. A user changing their password, removing the authorization for an application's account, or getting their account locked for any reason, results in the expiration of their current access tokens. Developers should always check the response and request a new access token if the current one fails to work.

### What kind of access token do I need?

Most API requests require an access token obtained via the OAuth client credentials flow.

The following [OAuth endpoints](/documentation/battle-net/oauth-apis) require an access token retrieved via the OAuth authorization code flow:

- GET /oauth/userinfo
- GET /profile/user/wow
- GET /profile/user/wow/protected-character/{realm-id}-{character-id}
- GET /profile/user/wow/collections
- GET /profile/user/wow/collections/pets
- GET /profile/user/wow/collections/mounts

## Learning More

See the official [OAuth 2.0 RFC](https://tools.ietf.org/html/rfc6749) for more information.

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