# Metadata Functions

## Metadata Functions

These functions have to do with getting and setting metadata. For more information about metadata, see [what is a metadata file?](../../../the-metadata-maker/using-the-metadata-maker/metadata.md)

## Read Functions

### _baseURI_ - Base URI

The baseURI function gives you just the Base URI which is the beginning part of a metadata link.  The Base URI is used to save gas/space because the repeated part of the link is saved only once.

Base URI + Contract URI = Contract Metadata

Base URI + Token URI = Token Metadata

### contractURI - From [IERC721J](../../interface-contracts/ierc721j.sol.md#read-functions)

The contractURI function returns the contract metadata link.  This link is made with the Base URI and then the unique part of the link which creates the finished contract metadata link.

### songURI - From [IERC721J](../../interface-contracts/ierc721j.sol.md#read-functions)

The songURI function takes a songId and generation as input and returns the song metadata link.

### tokenURI - From [IERC721Metadata](../../interface-contracts/other.md#ierc721metadata.sol)

The tokenURI function takes a tokenID as an input and returns the token metadata link.  This link is made with the Base URI combined with the unique part of the link that creates the finished token metadata link.

## Write Functions

* _**setBaseURI**_ - Sets the baseURI
* _**setContractURI**_ - Sets the contractURI
* _**setSongURI**_ - Sets the songURI for one song
* _**setSongURIs**_ - Sets the songURIs for many rarities of one song.  The songID stays the same but it accepts an array of rarities.
* _**setManySongURIs**_ - Sets the songURIS for many rarities of many songs.  This takes an array of songIDs and an array of rarities.
