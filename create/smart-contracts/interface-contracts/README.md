# Interface Contracts

## What Is An Interface Contract?

The interface contracts are used to define the functions that a contract must implement without providing the implementation of those functions.  They are similar to abstract contracts but cannot contain any implemented functions or state variables.  Interface contracts are particularly useful for defining the expected behaviours of other contracts that will interact with the implementing contract.

The interface contracts make it possible for anyone to build their own version of something while making sure the different implementations can talk to each other.

## 5 New Interfaces

There are 4 interface contracts that cover the 721J functions. There's 1 interface contract that covers the functions in The Contract Wizard. They are called:

* IERC721J / IERC721JUpgradeable [here](ierc721j.sol.md)
* IERC721JEnumerable / IERC721JEnumerableUpgradeable [here](ierc721jenumerable.sol.md)
* IERC721JFull / IERC721JFullUpgradeable [here](ierc721jfull.sol.md)
* IERC721JPromo / IERC721JPromoUpgradeable [here](ierc721jpromo.sol.md)
* IContractWizard [here](icontractwizard.sol.md)

The I stands for Interface. &#x20;

The 721J interfaces are named that way because the normal 721J ones are for the normal contract and the Upgradeable ones are for the 721J clones to be used with The Contract Wizard.

## Extra Interface Contracts

IERC2981 is for royalties. [here](other.md#ierc2981.sol)

IERC721, IERC721Metadata, IERC721Enumerable, and IERC721Receiver are to cover the functionality of a normal ERC721 contract. [here](other.md)

