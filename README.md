# Proof of Publication

Proof of Publication defines a protocol for timestamping and proving ownership of digital information in a distributed network.


### Problems with existing notary services

There exist problems with the methodology of current notary services. You can find them [here].

## Solution

The Proof of Publication approach abandons the unscalable, expensive 1:1 relationship between documents and transactions.


### Proof of Publication

Proof of Publication defines a protocol based on a merkle tree. Documents submitted to any Proof of Publication node are hashed, and that hash is added to a merkle tree. That markle tree root is published to the blockchain, and the original data of the merkle tree is saved on both the Proof of Publication provider's server and the user's computer. 

The cost of notarizing one document is the same as the cost of notarizing N documents. These savings can be transferred to the user, or paid towards miners for a higher priority transaction.


### Providers

Proof of Publication is provided as a web service to users. Each Proof of Publication web service is known as a Provider. Providers should store data for users and handle the heavy-lifting. It is not necessary for advanced users to rely on a Provider, as Proof of Publication can be built from source and run clientside. 

### Authentication

Authentication of documents via digital signature is possible within this protocol. Signatures are stored on the block chain alongside the merkle root of a document. Unauthenticated data can be lumped together in a merkle tree with all other unauthenticated data. 

### License

MIT

[here]:EXISTING_PROBLEMS.md
