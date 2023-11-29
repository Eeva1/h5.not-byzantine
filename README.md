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

## a) I Created a Wallet

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/d0c7bbc3-0ef3-480f-960b-c67fb203a995)

- I copied my Bitcoin receiving address; 

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/07743929-d1bc-4a99-831a-a01e8cfc6337)

Googled the bitcoin tesnet faucet page, and tryed to send bitcoins.. but my address is not valid: 

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/a3a1aad9-2280-4107-a13e-b256b00e3ab1)

- I don't understand why my address is not valid:

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/7b9942f3-5065-49d3-886b-d4f5a5065617)

- The second time I was able to send me some coins..

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/5982966e-f074-4e6c-b31c-543dbb00fe0a)

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/9dab79ae-6d2e-4107-ba04-4bf356ac2850)

## But some how I could not send them back... apparently I have freezd out some addresses..

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/deb25d0f-4a3f-4919-acb4-5ca719850da3)

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/0aa4be4d-c402-41fc-911d-a64200ccd616)

## b) This morning I didn't care about the warnings of the unusual big fee, but just sent the Bitcoins back

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/6b203d93-273f-452b-9f8a-99aaded513d3)

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/a9179c0b-cc2d-4b65-9459-9c8f0ffdedcd)

- It seems that the transaction is pending

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/99811f0c-9079-41ef-921f-a7602c1d1018)


d) Explorer. Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. You only need to analyze the block information and one sample transaction, as a block can contain many transactions.

- I Googled "block explorer" and chose some Bitcoin explorer.one: https://blockexplorer.one/bitcoin-cash/mainnet/tx/000a04c00fd5681ab98c03da6b42dc6d65114b08a350eca77ffc1c1f7e61cabb

- I chose the latest block transaction in blocexplorer.one

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/bcb6889e-b43d-4424-9c4d-59904a8d5d75)

- There is a "Block reward" so does that mean, that somebody was mining and solved the mathematical problem and got rewarded for 1410,19 USD worth of bitcoins: 6.29762264 BCH

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/37d45ad9-0ebb-4536-8ac2-e6ec00b75a9e)

- Then I downloaded a transaction receipt, but there was nothing interesting.

 ![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/3a5d646f-19e6-48a7-baf8-81dc25adda34)
 
- Here are all the details of the blockchain:

![image](https://github.com/Eeva1/h5.not-byzantine/assets/149093822/cc1479bf-d037-4e39-b970-fe491042a6d0)

- There is only one input and output
- Size in bytes is 173
- 821550 included in block
- there is 10 confirmations
- There is not any inputs since it is a reward
- total output: 6.29762264 BCH
- There is not any fees, because it is reward
- Value when transacted	1,410.19 USD

- This is the transaction URL: https://blockexplorer.one/bitcoin-cash/mainnet/tx/4af676a8679ad8eb48ba6701ee7d89f88f934c744c37b2febcf267742b6aa138

Sources:

Partz, H. 2020. How do you use a block explorer? URL: https://cointelegraph.com/news/how-do-you-use-a-block-explorer. Accessed: 29.11.2023

Satoshi Nakamoto. Bitcoin: A Peer-to-Peer Electronic Cash System. URL:Protoni77https://bitcoin.org/bitcoin.pdf. Accessed: 28.11.2023

Tero Karvinen 2023. Trust to Blockchain. URL: https://terokarvinen.com/2023/trust-to-blockchain/. Accessed: 28.11.2023

Youtube 2019. How to Setup a Electrum Bitcoin Wallet on Testnet | Free Bitcoin Faucet | PIAI. URL:https://www.bing.com/videos/riverview/relatedvideo?q=how+to+receive+money+on+bitcoin+testnet+faucet&mid=51CA81CF74C00245ECD551CA81CF74C00245ECD5&FORM=VIRE. Accessed: 28.11.2023

BlockExplorer.one 2023. URL: https://blockexplorer.one/bitcoin-cash/mainnet/tx/4af676a8679ad8eb48ba6701ee7d89f88f934c744c37b2febcf267742b6aa138. Accessed: 29.11.2023
