# Smart Contracts

The smart contracts that are used for The Contract Wizard are here.

{% embed url="https://github.com/jasondesante/721J-Token/" %}

You'll see a folder for the 721J contracts, a folder for the Contract Wizard contracts, and a folder for the metadata templates.

The 721J contract is made up of the main ERC721J.sol file and also includes five interface contracts.

The Contract Wizard contract is made up of the Contract Wizard contract and one interface contract.

## 721J Contracts

The 721J folder includes the code to deploy a single 721J contract.  This includes the contract solidity file and the interface solidity files.  The contract solidity file is where the code for the 721J contract is.   The interface contracts will let others build their own implementation of the 721J.

The contract file is called ERC721J.sol

The interface contracts are:

* **IERC721J.sol** - The main features of the 721J
* **IERC721JEnumerable.sol** - Indexes tokenOfPublicByIndex and tokenOfSongByIndex
* **IERC721JFull.sol** - The full set of features of the 721J
* **IERC721JPromo.sol** - Just the promo system of the 721J
* **IERC2981.sol** - For royalties. [Read more](https://eips.ethereum.org/EIPS/eip-2981)

## Wizard Contracts

The Wizard Contracts folder includes the code to deploy a full Contract Wizard.  This includes the Contract Wizard solidity file, the 721J clone solidity file, and the interface solidity files.  The Contract Wizard solidity file has the code for The Contract Wizard.  The 721J clone file is a slightly different version of the 721J contract with the ability to make clones of itself.  The interface files will let others build their own implementation of a Contract Wizard, or something that talks to many contract wizards.

The Contract Wizard's contract file is called ContractWizard.sol. &#x20;

The 721J clone's contract file is called ERC721JUpgradeable.sol

The interface contracts are:

* **IContractWizard.sol** - An interface contract just for the contract wizard. &#x20;
* **IERC721JUpgradeable.sol** - The main features of the 721J
* **IERC721JEnumerableUpgradeable.sol** - Indexes tokenOfPublicByIndex and tokenOfSongByIndex
* **IERC721JFullUpgradeable.sol** - The full set of features of the 721J
* **IERC721JPromoUpgradeable.sol** - Just the promo system of the 721J
* **IERC2981Upgradeable.sol** - For royalties. [Read more](https://eips.ethereum.org/EIPS/eip-2981)

The deployed Contract Wizard on mainnet is called [ApeTapesContractWizard](https://etherscan.io/address/0x1b9F04589183341Ad9b8Cd771983CEBeB0c1BC23).&#x20;
