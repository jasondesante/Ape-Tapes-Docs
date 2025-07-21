# Metadata Functions

## Metadata Functions

These functions involve getting and setting metadata. For more information about metadata, see [what is a metadata file?](../../../the-metadata-maker/using-the-metadata-maker/metadata.md)

## Read Functions

### _baseURI_

The baseURI function gives you the beginning part of a metadata link.  The baseURI is used to save gas/space. The longer the baseURI is relative to the songURI, the more gas is saved. You want the paths to be short and the baseURI to contain the manifest tx\_id to save the most gas writing on chain.

baseURI + Contract Path = Contract Metadata

baseURI + Song Path = Token Metadata

### contractURI&#x20;

From [IERC721J](../../interface-contracts/ierc721j.sol.md#read-functions). The contractURI function returns the contract metadata link.  This URL is made with the baseURI and the contract metadata path which creates the finished link.

### songURI

From [IERC721J](../../interface-contracts/ierc721j.sol.md#read-functions). The songURI function takes a songId and generation as input and returns the song metadata link.

### tokenURI

From [IERC721Metadata](../../interface-contracts/other.md#ierc721metadata.sol). The tokenURI function takes a tokenID as an input and returns the token metadata link.  This link is made with the Base URI combined with the songURI. The songURI is the path for the metadata with the songID and rarityID of that tokenID.

## Write Functions

* _**setBaseURI**_ - Sets the baseURI
* _**setContractURI**_ - Sets the contractURI
* _**setSongURI**_ - Sets the songURI for one song
* _**setSongURIs**_ - Sets the songURIs for many rarities of one song.  The songID stays the same but it accepts an array of rarities.
* _**setManySongURIs**_ - Sets the songURIS for many rarities of many songs.  This takes an array of songIDs and an array of rarities.
