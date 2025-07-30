---
description: Noteworthy 721J Variables
---

# Variables

## Saving Space

Every number is stored as a 256 bit integer by default, unless noted.  Every number you save on chain costs gas. On Ethereum, data is written in 256 bit chunks. You can save gas by making variables smaller than 256 bits when they're written at the same time.  Another idea is to store more than one value in the same variable with **digit packing**.

## Noteworthy Variables

These variables are documented because of the ways they saved space by using digit packing techniques or structs.

### \_songURIs

* **\_songURIs** - takes a number, which is the songId and songGeneration packed into one, and returns the string for the URI. For the input number, the first 18 digits are for the generation, and after are for the song id.
* **songGeneration** - is stored at the beginning of the number, in the first 18 digits.  This means the largest generation number is 10 \*\* 18.
* **songId** - Is stored in digits 19+. Saved as songID \* (10 \*\* 18) in \_songURIs.

### \_tokenIdInfo

* **\_tokenIdInfo** - Remembers what song and rarity each token is. Stores the data of the song id and generation id for each token id. Uses the tokenInfo struct.
* **tokenInfo** - A struct made up of song and generation. Song and generation are both 128 bit, adding up to a 256 bit struct. Is used in...

#### Promo Variables

### \_addressClaim

* **\_addressClaim** - Takes an address and outputs a **digit packed** number (called SongOut).  If there is no promo set, the value for the address will be 0.
* SongOut - Saved as (promoPercentOut \* (10 \*\* 36)) + (songIdOut \* (10 \*\* 18)) + generationOut. Contains the song id, rarity of the promotion reward, and promo percentage which is the discount percent multiplier.&#x20;
* generation - Stored in digits 0-18.
* songID - Stored in digits 19-36. Saved as songIdOut \* (10 \*\* 18).
* promoPercentOut - Stored in digits 37+. Saved as promoPercentOut \* (10\*\*36) in SongOut

### \_addressClaimSpecific

Specific promotions can be set way more granularly than contract wide promotions.

* **\_addressClaimSpecific** - Takes an address and a number (SongIn) as input. Outputs a number (SongOut). Both numbers are **digit packed**.&#x20;
* SongIn - Saved as (songIdIn \* (10\*\*18)) + generationIn. Contains the song id and rarity of the required promo.&#x20;
* SongOut - Saved as (promoPercentOut \* (10 \*\* 36)) + (songIdOut \* (10 \*\* 18)) + generationOut. Contains the song id and rarity of the promotion reward, as well as promo percentage which is the discount percent multiplier.&#x20;
* generation - Stored in digits 0-18.
* songID - Stored in digits 19-36. Saved as songIdOut \* (10 \*\* 18).
* promoPercentOut - Stored in digits 37+ in SongOut. Saved as promoPercentOut \* (10\*\*36) in SongOut
