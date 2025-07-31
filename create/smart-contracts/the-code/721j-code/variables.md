---
description: Noteworthy 721J Variables
---

# Variables

These variables demonstrate advanced gas optimization techniques used in the 721J smart contract.

## Gas Optimization Strategy

Ethereum stores data in 256-bit chunks. Every on-chain storage operation costs gas, so efficient data packing is crucial for cost-effective contracts.

**Digit Packing**: Multiple values stored in a single uint256 by assigning specific digit ranges to different data types. This reduces storage slots and gas costs.

**Struct Packing**: Multiple smaller variables combined into a single 256-bit struct when their combined size equals exactly 256 bits.

## Core Variables

### \_songURIs

```solidity
mapping(uint256 => string) private _songURIs;
```

**Purpose**: Maps song metadata URIs using a packed key for efficient lookups.

**Key Packing** (input): The `uint256` key combines songId and generation:

* Digits 1-18: `songGeneration` (max value: (10^18) - 1)
* Digits 19+: `songId` (calculated as songId × 10^18)

**Usage**: To retrieve a URI, pack the songId and generation into a single uint256, then use it as the mapping key. The stored value is simply the metadata string.

### \_tokenIdInfo

```solidity
mapping(uint256 => tokenInfo) private _tokenIdInfo;
```

**Purpose**: Stores song and rarity data for each token.

**Structure**: Uses `tokenInfo` struct with two 128-bit values (song + generation = 256 bits total).

### Promo System Variables

### \_addressClaim

```solidity
mapping(address => uint256) private _addressClaim;
```

**Purpose**: Contract-wide promotion data per address.

**SongOut Packing**:

* Digits 1-18: `generationOut`
* Digits 19-36: `songIdOut` (×10^18)
* Digits 37+: `promoPercentOut` (×10^36)

### \_addressClaimSpecific

```solidity
mapping(address => mapping(uint256 => uint256)) private _addressClaimSpecific;
```

**Purpose**: Granular promotions requiring specific song/rarity combinations.

**SongIn Packing** (requirement):

* Digits 1-18: `generationIn`
* Digits 19+: `songIdIn` (×10^18)

**SongOut Packing** (reward): Same structure as `_addressClaim`
