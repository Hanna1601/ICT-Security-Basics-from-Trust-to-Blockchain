# H4 To the moon
> Homework for task H1, summary of article and test with electornic money

## X Read and summarize
> Nakamoto 2008: Bitcoin: A Peer-to-Peer Electornic Cash System
To have electornic cash without needing the thrid party financial institution between to verify. The solution is peer-to-peer network, that timestamps transactions by hashing them into an ongoing chain of hash-baseed proof-of-work. 

* Chapter 1 Intorduction:
  * In most cases the financial institutions are the trusted third party to process electronic payments when doing online purchase
    * Issues in this: challenges of trust-based transactions, no mechanism for direct digital payment, transactions are not truly non-reversible leading to increased meditation costs.
      
* Chapter 2 Transactions:
  * Electornic coin = chain of digital signatures, where each owner transfers the coin to next and always digitally signing a hash of the previous transaction and the public key of the next owner, these are then added to the end of the coin. What this does is that by verifying    the chain of ownership a payee can verify the signatures.
     * Issue here is that the payee can't verify that in the chain some of the owners didn't double spend the coin
     * To accomplish this without needing to have a trusted thrid party like a bank the transactions need to be publicly announced, systems for participants to agree on a single history of the order, the payee needs a proof that at the time of each transaction it was first received
       
* Chapter 3 Timestam Server:
  * Timestamp proves that the data have existed at the time, they include the previous timestamp in its hash, forming a chain, with each additionl timestam reinfocing the ones before it.
  * Prevents double-spending
    
* Chapter 4 Proof-of-Work:
  * Involves scanning for a value that when hashed, the hash begins with a number of zero bits.
    * When required number of zero bits increased the amount of work is also increasing
  * A nonce will we added in the block until a value is found that gives he block's hash the required zero bits
  * The longer the chain there is also more proof-of-work effort invested in it
    * The honest chain will grow fastest and outspace any competing chains
      
* Chapter 5 Network:
  * Nodes always consider the longest chain to be the correct one
  * There are 6 steps to run the network, new transactions are boradcast to all nodes, nodes collects new transactions into a block, node tries finding a difficult proof-of-work for its block, when proof-of-work has been found is the node broadcasts the block to all nodes, nodes accept the block only if all transactions in it are valid and not already spent, accpentance of the block is expressed by creating a the next block in the chain. 
 
* Chapter 6 Incentive:
  * There is no central authority to issue coins, the creator of the block starts a new coin that he owns and that is the first transaction in a block.
    * This adds incentive to nodes to support the network and provides a way to distribute coins into circulation
    * The incentive can also be funded with transactions fees
      
Sources: Nakamoto, Satoshi. Bitcoin: A Peer-to-Peer Electornic Cash System. 2008. https://bitcoin.org/bitcoin.pdf
## 
## A Wallet
