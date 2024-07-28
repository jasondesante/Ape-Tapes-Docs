# Promos

## What Are Promos?

The promo system is very capable and robust. You can do whitelists, free claims, discounts and ultra rare copies with the promo system. There are 2 different types of promos.  One is contract wide, and works for all 721 tokens. The second type works just for 721J tokens and allows more specific promos to be set.

Promos are:

* Any token gated mint
* Whitelists, free claims, discounts, and expensive rare variants
* Can use any token from a contract, or any song or rarity of a 721J to be a given a promo
* Gives more freedom in how something gets distributed by token gating the audience, and by giving the option to reward holders of tokens.

Promos (short for promotions) are special token gated mints you can set to limit minting or reward holders.  This can be used for whitelists, free claims, or discounted mints

Any token from an ERC-721 collection can be eligible for a promo.  The artist can set a promo to require any NFT in the collection, a specific song, rarity, or song and rarity if it's a 721J token. &#x20;

Promos can reward a free claim, so it's 0 friction to explore new directions. Using promos for whitelists results in an old fashioned token gated mint.  Using a discounted or inflated price for minting is an option too.



## Promo Code

The promo system includes its own mappings to keep track of all the active promos, and which tokens have used up their claim.  The mappings can be read with the functions promoCheck and promoCheckSpecific, to see what the reward is for a promo.  The functions tokenClaimCheck and tokenClaimCheckSpecific will return yes or no to if a token has used up its claim.

The functions setPromo and setPromoSpecific are used to set the 2 different types of promos. &#x20;

The functions promoMint, promoMintSpecific, promoMintSong, and promoMintRarity are used to mint promos.  PromoMint deals with normal contract wide promos.  Specific has to do with a promo that requires both a specific song and rarity. PromoMintRarity is for minting promos that require any song of a certain rarity.  PromoMintSong is for minting promos that require any rarity of a specific song.





{% embed url="https://7hhxakj2amkxdwmljzdjwchwtg3rendytupyqqqq4yzmsamgaaqq.arweave.net/-c9wKToDFXHZi05Gmwj2mbcSNHidH4hCEOYyyQGGACE" %}
An example of a promo on the promo page
{% endembed %}

## Examples of promos:

An example of a specific song free claim is to reward holders of any rarity of song 1 with a normal edition of song 2. &#x20;

An example of a normal discount promo is to reward any holder of a MAYC with a 69% discount of a particular song.

An example of a specific free claim is to reward holders of generation 3 of song 2 on your buddy's contract with generation 3 of song 5 on your contract.

An example of a whitelist promo is to allow all holders of a BAYC whitelist to mint a rarity 69 token of the most recent song.







## Old Video

{% embed url="https://youtu.be/jvy83ZYXLbg" %}

{% embed url="https://youtu.be/u-BQA4j212k" %}

