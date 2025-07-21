# Feature Functions

There are various features in the ERC721J contract.  Here are the functions related to each feature.

### Mint Price Functions

* **mintPrice** - From [IERC721J.](../../interface-contracts/ierc721j.sol.md)
* **tokenMintPrice** - From [IERC721JFull.](../../interface-contracts/ierc721jfull.sol.md)
* _**setMintPrice**_ - Sets the mint price in ETH
* _**setTokenMintPrice**_ - Sets the mint price in an ERC20 token

### Song Supply Functions

* _**setMaxEditions**_ - Sets the max supply for a song
* **songSupply** - From [IERC721J.](../../interface-contracts/ierc721j.sol.md)
* **maxSongSupply** - From [IERC721J.](../../interface-contracts/ierc721j.sol.md)

### Staking Functions

* **publicMint** - From [IERC721JFull.](../../interface-contracts/ierc721jfull.sol.md)
* _**togglePublicMint**_ - Toggles public minting on a token id. Also known as staking.
* _**togglePublicMints**_ - Toggles public on more than one token id.  For staking multiple songs.

### Recycle Functions

* _**recycleEnabled**_ - Returns whether or not recycling is enabled for the collection
* _**toggleRecycleMint**_ - Toggles recycling mode on/off

### Split Contract Functions

* _**splits**_ - Returns the split address for the song id
* _**setSplit**_ - Sets the split address for the song id

### Rarity Multiplier Functions

* **rarityMultiplier** - From [IERC721JFull.](../../interface-contracts/ierc721jfull.sol.md)
* _**setRarityMultiplier**_ - Sets the % rarity multiplier for a rarity.  This lets you have different rarities be different mint prices relative to the normal price.

### Royalty Functions

* **royaltyInfo** - From [IERC2981.](../../interface-contracts/other.md#ierc2981.sol)
* _**royaltyBPS**_ - Returns the basis points for royalties to be used in royaltyInfo.
* _**setRoyalty**_ - Sets the royalty basis points.

