# Contract Wizard Code

The code for ContractWizard.sol can be read [here.](https://github.com/jasondesante/721J-Token/blob/master/Wizard%20Contracts/ContractWizard.sol)

{% embed url="https://github.com/jasondesante/721J-Token/blob/master/Wizard%20Contracts/ContractWizard.sol" %}

## Events

There are 2 events in ContractWizard.sol and 1 event from IContractWizard, making 3 total:

* **NewContract** - from [IContractWizard](../interface-contracts/icontractwizard.sol.md)
* _**TokenPriceSet**_ - Emits when a price changes for an ERC20 token
* _**ContractURIChange**_ - Emits when the contractURI is changed with setContractURI

## Functions

There are 16 public functions in the ContractWizard.sol contract.  I will do my best to organize the public functions in an understandable order here. &#x20;

### Public Write Functions

* _**ownerCreateClone**_ - Lets the owner of the wizard create a clone for free. &#x20;
* _**ownerAddContract**_ - Lets the owner of the wizard add any contract to the library.  This is a powerful tool that needs to be wielded carefully. Should only be used to add 721J compatible contracts.
* _**setContractURI**_ - Sets the contractURI
* _**setMintPrice**_ - Sets the mint price in ETH
* _**setTokenMintPrice**_ - Sets the mint price for a particular ERC20 contract address
* _**withdraw**_ - Withdraws the ETH that was sent to the contract

### From IContractWizard

#### Write Functions [here](../interface-contracts/icontractwizard.sol.md#write-functions)

* createClone
* createCloneToken

#### Read Functions [here](../interface-contracts/icontractwizard.sol.md#read-functions)

* contractURI
* contractByIndex
* inCollection
* name
* mintPrice
* tokenMintPrice
* totalSupply

### From IERC165

* supportsInterface - [here](../interface-contracts/other.md#ierc165.sol)
