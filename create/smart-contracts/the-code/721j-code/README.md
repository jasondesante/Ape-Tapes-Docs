# 721J Code

The code for ERC721J.sol can be read [here.](https://github.com/jasondesante/721J-Token/blob/master/721J%20Contracts/ERC721J.sol)

{% embed url="https://github.com/jasondesante/721J-Token/blob/master/721J%20Contracts/ERC721J.sol" %}

## Events

There are 10 new events in ERC721J.sol and 3 events imported from interfaces, making 13 total:

* **Copy** - from [IERC721J](../../interface-contracts/ierc721j.sol.md#new-event)&#x20;
* **Recycle** - from [IERC721JFull](../../interface-contracts/ierc721jfull.sol.md#new-event)
* **SetPromo** - from [IERC721JPromo](../../interface-contracts/ierc721jpromo.sol.md#new-event)
* _**TokenPriceSet**_ - Emits when a price changes for an ERC20 token
* _**TogglePublic**_ - Emits when a tokenId is staked or unstaked
* _**NewSongURI**_ - Emits when a piece of song metadata is added or changed
* _**NewMax**_ - Emits when setMaxEditions is called to change the max supply of copies for a song.
* _**NewSplit**_ - Emits when a split address is set to a song
* _**NewMultiplier**_ - Emits when setRarityMultiplier is called and a generation's rarity multiplier is updated
* _**BaseURIChange**_ - Emits when setBaseURI is called and the baseURI is changed.
* _**ContractURIChange**_ - Emits when setContractURI is called and the contractURI is changed.
* _**NameChange**_ - Emits when setName is called and the contract name is changed
* _**SymbolChange**_ - Emits when setSymbol is called and the symbol is changed.
* **Transfer** - from [IERC721](../../interface-contracts/other.md#ierc721.sol)
* **Approval** - from [IERC721](../../interface-contracts/other.md#ierc721.sol)
* **ApprovalForAll** - from [IERC721](../../interface-contracts/other.md#ierc721.sol)

## Functions

There are lots of functions in ERC721J.sol. 72 public functions, and a bunch of private functions too!  I'll do my best to organize the public functions in an understandable order here. &#x20;

Functions are separated into categories because there are so many.  Every function that isn't from an interface is properly noted.

### Categories

#### [Metadata Functions](metadata-functions.md)

There are 4 read and 5 write functions related to metadata.  Read more [here.](metadata-functions.md)

#### [Minting Functions](minting-functions.md)

There are 10 write functions related to minting. Read more [here.](minting-functions.md)

#### [Feature Functions](feature-functions.md)

There are 7 features that have their 19 functions detailed [here.](feature-functions.md)

#### [Promo System Functions](promo-system-functions.md)

There are 4 read and 6 write functions related to the promo system. Read more [here.](promo-system-functions.md)

#### [Other Functions](other-functions.md)

The misfit unsorted functions that are still important. Read more [here.](other-functions.md)

## Imported Interface Contracts

All the imported interface contracts have their corresponding functions implemented into ERC721J.sol.  The new interface contracts are:

* IERC721J - See functions [here.](../../interface-contracts/ierc721j.sol.md)
* IERC721JEnumerable - See functions [here.](../../interface-contracts/ierc721jenumerable.sol.md)
* IERC721JFull - See functions [here.](../../interface-contracts/ierc721jfull.sol.md)
* IERC721JPromo - See functions [here.](../../interface-contracts/ierc721jpromo.sol.md)

The interface contracts from existing standards are:

* IERC2981 - See function [here.](../../interface-contracts/other.md#ierc2981.sol)
* IERC721 - See functions [here.](../../interface-contracts/other.md#ierc721.sol)&#x20;
* IERC721Metadata - See functions [here.](../../interface-contracts/other.md#ierc721metadata.sol)
* IERC721Enumerable - See functions [here.](../../interface-contracts/other.md#ierc721enumerable.sol)
* IERC165 - See function [here.](../../interface-contracts/other.md#ierc165.sol)
