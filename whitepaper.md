# MorphToken
A non-fungible token to serve as a standalone collectable and also as a backbone for other non-fungible projects and assets.

## Goals
1. Make is easier for people to launch collectable games and other projects that rely on non-fungible assets.
2. Provide a fungible token to serve as "packs" of MorphTokens. Similar to how trading cards come in a pack which is undistinguishable from other packs, yet the cards within are all unique. (Morph Token Pack, MTP)
3. Provide a non-fungible token with several fields of varying types of data attached to each token. (morph token. notice )
4. Provide an algorithm that is acceptably random for generating new MorphTokens.

## Why

### Problems
Since the success of Cryptokitties, dozens of non-fungible token (NFT) projects have been launched. There will be hundreds more NFT projects launched in coming years, as we are just getting this party started.  Each launch has to work on
- A community of players/users must be created from scratch
- A (often complicated) secure and acceptably random algorithm for creating each individual NFT must be developed.
- Smart Contracts for proving ownership of the NFTs must be written.
- An Explorer, for users to view their tokens, must be developed.
- The security of all contracts must be tested.
- A lot of Gas must be spent to distribute the initial NFTs.

### Solutions
A Morphtoken is a generic and unique crypto asset which can be used to in any number of different collectible games.

For developers, they can use the MorphToken smart contracts as backends for their own NFT project. No need to develop random algorithms, write any contracts, pay for distribution of tokens, now worry about security.  A NFT project built on MorphToken could be built with just a few lines of javascript and [web3.js](github.com/web3/web3). Creators can decide what they want their collectable project to be, for example, a crypto flower collectable game.  Then use the data fields of each morph token to represent any attribute of their collectables, for example the color and shape of a flower.

For morph token holders, if a user owns a morph token, it can be used as an NFT in _every_ collectable project built on top of MorphToken. That means at launch, a new project will already have all of the users MorphToken does.

This adds some other interesting aspects to every project.  A morph token might represent a very rare item in one project but a very common one in another.  This might make people curious in seeing what

#### Examples
What if every professional athlete played in every sports league? If you owned the baseball card for pitcher Joe Schmoe you could also use it as the basketball card for point-guard Joe Schmoe.  

A single morph token could be used in a crypto baseball collectable game as David Ortiz, but in a crypto

## Specifics
The MorphToken project has a few parts. First, there are boxes which are fungible tokens, each of which can be converted in many packs. Second, there packs, which are fungible tokens which can be converted in morph tokens. Second, it has non-fungible tokens, which are the morph tokens.  Fourth, it has a front end website at [Morphtoken.net](http://morphtoken.net) where users are able to learn more about the project, see data on their owned morphtokens, and find a list of other projects being built on top of MorphToken.  The code for the website (as well as all of the contracts) can be found on the creator's [github](http://github.com/jschiarizzi) and is 100% open source. Should the website or github repository be deleted (it won't be), all of the tokens would be unaffected, as they live on Ethereum's blockchain.

### Boxes
Boxes are a fungible ERC-20 token. When this project is deployed there will be exactly *2000* boxes minted. No further boxes can be created, ever. Each box can be converted into *50* packs. Packs can not be converted back into Boxes.

Initial Box Distribution:
- 60% (1200): To be given away to the first 200 project which get build on top of MorphToken.
- 20% (400): To be sold to fund further development of this project.
- 10% (200): To be immediately converted into packs and given away at conventions, meetups, hackathons, parties, etc. with the goal of driving adoption.
- 9.75% (195): For Joseph Schiarizzi (creator) to save and give away at leisure. I made this after all, I should get to do what I want with at least some of it.
- 0.25% (5) For Abigail, Avi, Eric, Osebo, and Rowland, for helping inspire this project and support me through its development.

### Packs
The packs in this project behave similarly to packs of trading cards.  You don't know what is in them, they are all undistinguishable and can be easily transferred between people. We use the acronym *MTP* to represent our "Morph Token Pack" tokens.  The packs are ERC-20 compatible, so easy to store, transfer, and interact with. Each pack can be "opened" to be converted in *10* tokens.

The purpose of having packs (and boxes) is to make it easier to distribute morph tokens.  Instead of paying gas for 500 transactions to transfer 500 morph tokens, we can simply make 1 transaction by sending a box. Also, more wallets and services support ERC-20 tokens, so we can make use of a lot more potential integrations that could be fun.

### morph tokens
(notice lower case)
A non-fungible token that is the reason for this project. It can be used in multiple collectable games.

#### Data
Every morph token has several data fields attached to it, called "genes". The genes of a morph token determine how it is represented  Currently, those are:
- A 'C variable' (counter) which is the unique number for the order the assets were created in. The first morph token is 0; the last is 9,999,999.
- 3 'Boolean variables' represented as a 1 or 0.
- A 'DNA sequence' represented as an 18 digit long number.
- A 'P variable' (percent) represented as a number between 1 and 100.s

### Explorer
MorphToken will provide a way for users to check what tokens they own and the data associated with each token, on our website.

### Future Plans
- A javascript SDK so people can create their own blockchain collectable super fast with easy web requests.
- A big hackathon where we give away a bunch of boxes and packs to people that complete a project built on top of MorphToken.
- A marketplace for trading morph tokens.

No specific time line or "roadmap." I think those are kind of dumb. It will take as long as it takes, and we will be transparent with development.  If you have other ideas for things that should be built in order to support the MorphToken community, please let us know. We want to build those things too!

## Definitions of Terms Used Here
- Fungible: An asset which is interchangeable with other assets of the same kind. For example, a dollar.  It doesn't matter which dollar it is, you can use any dollar to buy things in a store.
- Non-fungible: An asset which is _not_ interchangeable. For example, a baseball card.  All the cards in a set are unique and have different attributes, even though they are all baseball cards.
- Smart Contract: A piece of code that lives on Ethereum's Blockchain.  It can not be modified or deleted. Ever. It will always exist exactly as originally designed, and anyone can interact with it. Interactions with the Smart Contract are guaranteed to be executed accurately, in the way the contract specifies.
- Acceptably Random: Having true randomness on a computer, especially on a blockchain, is extremely hard.  It is also very important that the method for getting randomness can not be influenced by any outsider.  Our algorithm is not perfectly random, but we think it is close enough for our purposes.  We chose security, and freedom from outside interference, in the tradeoff between slightly more random and more secure.
- Gas: The term for the small fee for doing work in Ethereum.  At the time of writing this that is about $0.04 USD for a transfer.
- ERC-20: A [standard](github.com/ethereum/EIPs/issues/20) for fungible tokens. Works very well with pretty much all Ethereum wallets and apps.
- Minted: Similar to how the US Mint creates dollar bills.  We will create 2000 boxes.

## Notes
- We chose Morphtoken.net because we want morph token to be a network.
