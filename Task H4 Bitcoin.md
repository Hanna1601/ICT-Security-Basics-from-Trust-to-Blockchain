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
## A - Wallet

* I was not able to login to Virtual Box
>
## F - RogeCoin. 

*Critically comment on Honest Ads: If Cryptocurrency Was Honest*

Identify and list arguments made. Provide commentary to support and challenge each of the claims. 
1. Transfer cash "real money" to computer cash
2. Digital money cannot be changed to goods and services
3. Makes you look cool for small amount of internet trolls
4. Blockchain - if you don't know what it is you are a good candidate to camble your real money
5. Math problems and a lot of electircity
6. Fancy words to gain traction
7. Real money will come worthless
8. Governments will collabse
9. Pay exchange
10. Climate change - use of electricity
11. Wallet password forgot - loose all you money
12. Investent - why would you wanna use it. Money you shouldn't spend
13. Mining and CPU, 10 % is only left for mining
14. Amateurs loose money, because they don't know what they are doing.
15.If you can, provide references or real life examples to your claims. 

Source: https://www.youtube.com/watch?v=GUs5y9leCyA
