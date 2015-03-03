# Existing Problems

There are many problems with existing block chan based notary services:

## Block Chain Transaction Limitations

Existing block chain notary services require a new transaction to be created and placed in a block for each new document. It is estimated that the Bitcoin block chain can handle, at maximum, 3.5 transactions per second (citation needed). Since each notarized document must be included within a new transaction, this limit applies to all block chain notary applications. 

## Transaction Priority Limitations

In order for a block chain notary service to not lose coins, they generally write each transaction such that the output address exists in their wallet. The next transaction to include notary information uses this output as an input, and this pattern continues as long as the service exists. The priority of transactions becomes a limiting factor; a transaction with outputs having the same address as its inputs will have lower priority by default. With low priority, transactions may take longer than expected to be included in a block, causing a disruption in the timestamping service promised by the notary.

## Denial of Service Attacks

Whenever a new raw transaction is being created, previous unspent outputs must be found that can be used as inputs. These unspent outputs are selected based on an algorithm taking into account many factors, and each new output must be signed. Due to the complexity of this process, attempting to create many transactions at once can cause memory and CPU usage to significantly rise. Therefore, creating many transactions at once is both a scability problem for a notary with many customers, and also a potential denial of service attack vector.

## User Responsibility

Users must be responsible for keeping track of the txid that corresponds with each document they notarize. 

## Cost

The cost to notarize each document is equal to the minimum non-dust fee according to the codebase associated with the block chain that transaction is included in.

## Authentication

There is currently no existing distributed protocol enabling association of a digital signature with a document. Signatures can be hashed and stored in the block chain, but the original signature must be stored somewhere outside of the system itself. This leads to problems of centralization and persistence of data. Putting all authenticating information on the block chain is a more secure all-or-nothing approach.

## Reputation

It is not possible to build reuptation in existing distributed notary applications because of absent authentication information.

