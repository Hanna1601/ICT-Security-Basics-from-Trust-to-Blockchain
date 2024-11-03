# H2 Summary of the articles 

>This page summarizes the articles in homework 2

## Read and summarize Chapter 2 - sections 2.5 - 2.8 of Applied Cryptography

### Section 2.5 Communications using public-key Cryptography

* The history of public-key cryptography goes back to 1976 to Whitfield Diffie and Martin Hellman.
  * They used public and private key, where anyone with the public key can encrypt the message but not decrypt it, only with the private key you can decrypt it.
  * Before that in 1974 Ralph Merkle invented the first construction of public-key cryptography using puzzles where no keys were send between parties
    
    ![image](https://github.com/user-attachments/assets/ca8c20af-b2a7-4d6b-8b1b-d1082cc2a88e)

* Public-key algorithms are used to encrypt key, not messages.
* They are also used to secure and disitribute session keys, the keys are used with symmetric algorithms to secure message traffic.
   --> Hybrid cryptosystem
    * The session key is created when it is needed to encrypt communications and destroyed when it is no longer needed

### Section 2.6 Digital Signature

There are many digital signature algorithms. All of them are public-key algorithms with secret information to sign documents and public information to verify signatures

* Handwritten signatures are considred as a proof of authencity, but that is not the case at all. Signature can be forced, documents can be altred after signing. If the old way of doing this is hard how can you do this with the help of computers?
  * Files on computers are easy to copy
  * Simple cut and paste of signature from one document to another is easy
  * Files are also easy to modify after they are signed without leaving any evidence behind
 
* Signing documents with symmetric crypsosystems and an arbitrator
    * The arbitrator shares diffrent secret keys with both signing parties
    * Time consuming for the arbitrator as lot of time goes to decrypting and encrypting messages
    * The trust to the arbitrator needs to be there from the community
          
* Signing documents with public-key crypthography and timestamps
  * There are public-key algorithms that can be used for digital signatures where arbitrator isn't needed to sign or   verify the signature. --> The arbitrator is needed to certify the public used 
   * Digital signatrue often include timestamps, the date and time of signature at attached to the message
       
* Signing Documents with Public-Key Cryptography and One-Way Hash Functions
  *  Digital signature protocols are often implemented with one-way hash function
  *  Both the one-way hash function and the digital signature algorithm are agreed upon beforehand
 
### Section 2.7 Digital Signature with encryption

Digital signature with public-key cryptography is protocol that combines the security of encryption with authencitiy of digital signature. 

* The public-key/private-key key pair for encrypting and signing can be different
* Signing before encrypting prevents unauthorized message alteration and keeps the signature legally binding.
  
### Section 2.8 Random and pseudo-random-sequence generation and cryptographically secure pseudo-random sequences

* Random-number generators are almost definitely not secure enough for cryptography
  * They don't produce a random sequence

* A pseudo-random sequence is one that looks random
  * sequence's period should be long enough
  * all computer-generated sequences are somewhat periodic and subject to small, detectable patterns over time.

*  Cryptographic randomness doesn't mean just statistical randomness
  * For a sequence to be cryptographically secure pseudo-random it needs to be unpredictable

Source: https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec005

## Read and summarize Chapter 2 Cryptographic hash functions and digital signatures

### Cryptographic hash functions
* Bitcoin uses cryptographic hashes and one cannot learn Bitcoin without knowing the hashes
* You can compare a cryptographic hash to a fingerprint on particular finger, these is no same in the entire world, yet it doensn't reveale any personal data about the person, it just a fingerprint.
  * Hash = something that is chopped to small pieces what does it mean in the world of computers?
    * It takes something, for example a picture, performs mathematical calculations on it and out comes a big unique number that doesn't resemble the orgianal picture
    * Cryptographic hash functions can be used as an integrity check to detect changes in data
      
### Digital signatures

Digital signature is tied to a random number called a private key ant it is much harder to forge than a handwritten signature.
The private and public keys are a pair because they have a strong relationship: 
* The public key can be used to encrypt messages that only the private key can decrypt
* The private key can encrypt messages that only the public key can decrypt

Source: https://learning.oreilly.com/library/view/grokking-bitcoin/9781617294648/OEBPS/Text/kindle_split_011.html#ch02lev1sec1

## Read and summarize PGP - Send Encrypted and Signed Message - gpg

PGP = Pretty Good Privacy, encryption
GPG = The tool 

These can be used to encrypt emails, many email applications encrypt messages automatically.
The article tell how to you PGP and GPG in Linux to encrypt messages on command line. 

* First steps are setting up trust or other words excganging the keys and the setting up the required tools to do this
* Second step is sending the messages and encrypting them
* Thrid step the receiver decrypts and verifies the message 

Source: https://terokarvinen.com/2023/pgp-encrypt-sign-verify/

## Task A

* Pubkey today. Explain how you have used public key cryptography today or yesterday, outside of this homework. In addition to naming the system, identify how different parties use keys in different steps of the system.

I use Apple Pay quite often, it comes in handy when forgetting wallet at home. 


Source: https://developer.apple.com/documentation/passkit_apple_pay_and_wallet/apple_pay/payment_token_format_reference#//apple_ref/doc/uid/TP40014929-CH8-SW3
 
## Task B

* Messaging. Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. Don't use Tero as a name of any party, unless that's your given name.)

## Task C

* Other tool. Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen.

## Task D

*Eve and Mallory. In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)

 ## Task F
 
 * Password management. Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)

 ## Task G
 
 * Refer to sources. Verify each homework report (this and the earlier ones) refers to sources. Every homework report should refer to this task page. It should also have references to any other source used, such as web pages, LLMs, man pages, other reports... References are mandatory, and must be present in every report. (This subtask does not need a report, you can just do it and write "Done." as the answer for this subtask.)


