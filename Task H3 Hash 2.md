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

## E How can you make a password that's protected against a dictionary attack?


![image](https://github.com/user-attachments/assets/27a01260-7257-442e-813f-2726dd003c7f)





