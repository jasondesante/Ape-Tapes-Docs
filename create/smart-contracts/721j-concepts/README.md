# 721J Concepts

## 721J Intro

We are entering a new era where verifying authenticity is more important than ever. The 721J token/contract is a modified ERC-721 with a focus on the needs of musicians and other artists in this new era. &#x20;

## Features

A quick list of the 721J features:

* 1/1 original master with any edition size of copies minted from the original
* Rarity affected by generation of copy
* Minting a copy requires the minter to own a copy, or for the token to be staked.
* Promo system. Supports ERC721 tokens, and 721J support letting you set promos with rarity and songId. Each promo has it's own price multiplier.
* Mint price can be set in ETH and any ERC-20 token.
* Support for splits, each song can send it's tokens to a specified address.
* Change max editions of a song, the name or symbol of the contract after deploying (will trigger an event marking it).
* Rarity price multiplier for specific rarities optional.
* Recycle to burn 2 songs to mint 1 optional.
* Support for IERC-2981, and on chain royalties.
* 4 interfaces to represent the essential functions in the 721J
* IERC721J for the main parts, IERC721JFull for the full essentials, IERC721JPromo for the promo system, IERC721JEnumerable for the indexes

## Why bother with this over a regular ERC-721 token?

You will find the 721J particularly useful if you want to:

* Make tokens of your art to build an artist wallet full of art
* The ability to make copies from the original.
* Want the token that the artist holds to be uniquely different from the copies.

Because of artist held originals.  The artist's wallet could be their digital discography which contains the original tokens of every song.  The wallet and contracts from the artist are an important thing in verifying whether or not you are looking at a genuine creation.

By introducing the idea of the 721J, the artist can create their 1/1 original and at any point they can mint copies from the original that have a different rarity on chain called "generation".  A copy is always the next generation of its parent.

