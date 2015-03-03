# Proof of Publication

Proof of Publication defines a protocol for timestamping and proving ownership of digital information in a distributed network.


### Problems with existing notary services

There are many problems with the methods implemented by existing notary services. You can find them [here].

## Solution

The Proof of Publication approach abandons the unscalable, expensive 1:1 relationship between documents and transactions.


### Proof of Publication

Proof of Publication defines a protocol based on a merkle tree. The client process hashes documents and adds each hash as a leaf in a merkle tree. The program publishes the merkle tree root to the block chain, saving the original data of the merkle tree in a local file. 

The cost of notarizing one document is the same as the cost of notarizing N documents. These savings are transferred to the user, or paid towards miners for a higher priority transaction.


### Providers

Providers offer a Proof of Publication web service. Each Proof of Publication web service is known as a Provider. Providers should store original merkle tree data for users and handle the heavy-lifting, and ideally display a simple and easy to use interface. Providers fill a need in the market for "quick and easy" notary services, eliminating learning and setup times by acting as trusted service providers.

### Authentication

Authentication of documents via digital signature is possible within this protocol. Publishers store the merkle root of all hashed documents and a signature (proving authenticity) on the block chain. Publishers lump all unauthenticated data together in a single merkle tree to save time, space, and money.

### License

MIT

[here]:EXISTING_PROBLEMS.md
