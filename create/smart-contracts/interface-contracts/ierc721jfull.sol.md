---
description: IERC721JFull.sol and IERC721JFullUpgradeable.sol
---

# IERC721JFull.sol

The IERC721JFull interface contract details 1 event and 6 functions.  These functions add ERC20 support, recycle minting, staking, and rarity price multiplier.

### New Event

The new event is called:

* _**Recycle**_ - Event to show which tokens were created by recycling

### Read Functions

The new read functions are:

* _**publicMint**_ - Returns status of public mint for tokenId
* _**rarityMultiplier**_ - Returns the % price multiplier for a rarity
* _**tokenMintPrice**_ - Returns the mint price for an ERC20 token address

### Write Functions

The new write functions are:

* _**mintCopyToken**_ - Mint a copy with an ERC20 token. Triggers the _**Copy**_ event.
* _**mintCopyTokenTo**_ - Mint a copy with an ERC20 token to a wallet address of your choice. Triggers the _**Copy**_ event.
* _**recycleMint**_ - Recycle mint burns 2 tokens to mint 1. Triggers the _**Copy**_ and _**Recycle**_ events.

Read more [here.](https://github.com/jasondesante/721J-Token/blob/master/721J%20Contracts/Interfaces/IERC721JFull.sol)
