# H4 To the moon
> Homework for task H4, summary of article and test with electornic money

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

## A - Wallet

Create a BitCoin testnet wallet. (For example, electrum)
* Run the Update sudo apt-get update and then installed the electrum sudo apt-get install electrum.
 * The installion worked with no errors
* Created the wallet with standard 
  
![image](https://github.com/user-attachments/assets/154bcb6d-6369-4769-9c40-009112bbb01f)

![image](https://github.com/user-attachments/assets/09952791-8552-4c3b-8a8f-034935d8fed2)

  * Chose not to encrypt the wallet to hopefully maket it easier. 

![image](https://github.com/user-attachments/assets/15ee998a-6b83-4ccc-a3d9-aedb7834151e)

* Got the wallet open but it says in the bottom not connected

![image](https://github.com/user-attachments/assets/b4a57167-e2cb-47ff-a623-9f14fb6c86c5)

## B Faucet 

Get worthless fake money from a testnet Bitcoin faucet.
* I used this: https://bitcoinfaucet.uo1.net/send.php
  * The one in the document didn't work
  * Really not sure if it work correctly or not but didn't give an error but really don't see the coins anywhere
  * Did it again with same result
        
![image](https://github.com/user-attachments/assets/6219eff6-f3c4-43c1-b5e8-851dd81f1aed)

* As I saw that the elctrum testnet was not connected I tried running it again from terminal wtih electrum --testnet
  * I started the process again, gave a new name added number 2 but then thought I would get the same seed (?) as it suggested it and tadaa I was online my balance was 0,02!
  * Really can't say that I know what I was doing
 
 ![image](https://github.com/user-attachments/assets/fb3a2546-bc03-455a-b5c6-77b114efe609)


## C Giveway and D Recyle

Move money to another Bitcoin wallet. Choose an amount where the last two digists are 73.

* Don't have another wallet of my own so send it to back
  * Got error that not enough funds (the fees)

![image](https://github.com/user-attachments/assets/5953fe50-d1a7-40c7-b220-8166b807d1a8)

* I got stuck in here, couldn't send out any money out or the next step return it to the faucet as the above error.

![image](https://github.com/user-attachments/assets/24657fba-d871-4f33-80c8-c2c6c078bb24)

  
## D Recycle 

Move the testnet money back to the same faucet you got it from

## E Explorer 
Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. You only need to analyze the block information and one sample transaction, as a block can contain many transactions. 
* I chose a block 870903 from https://blockstream.info/ and opened in blockexplorer.one

The site gives you information about the block size, the total transactions which at the time were 6 179. 
The difficulty I think means at some scale how difficult it is to mine the block. Rewards tell you what the miner gets. 

![image](https://github.com/user-attachments/assets/c16ac9da-5225-4654-bd74-e459771704b7)

* I looked in to one transaction the block

It shows from where and to whom the coins were transferred. What the fee was for this transaction and what the transferred amount was in bitcons vs usd. 
And of course the date and time of the transaction. There is also the number of transactions which is 170, that refers to number of blocks that have been added to the blockchain, each added block increases the security of the transaction. 

![image](https://github.com/user-attachments/assets/040321fc-2da2-4220-8f82-94e7974d1892)


## F - RogeCoin. 

*Critically comment on Honest Ads: If Cryptocurrency Was Honest*

Identify and list arguments made. Provide commentary to support and challenge each of the claims. 

1. Transfer cash "real money" to computer cash "magical money"
   * Who actually gets you "real money" in this, just wondering and what is done with it if crypto is the way to go       
2. Digital money cannot be changed to most of the goods and services
   * I think this true, at least how I look at this. And after the exercise above I will be happy to use the "traditional" money     
3. The "cool factor" - makes you look good for tiny bunch of internet trolls
   * True maybe, but that is the case with many other things also, whether it is the latest super duper electrolyte drink that young these days couldn't survive. Maybe these guys don't show up in you instagram feeds to troll you when having a cup of old fashioned coffee.   
4. Blockchain - if you don't know what it is you are a good candidate to camble your real money
   * At least some part of it is true, Cryptocurrency has had its hype and maybe there were people involved and lost something due to fancy words and trying to be part of the hype.
   * But there has been other hype investements that maybe weren't that succesfull either.
5. Real money will come worthless and governments will collabse
   * How do you determine the value of crypto, then again for the money that we use now the value is just the same, we have just accepted it globally.             
6. Increase climate change - use of electricity
   * I think true to some point, there are also other things in IT sector that consumer lots of energy and we could do without.
7. Security risks
   * Wallet password forgot, scammers, hackers and tech in general fails
   * Risky business from many points if you don't know what you are doing. 
9. Investment - why would you wanna use it?
    * Maybe yes, cannot really say if it is good or bad investment, did the bubble already broke? 
10. Amateurs loose money, because they don't know what they are doing.
    * Defenetely would say this is true

Source: https://www.youtube.com/watch?v=GUs5y9leCyA
