# Promotion System

Promo is short for promotion.  This feature lets you create token gated mints, free claims, discounts, rare mints, and anything else you can think of.

## Promos

In the Promos tab you can see all the active promotions for your contract.  You can see the requirements and reward for every promo and be able to sort through them.

## Set Promo

You can set a promotion with this button, which opens up a bunch of fields to enter. For a contract wide promotion, you need to enter in 4 things.  For a specific promo you need to enter in 6 things.  A regular contract wide promo is compatible with all ERC-721 tokens.  Specific promotions are only available to ERC-721J tokens because they require a Song ID and Rarity.

A contract wide promo needs:

* Contract Address - The address where the tokens you want to reward with the promo are from.  This contract address needs to be an ERC-721 standard contract.
* Price Multiplier Out - The cost to mint the promo, relative to the normal mint price. This should normally make the mint price discounted or free, but it's up to the artist.  Promos can require a specific token to unlock, and then be more expensive than a normal mint on top of it.  For layers of exclusivity. Defaults to 0%, for free.
* Song ID Out - The Song ID of the reward
* Song Rarity Out - The Rarity of the reward

A specific promo needs the additional:

* Song ID In - The Song ID required for a promo to be eligible.  If the Song ID is set to 0 that means any song is able to mint.
* Generation In - The Generation required for a promo to be eligible.  If the generation is set to 0 that means any rarity is able to mint.

## Promo Info

With this button you can look up any promo and see what it rewards.&#x20;

## Token Check

With this button you can look up any token on any contract and see if it's claimed it's promos.





