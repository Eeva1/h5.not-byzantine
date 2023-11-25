# Nakamoto 2008: Bitcoin: A Peer-to-Peer Electronic Cash System

## Introduction

- Nakamoto is writing in the article that there should be an electric payment system based on cryptographic proof instead of trusted third party.
- There should be able to transact directly between two willing parties without the need for a trusted third party.

## Transactions

- Electronic coin is defined as a chain fo digital signatures
- Transferring the coin to next is happening by signing a hash of the previous transaction and the next owner's public key and adding them to the end of the coin.
- However, there is a problem with double-spendig the coin. A payee cannot verify, that one of the previous owners didn't double spend the coin.
- A common solution is to use mint, a trusted central authority to check every transaction for double spending, but it is exactly like a bank.
- To achieve this, transactions has to be publicly announced.
- There must be a system for participants so that they can agree on a single history of the order in which they got.

## Timestamp server

- The solution starts with a timestamp server.
- A timestamp server works by taking a hash of a set of items that need a timestamp. This hash is then shared widely, perhaps in a newspaper or a Usenet post.
- The timestamp essentially confirms that the data must have been present at that specific time, as it's required for the hash creation.
- Each timestamp contains the hash of the previous timestamp, creating a chain. With each new timestamp, the previous ones are further verified and strengthened.

## Proof of work

- is associated with scanning for a value, e.g SHA-256, the hash begins with a zero bits number.
- For timestamp network, the proof-of-work function has to be made by continuously increasing a nonce within the block until a value that results in the required number
of zero bits at the beginning of the block's hash is found.
- 

