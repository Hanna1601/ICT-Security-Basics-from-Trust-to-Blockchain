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
## 
> Karvinen 2022: Crackin Passwords with Hashcat

* Hashcat is a password recovery program that you can install in Linux terminal
* The idea in passwords is that systems don't store the orignal passwords they store hashes
  * If user input password Salasana123 the system stores in hash value that could look like this "1e4e7a154dsr4f366ab81f2ac3e3267i" (totally made up value)
  * When user retrieves the password they type Salasana124 and the systems compares the hash values and they don't match (in this case) the login is denied
* With Hascat you can make computer try the different words and tell what matches
  * After insalltion you tell the program the hash it need to crack and what type of hash it is cracking

Sources: https://terokarvinen.com/2022/cracking-passwords-with-hashcat/
## 
> Karvinen 2020: Command Line Basics Revisited, Voluntary
* $ - marks the normal user command promt, user doesn't need to write this. With # you can make a comment, then rest of the line is ignored. 
* $ ls - list files in working directory and $ pwd prints the working directory
* $ cd - change directory and you can give $ cd test/ - after that you workd in test directory. Getting back to main just write $ cd

* You can view text file and edit the file also.
* Create new directories (folders) and move and rename files forexample to that new directory

* In Linux there are important directories that you need to remember and they are the same in every Linux systems.
  *  $ / - root direcotry
  *  $ /home/ - home directories for all users
  *  $ /home/test - home directory for user test
  *  $ /etc/ - system wide settings
  *  $ /media/ - removable media
  *  $ /var/log/ - system logs
* There are also administrative commands like sudo, which allow to install and remove software, creating users and managing privileges. In order to use the you need to have the highest privileges. 

Sources: https://terokarvinen.com/2020/command-line-basics-revisited/
>**Please see [additional page] the points a-e. (https://github.com/Hanna1601/ICT-Security-Basics-from-Trust-to-Blockchain/blob/main/Task%20H3%20Hash%202.md)**
