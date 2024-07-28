---
description: IERC721J.sol and IERC721JUpgradeable.sol
---

# IERC721J.sol

The IERC721J interface contract details 1 event and 13 functions.

### New Event

The new event is called:

* _**Copy**_ - When a copy is minted, emits the tokenId that was used to make the copy. To count referral points.

### Read Functions

The 8 new read functions are:

* _**contractURI**_ - Returns the contract metadata.  Similar to tokenURI from [IERC721Metadata](other.md#ierc721metadata.sol) but for the collection. This should have been part of IERC721Metadata in my opinion.  It's essential.
* _**mintPrice**_ - Returns the price to mint a copy.  This is also something that should have been part of IERC721Metadata or IERC721 because of how essential it is.
* _**rarityOfToken**_ - Returns the generation / rarity of a tokenId.
* _**songOfToken**_ - Returns the songId for a tokenId.
* _**songSupply**_ - Returns the current supply of copies for a songId.
* _**maxSongSupply**_ - Returns the max supply of copies for a songId.
* _**songURI**_ - Returns the metadata for a songId and generation.  This is inspired by tokenURI from [IERC721Metadata](other.md#ierc721metadata.sol).
* _**totalSongs**_ - Returns the total amount of originals created.  This is inspired by totalSupply from [IERC721Enumerable](other.md#ierc721enumerable.sol).

### Write Functions

The 5 new write functions are:

* _**mintCopy**_ - Mints a copy. There are two mint copy functions because it saves gas to not enter an address if you are copying to your wallet.
* _**mintCopyTo**_ - Mints a copy to a wallet address of your choice. &#x20;
* _**mintOriginal**_ - Mints an original using 1 piece of metadata.  This is good if you want to be simple.
* _**mintOriginal3**_ - Mints an original using the default 3 pieces of metadata. There are two mint original functions because the spirit of the on chain rarities is to have different metadata for the original and the copies, so this is the actual suggested default mint original function.  The other cleaner mintOriginal function is provided because the default mintOriginal3 is a bit more gas, and there should always be a gas efficient option.
* _**ownerMintCopy**_ - The owner of the contract can mint copies for free and also mint custom rarity copies

Read more [here.](https://github.com/jasondesante/721J-Token/blob/master/721J%20Contracts/Interfaces/IERC721J.sol)
