# Existing Problems

There are many problems with existing block chain based notary services:

## Block Chain Transaction Limitations

Existing block chain notary services hide data inside a new transaction for each new document. Evaluations of the Bitcoin block chain indicate Bitcoin can handle a maximum of 3.5 transactions per second (citation needed). This acts as a hard limit on scalability, and introduces wasted competition in the ecosystem between financial and non-financial transactions.

## Transaction Priority Limitations

In order for a block chain notary service to not lose coins, they generally write each transaction such that the output address exists in their wallet. The next transaction to include notary information uses this output as an input, and this pattern continues as long as the service exists. Transaction priority becomes a limiting factor; a transaction with outputs having the same address as its inputs will have lower priority by default. With low priority, transactions may take longer than expected to become part of a mined block, causing a disruption in the timestamping service promised by the notary.

## Denial of Service Attacks

When creating a new transaction, bitcoind finds unspent outputs and uses them as inputs. It selects this outputs based on an algorithm taking into account many factors, and signs each new output. Attempting to create many transactions at once can cause system instability. Therefore, creating many transactions at once is both a scalability problem for a notary with many customers, as well as a potential denial of service attack vector.

## Duplication

Current notary services do not help distinguish between an authentic original and a copy with a single bit flipped. 

## User Responsibility

Users are responsible for keeping track of the txid that corresponds with each document they notarize. 

## Cost

The cost to notarize each document is equal to the minimum non-dust fee according to the codebase associated with the block chain containing that transaction.

## Authentication

There is no existing distributed protocol enabling association of a digital signature with a document. The block chain can store hashed signatures, but the original signature cannot be stored within the system itself. This leads to problems of centralization and persistence of data. Putting all authenticating information on the block chain is a more secure all-or-nothing approach.

## Reputation

It is not possible to build reputation in existing distributed notary applications because of absent authentication information.

