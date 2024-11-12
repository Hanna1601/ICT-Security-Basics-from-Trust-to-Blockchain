# H3 Hashes part 2
> The Linux part of the homework

## A Billion dollar busywork
Command 'echo -n "hello"|sha256sum' prints a hash.  

![image](https://github.com/user-attachments/assets/261f2eb1-8f5d-4973-a94a-e485265abb16)

Try adding something to the string, e.g. 'echo -n 'hello asdf'|sha256sum'. 
![image](https://github.com/user-attachments/assets/bf6698ed-a9b1-4a8a-b430-60340fe25e26)

What do you have to add to get a hash that starts with a zero? 
* In honor of the missing light in November I tried out with few different versions and hello sun gave me hash that starts with 0
  
![image](https://github.com/user-attachments/assets/d1e2a69e-f673-4698-a497-ca8771d1dc53)

Voluntary bonus: How is this related to Bitcoin? 
* Bitcoins is only familiar to me as word, so this is just from the internet: In Bitcoin, SHA-256 is used for mining process (creation of bitcoins), but also in the process of generating bitcoin addresses. This is so because of the high level of security it offers.

Source: https://academy.bit2me.com/en/sha256-bitcoin-algorithm/

## B Compare hash 

Create a small text file. Take it's hash (e.g. 'sha256sum tero.txt'). 
* Created a text file called: taskb with text ![image](https://github.com/user-attachments/assets/f189712d-64bc-4f21-8532-7fb0624669b1)
  
  * Read the file content in terminal: ![image](https://github.com/user-attachments/assets/7fd30b9e-f30d-46f7-a77f-977739a2d9e2)
* Got the hash for it
  
![image](https://github.com/user-attachments/assets/07e80c55-d0f9-417a-a2f9-c568662fea51)
 
* Changed one letter in the file using nano from test to testi
  
![image](https://github.com/user-attachments/assets/051387ca-197b-4dbb-8c22-86bf9b5cda02)
 
* Take the hash again.
  
![image](https://github.com/user-attachments/assets/d2bbef6d-09dd-4343-814a-3570d6d5fb65)

Compare hashes, what do you notice?
* The hashes are totally different just by changing or in this case adding one letter

## C Hashcat 

Install hashcat and test that it works

![image](https://github.com/user-attachments/assets/112804bf-c363-4b97-82c7-e83e81589fb2)

* Added a new folder / directory hashed

![image](https://github.com/user-attachments/assets/75bd8bb2-4a9f-4dba-9840-b6d619dd994f)

![image](https://github.com/user-attachments/assets/c9bff60d-24ed-4bb2-a6c5-0d74da27f350)

* Got the rockyou directory from gtihub link (https://terokarvinen.com/2022/cracking-passwords-with-hashcat/) and saved it to directory hashed

![image](https://github.com/user-attachments/assets/f3272f3a-a3ab-426a-b3c7-4c546797ed7f)

![image](https://github.com/user-attachments/assets/52e9bb11-84cc-44bf-bf43-5e0bef73ecc9)

* Tested the hashid

![image](https://github.com/user-attachments/assets/5a4d912c-26c1-4dd7-84e2-0dde0ab51d17)

## D Dictionary attack 

Crack this hash: 21232f297a57a5a743894a0e4a801fc3

![image](https://github.com/user-attachments/assets/58583bb5-2ea6-4fc8-a0f2-57d3f287654c)

* I think I got the start correct but apparantly not enough memory
  
![image](https://github.com/user-attachments/assets/63db614d-d17f-4ff7-bd6f-461c64e56ce9)

* I added the memory to Virtual Box (with the help of google) and got different result
  
![image](https://github.com/user-attachments/assets/2f4d1217-2975-4a84-af51-6435ef5d0cd9)

* And to the the file solved got the password : admin

![image](https://github.com/user-attachments/assets/cd508f7c-fcac-4f16-a090-1a8e6aa083ec)

## E How can you make a password that's protected against a dictionary attack?

It's important to use robust, unique passwords, enable multi-factor authentication, and consider using a password manager to protect against dictionary attacks.
* add length your password as it increases the error needed to crack the password
  
Source: https://www.howtogeek.com/devops/how-to-protect-your-organization-against-password-dictionary-attacks/

## J John. 

Install Jumbo John (John the Ripper, open source Jumbo version). Compile it from source code as needed. 

* Followed the instructions got the error that it couldn find package zlib-gst and I couldn't find any help to this

![image](https://github.com/user-attachments/assets/f075895a-8152-490b-98e7-c3e2599b640d)

* Tried to move forward if the above error wouldn't matter, so moved on downloading the john.git
* but needed to first install the git because got error that git:command not found. After the installion the cloning was successfull.

![image](https://github.com/user-attachments/assets/b073af7a-e0bc-42d1-a844-b2f9393f0ee7)

![image](https://github.com/user-attachments/assets/25b91e68-e568-4e5d-95cd-b45a568e111d)

* Had to install the development headers based on error on previous part

![image](https://github.com/user-attachments/assets/0ff8075c-c9dc-4021-b986-dac5b0c4868a)

![image](https://github.com/user-attachments/assets/c9a8f477-9030-4b5a-9bc6-4ea25316d316)

* Ran the make and clean

![image](https://github.com/user-attachments/assets/67b603c0-4d09-4333-8208-7cdd450a49f2)

  
Source: https://terokarvinen.com/2023/crack-file-password-with-john/

* listed tons of files under john/run and was able to het the version so I think I managed to get it downloaded, compiled and running.
  * although I think the one error before will show up later to give hard time that I wasn't able to solve

![image](https://github.com/user-attachments/assets/37587ad1-95e7-42be-9093-f11538032ad8)


## K Crack file password with John

* Downloaded the tero.zip file and tried opening it

![image](https://github.com/user-attachments/assets/5de2ed06-3f90-4512-a570-ef158b54a1d3)

* Was able to get the hash to new txt file

![image](https://github.com/user-attachments/assets/d049098b-68b5-4c0a-99ff-6ac5e2c637f4)

* Encounted error that couldn't solve with the actual dictionary attack

![image](https://github.com/user-attachments/assets/3d626077-0469-48ac-8e06-a8bb118aa368)

* Was able based on instruction to read the file in terminal

![image](https://github.com/user-attachments/assets/c906a021-b611-46a5-b193-ce007de7362c)


