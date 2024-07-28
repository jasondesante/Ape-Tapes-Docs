# Database

## Current Database Framework

Moralis - Blockchain indexing

IPFS - Token metadata and files of outside tokens

Arweave - Token metadata and files of tokens, and hosting of front end.

Railway - Back end server hosting

MongoDB - DB server hosting

Redis - Caching server hosting

## Future Database Considerations

Upgrading to work with parse live query server?

Moving to a paid MongoDB or Firebase DB?

Cloud Firestore vs Live Query?

Weave DB?

The Graph?

Getting The Graph working with the DB?

AO?

AO?

AO?

Or AO?

## The Graph Integration

We need The Graph support but it is irrelevant until they support getting tokenURIs hosted on Arweave.  Currently The Graph only supports grabbing metadata from the tokenURI function if the file is hosted on IPFS.&#x20;

### Subgraph Explanation

A subgraph will index all the contracts made by the Contract Wizard all at once so it becomes an added feature of being a part of the Wizard's Library.  A deployed subgraph for the Contract Wizard would mean that everything is automatically indexed without the need of a centralized indexing solution, and makes it easier for artists to build because the indexing part could be all figured out automatically for everyone if this is setup.

### WeaveDB Integration

WeaveDB will let the subgraph be stored as a traditional no-sql database on Arweave which makes things even better.

### AO Integration

I think AO might be the way to get a decentralized server working with Arweave.
