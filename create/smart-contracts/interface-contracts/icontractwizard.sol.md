---
description: IContractWizard.sol
---

# IContractWizard.sol

The IContractWizard interface contract details 1 event and 9 functions. &#x20;

### New Event

The new event is called:

* _**NewContract**_ - Emits when a new contract is created

### Read Functions

The new read functions are:

* _**contractURI**_ - Returns the contract metadata
* _**contractByIndex**_ - Returns the contract address for a contract id
* _**inCollection**_ - Returns the contractId if an address can be found in the List of the Wizard
* _**mintPrice**_ - Returns the mint price in eth to create a contract
* _**name**_ - Returns the name of the contract
* _**tokenMintPrice**_ - Returns the mint price in an ERC20 token to create a contract
* _**totalSupply**_ - Returns the total amount of contracts that have been minted by this Contract Wizard

### Write Functions

The new write functions are:

* _**createClone**_ - Creates a new contract
* _**createCloneToken**_ - Creates a new contract and pays the wizard with an ERC20 token

This lets someone build their own contract wizard or even build something that talks to a whole bunch of contract wizards.  A super DAMN? :exploding\_head:

Read more [here.](https://github.com/jasondesante/721J-Token/blob/master/Wizard%20Contracts/Interfaces/IContractWizard.sol)
