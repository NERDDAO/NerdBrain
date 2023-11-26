# Memento Mori
Fs onChain



![[mmoriflame.gif]]

Every research project starts with a question. For Memento Mori, I started with the following:

***"What is the best way to capture the uniqueness of Hardcore World of Warcraft characters onChain?"*** 

In order to answer that question I spent a lot of time learning  about what makes onChain records important, how perception and value interact with each other and what protocols can do to make this happen. We've used all we learned to create [Memento Mori](https://mmorionchain.com) an onChain memorial for the fallen.

![[logobadge.png]]

This is a technical post outlining the design decisions that lead to this build and where we want to take it from here. Lets dive right in the Whys and the Hows of this build.

## The Whys

## Why capture the uniqueness of Hardcore World of Warcraft Characters?

At NERD, we structure our projects as research. That means that we always have a reason to try out a build. In this case we were playing this new mode in World of Warcraft and wanted to test something out.

World of Warcraft,  for those who dont know (losers!) is the most popular MMORPG game in history. However recently they've releasead a new feature called  called [Hardcore](https://www.youtube.com/watch?v=w7oAjhccYJU). in a nutshell if your character dies its game over, there's no going back. As an incentive design enjoyoor this was very interesting for me to see and experience. At a first glance, not letting a user revive seems to be an awful feature, but it adds so much to the gameplay experience because it makes the world have more *weight* to it. 

The fact that any mistake can spell the demise of your character and therefore putting an end to an adventure in which the average player spends 100s of hours completely rearranges their priorities, which haves them pay more attention to the environment, plan ahead and coordinate. Without changing any game systems the game turns into  a much more immersive experience. [theres also bloopers](https://www.youtube.com/watch?v=d800hmQkl_c) and even a 100,000$ price pool tournament for dueling to the death. With all this attention, and a graveyard full of dead players it was easy to see that these are valuable stories that are waiting to broken out into the Metaverse.

![[Screenshot from 2023-11-03 18-49-58.png]]
Summary in one picture
## Why onChain?

One of the first things i learned doing this project is that the gaming community is really skeptic of anything to do with this technology. When talking about my initial ideas with people in the game I faced a mix of mild interest and downright vitrol against the idea of polluting games with "NFTs".  Although we know most of the critiques are more or less baseless, and that the main argument which was levied against the medium was the expense of mining, which is no longer a factor in the ETH network, these are still their views and repeating some technical jargon will not change the perception of this technology.

In order  to change this perception we set out to use the chain as a tool rather than the goal of the experience in order to showcase why its interesting and how powerful onChain experiences can be.

## F to pay Respects


![[Pasted image 20231122103358.png]]


This is the origin of the well known meme. The reason it became viral is because it achieved the opposite of the intended result. Most people thought it funny that the game would force you to press F to pay respects. There's no other way to progress. When delving into it, CoD a single player game was trying to get the player to feel emotions towards this character, but in doing so revealed the fruitlessness of paying respects on a vaccum. 

In WoW HC there's a notification sent out to the world whenever a player dies. And the entire world (of Warcraft) will press F and pay respects in their own way. This ephimeral interaction is lost to the void as the chat just keeps going. This is what we set out to capture in our build.

## The Hows

# How to capture the uniqueness of Hardcore World of Warcraft Characters onChain?

# Ethereum Attestation System: 
### I attest that I am

We're trying out a new lego block: attestations, using [EAS](attest.sh) as a protocol for defining the data structure that we will create onchain. The EAS allows for the creation of schemas which can serve as sources of truth for signed data and anchor points for backend routes to utilize in their design. 

We created two schemas for this project: The **Player** schema, and the Repects **schema**. The Player schema holds the information of the dead HC character and Respects track prayers and the sources of the respects paid. Together, we can see who the most respected player is and track attestations of respect as points for a number of things.

![[Pasted image 20231122110907.png]]

## Trustless verification

While implementing the attestation design we figured out an interesting thing. It acts as a form validation structure. We collect offchain attestations on our database which is not accessible outside of the established endpoints. Therefore if someone creates their own attestations outside of our front end our data structure will not be compromised. This allows for a several of interoperable use cases and the creation of a complex web of verifications before anything is put on chain. Effectively creating mini rollups of attestations that can represent a segment of activity.

# The Build

 We created an express application backend and started mapping out the routes required to authenticate a user into Bnet. We also established a mongoDB database that would hold the player data to be parsed and later put onChain. Once there, we received the player data and filtered out the dead characters. 

Once the data pipelines are established we set out to design how to represent this onChain. Initially we were going to create a merkle tree of all the players and submit it but we have now moved on to an attestation based design, from which we can still create this merkle tree eventually.

![[Pasted image 20231122095855.png]]

For the front end experience we iterated on our spatial design ideas explored with [AI-Universe](ai-universe.io) which led us to create a somber orb like experience. The app has two modes: If a player has dead characters they can submit them into the database through the player attestation. otherwise, a player can select a hero and attest to paying respects with a prayer.

The code for the build is available on [Github](https://github.com/Ataxia123)

## Future Work

With the established pipeline for attestations the goal is to create a NFT collection of the dead players with the number of respects paid as an extra feature which can dynamically grow over time.

The composable nature of attestations makes it hard to establish what will be built next, but our setup can serve as a stepping stone to create complex experience from the interaction of different attestation loops. 

If you'd like to build something using EAS, or anything really reach out to the NERDS!

-At0x.eth
![[minisquig.png]]









