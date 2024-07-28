# Other

## IERC2981.sol

[Read more](https://eips.ethereum.org/EIPS/eip-2981)

IERC2981 details one function called royaltyInfo. &#x20;

You tell it the token id and how much the sale was, and it tells you what address you send the royalties to and how much the royalties amount to. &#x20;

```
    function royaltyInfo(
        uint256 _tokenId,
        uint256 _salePrice
    ) external view returns (
        address receiver,
        uint256 royaltyAmount
    );
```

The way I implement this is calculating the royaltyAmount with a variable called royaltyBPS which I can view with the function royaltyBPS() and setRoyalty().  This takes a number of basis points that will become the royaltyBPS value.  I calculate the receiver address by checking if there's a split address linked to the songId of the inputted tokenId.&#x20;



## IERC721.sol

IERC721 details 3 events and 9 functions.

The events are:

* Transfer
* Approval
* ApprovalForAll

The functions are:

* balanceOf
* ownerOf
* safeTransferFrom (with and without calldata)
* transferFrom
* approve
* setApprovalForAll
* getApproved
* isApprovedForAll

Read more [here.](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/IERC721.sol)

## IERC721Metadata.sol

IERC721Metadata details 3 functions.&#x20;

The functions are:

* name
* symbol
* tokenURI

Read more [here.](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/extensions/IERC721Metadata.sol)

## IERC721Enumerable.sol

IERC721Enumerable details 3 functions.

The functions are:

* totalSupply
* tokenOfOwnerByIndex
* tokenByIndex

Read more [here.](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/extensions/IERC721Enumerable.sol)

## IERC721Receiver.sol

IERC721Receiver details 1 function

That function is called:

* onERC721Received

Read more [here.](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/IERC721Receiver.sol)

## IERC165.sol

IERC165 details 1 function

That function is called:

* supportsInterface - Returns true if this contract implements the interface defined by `interfaceId`

Read more [here.](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/introspection/IERC165.sol)
