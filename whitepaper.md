# MorphToken
A non-fungible token to serve as a standalone collectable and also as a backbone for other non-fungible projects and assets.

## Goals
1. Make is easier for people to launch collectable games and other projects that rely on non-fungible assets.
2. Provide a fungible token to serve as "packs" of MorphTokens. Similar to how trading cards come in a pack which is undistinguishable from other packs, yet the cards within are all unique. (Morph Token Pack, MTP)
3. Provide a non-fungible token with several fields of varying types of data attached to each token. (morph token. notice )
4. Provide an algorithm that is acceptably random for generating new MorphTokens.

## Why (the problem)
Since the success of Cryptokitties, dozens of non-fungible token (NFT) projects have been launched. There will be hundreds more NFT projects launched in coming years, as we are just getting this party started.  Each launch has to work on
- A community of players/users must be created from scratch
- A (often complicated) secure and acceptably random algorithm for creating each individual NFT must be developed.
- Smart Contracts for proving ownership of the NFTs must be written.
- An Explorer, for users to view their tokens, must be developed.
- The security of all contracts must be tested.
- A lot of Gas must be spent to distribute the initial NFTs.

## Specifics
The MorphToken project has a few parts. First, is has a fungible token of packs. Second, it has non-fungible tokens, which are the morph tokens. Third, it has a front end website at [Morphtoken.net](http://morphtoken.net) where users are able to learn more about the project, see data on their owned morphtokens, and find a list of other projects being built on top of MorphToken.  The code for the website (as well as all of the contracts) can be found on the creator's [github](http://github.com/jschiarizzi) and is 100% open source. Should the website or github repository be deleted (it won't be), all of the tokens would be unaffected, as they live on Ethereum's blockchain.

### Packs
The packs in this project behave similarly to packs of trading cards.  You don't know what is in them, they are all undistinguishable and can be easily transferred between people. We use the acronym *MTP* to represent our "Morph Token Pack" tokens.  The packs are ERC-20 compatible, so easy to store, transfer, and interact wit

### morph tokens

## Definitions of Terms Used Here
- Fungible: An asset which is interchangeable with other assets of the same kind. For example, a dollar.  It doesn't matter which dollar it is, you can use any dollar to buy things in a store.
- Non-fungible: An asset which is _not_ interchangeable. For example, a baseball card.  All the cards in a set are unique and have different attributes, even though they are all baseball cards.
- Smart Contract: A piece of code that lives on Ethereum's Blockchain.  It can not be modified or deleted. Ever. It will always exist exactly as originally designed, and anyone can interact with it. Interactions with the Smart Contract are guaranteed to be executed accurately, in the way the contract specifies.
- Acceptably Random: Having true randomness on a computer, especially on a blockchain, is extremely hard.  It is also very important that the method for getting randomness can not be influenced by any outsider.  Our algorithm is not perfectly random, but we think it is close enough for our purposes.  We chose security, and freedom from outside interference, in the tradeoff between slightly more random and more secure.
- Gas: The term for the small fee for doing work in Ethereum.  At the time of writing this that is about $0.04 USD for a transfer.
- ERC-20: A [standard](github.com/ethereum/EIPs/issues/20) for fungible tokens. Works very well with pretty much all Ethereum wallets and apps.

## Notes
- We chose Morphtoken.net because we want morph token to be a network.
