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
