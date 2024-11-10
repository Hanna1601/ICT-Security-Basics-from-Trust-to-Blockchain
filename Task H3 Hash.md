# H3 Hashes
> Homework for task H3

## Read and summarize
> Schneier 2015: Applied Cryptography, subchapter 2.3 One-way function and 2.4 One-way hash functions

* 2.3 One-way function
  * Central concept in public-key cryptography and fundamental building block for different protocols
  * Example to open the one-way function: breaking a glass in to million pieces is easy, but putting it back together to one glass from those millions of pieces isn't that easy
  * Cannot be used as is for encryption for example messages, because it couldn't be decrypted. 
  * Trapdoor one-way function makes is possible to compute the function to the other direction if you know the secret.
    * You can think the secret like a insctruction to put together Ikea furniture, much easier, coulf still lead to despare but you get the finished furniture as end result.

* 2.4 One-way hash function
  * Central part of modern cryptography and building block for many protocols
  * Hash function:
    * Has been used in computer sience for a long time
    * Takes input string (pre-image) and converts it to a fixed lenght output string (hash value)
  * One-way hash function is collision-free, it is hard to genrate two pre-images with the same hash value.
  * Hash function is public, the security comes from the one-way of hash function
    * If the pre-image changes even slighlty it changes the hash value also, so it is computationally impossible to find pre-image that deliveres the same hash value
  * Message authentication code (data authentication code) is a one-way hash function with a secret key
    * the hash value is a function of the pre-image and the key
    * someone with the key can verify the hash value
    
Sources: https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003

> Karvinen 2022: Crackin Passwords with Hashcat


Sources: https://terokarvinen.com/2022/cracking-passwords-with-hashcat/
