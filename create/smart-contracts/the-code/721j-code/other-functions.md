# Other Functions

The other functions that don't fit in a category but are still important are below:

## Write Functions

* _**setName**_ - Lets the owner set the name for the contract. Triggers the _**NameChange**_ event.
* _**setSymbol**_ - Lets the owner set the symbol for the contract. Triggers the _**SymbolChange**_ event.
* _**setVariables2**_ - Intended as the first function after initializing which sets the baseURI, contractURI and royaltyBPS all in one.  Meant to be used once at the beginning as a way to initialize the collection with a profile.  If you load into The Manager page right after minting a contract with The Contract Wizard, you will see a special button that is asking you to use this code.
* _**withdraw**_ - Withdraws the ETH that was sent to the contract.

## Read Functions

### From [IERC721J](../../interface-contracts/ierc721j.sol.md#read-functions)

* rarityOfToken
* songOfToken
* totalSongs

### From [IERC721JEnumerable](../../interface-contracts/ierc721jenumerable.sol.md)

* tokenOfPublicByIndex
* tokenOfSongByIndex
