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
- For timestamp network, the proof-of-work function has to be made by continuously increasing a nonce within the block until a value that results in the required number of zero bits at the beginning of the block's hash is found.
- Proof-of-work, in essence, operates on a one-CPU-one-vote principle. The majority decision is represented by the longest chain, which reflects the highest amount of effort in proof-of-work.
- If the majority of CPU power is in the hands of honest nodes, the honest chain grows the quickest, surpassing any competing chains.

## Network

- These are the steps, that needs to run the network:

1) New transactions are broadcast for all nodes.
2) Every node collects new transactions into a block. 
3) Every node works on finding a difficult proof-of-work for its block.
4) When a node finds a proof-of-work, it broadcasts the block to all nodes.
5) If all transactions in the block are valid and not already spent, nodes accept it.
6) Nodes express their acceptance of the block by working on creating the next block in the
chain, using the hash of the accepted block as the previous hash.

- Nodes consider the longest chain is the correct one always, and will work on extending it
- New transactions sends does'nt need to reach all nodes

## Incentive

- By agreement, the first transaction that begins a new coin owned by the creator of the block is special
- The consistent introduction of a fixed amount of new coins is like gold miners putting in effort to bring more gold into circulation. Here it's the time spendin on CPU and electricity
- If the total value of a transaction is less than what was put into it, the extra amount becomes a transaction fee, added to the overall incentive of the block that includes the transaction.
- Once a set number of coins have been circulated, the incentive can shift entirely to transaction fees, making the system completely free from inflation.

## a Created a Wallet

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/d0c7bbc3-0ef3-480f-960b-c67fb203a995)

I copied my Bitcoin receiving address; 

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/07743929-d1bc-4a99-831a-a01e8cfc6337)

Googled the bitcoin tesnet faucet page, and tryed to send bitcoins.. but my address is not valid: 

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/a3a1aad9-2280-4107-a13e-b256b00e3ab1)

I don't understand why my address is not valid:

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/7b9942f3-5065-49d3-886b-d4f5a5065617)

