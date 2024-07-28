---
description: IERC721JPromo.sol and IERC721JPromoUpgradeable.sol
---

# IERC721JPromo.sol

The _**IERC721JPromo**_ interface contract details 1 event and 8 functions. This adds setting promotions, minting promotions, and the necessary read functions to display promos on the front end.

### New Event

The new event is called:

* _**SetPromo**_ - Emits when a promo is set

### Read Functions

The new read functions are:

* _**promoCheck**_ - Takes a contract address and returns (if one exists) the promo claim set for that contract
* _**promoCheckSpecific**_ - Takes a contract address, song and generation and returns (if one exists) the promo claim set for that specific set of tokens on that contract
* _**tokenClaimCheck**_ - Returns if a token from an address has claimed it's promo token for the contract wide reward
* _**tokenClaimCheckSpecific**_ - Returns if a token from an address has claimed it's promo token for the specific reward

### Write Functions

The new write functions are:

* _**promoMint**_ - Mints a promo token using the contract wide setting
* _**promoMintSpecific**_ - Mints a promo token using the setting that needs matching songId and generation to be accepted
* _**setPromo**_ - Sets a promo claim for a contract wide reward. Any token from an ERC721 contract gets a reward.
* _**setPromoSpecific**_ - Sets a promo claim for a ERC721J specific reward. Any token from an ERC721J contract can get a reward based on it's song, rarity, or both.

Read more [here.](https://github.com/jasondesante/721J-Token/blob/master/721J%20Contracts/Interfaces/IERC721JPromo.sol)
