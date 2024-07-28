# Minting Copies

## Minting Copies

Anyone who holds a token can mint a copy of that token.  The copy will be the next generation of rarity from its parent.

The artist can mint copies one at a time to decide who gets them, or it can be staked and let anyone mint a copy.  The artist can distribute the "gen 2" copies to the collaborators of the song, normally, or as high priced investor tier tokens to fund the project.

The supply of each generation can be visualized like a tree.

{% embed url="https://awwevrdas7hu7x5byomcw3sy6dmocvuvz7xqitkvze72nbaucxoq.arweave.net/BaxKxGCXz0_focOYK25Y8NjhVpXP7wRNVck_poQUFd0" %}

As you can see from this detailed render of a simulation there is a higher chance that there would be more tokens of a rarity the farther down it goes in generations.  In other words, the "gen 2" will always be the most rare next to the 1/1.  And the "gen 4" tokens are the least rare in this visualization.&#x20;





## Code

Only the owner of the contract can interact with the functions to create a new original.

Only the owner of a token can interact with the functions to mint a copy.  If a token is staked, then anyone can mint from that token.

#### The functions to mint an original are called:

mintOriginal, mintOriginalSplit, mintOriginal3, mintOriginal3Split

MintOriginal lets you create an original with 1 piece of metadata for all rarities, mintOriginal3 lets you set 3 pieces of metadata when you create the original, for generations 1-3.  The "Split" variants let you add a split address when creating an original.

#### The functions to mint a copy are called:&#x20;

mintCopy, mintCopyTo, mintCopyToken, mintCopyTokenTo, recycleMint, ownerMintCopy

MintCopy mints a copy with ETH from the specified tokenId to the wallet that initiated the transaction. MintCopyToken lets you add an ERC-20 address which will be used instead of ETH as the mint fee.  Only works if a price has been set for that token.  Mints to the same wallet that paid the ERC-20 token.  MintCopyTo and mintCopyTokenTo both add a wallet address that you will be sending the token to.  This lets you mint directly to someone else's wallet.  Like sharing music to a friend!

RecycleMint lets you mint a copy by burning 2 other tokens from the same contract.  OwnerMintCopy lets the owner of the contract mint a copy without paying themselves the mint fee, also with the added extra ability to set the rarity of the copy.  This is because it allows the owner of the contract use rarities in more creative ways. For example, the artist could make a rarity 100 billion that is impossible to get any other way, and then attach special art to it's metadata making a unique variant of a song that is still traceable back to it's original 1/1.

## Minting It Forward

Pay it forward minting!  Don't mint for yourself, mint for the next person! &#x20;

It's like back in the day with physical media, where you could make a copy with a tape or cd, and then give your friend that copy.  The only music that got shared was the best stuff, so making a copy means you like the music and want to share it.

## St(e)aking

The rule "only the holder of a token can mint a copy" can be broken if the token is staked.  Once a token is staked, then anyone can mint a copy of it.

On Ape Tapes staking is a button on the Create Copies page.  There's 2 functions that can stake, called togglePublicMint and togglePublicMints.  Which let you stake 1 or many tokens at once.  See [Staking](staking.md).

## Recycling

If recycling has been turned on, anyone can mint a new token by burning 2 tokens from the contract. &#x20;

This reduces supply in the tokens that aren't as desirable as a new one might be.  It rebalances rarities a little bit, and lowers supply.  This could be good if there are too many tokens of something, they can be repurposed to bring balance to the collection, if that's desired.



Recycle mint is a special way to mint that burns 2 tokens to mint 1 new token.  It is turned off by default, but the owner of the contract can enable it with a quick toggle.  This can be used to help bring balance of supply and demand, and give a use for a potential oversupply of tokens.  There are other ways to be creative with recycle minting like if you distribute an oversupply on purpose in an interesting way with the intention of them being used for recycling in the future.





## Old Video

{% embed url="https://youtu.be/2XjG5eSNkCs" %}

{% embed url="https://youtu.be/duXeNedDHeE" %}
