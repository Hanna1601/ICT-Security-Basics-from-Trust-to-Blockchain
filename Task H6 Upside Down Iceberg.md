# H6 Upside Down Iceberg
> Homework for task H6

## Read and summarize
> Dingledine, Mathewson and Syverson 2004: Tor: The second-generation onion router.

* Chapter 3 Design goals and assumptions
  * Deployabilty: The design must be used in a real world, so it can't be too expensive to run, must avoid creating a substantial liability burden for operators, implementation should be relatively easy and affordable. 
  * Usability is a security requirement, if it is hard to use fewer people use it. And Tor is about user anonymity, so with fewer users the less anonymity it provides. How is this acheived? - not required to modify familiar applications, no unreasonable delays, configuration decisions to minimun, easy to implement on all common platforms from Windows to Mac etc.
  * Flexibility and simple desing: The protocol must be flexible and well-specified, so Tor can be used in testing for future desings. The protocol design and security must be understood, simple and stable system that has the best accepted approaces to protect anonymity. 
  * Non-goals: As Tor favors simple and deployable designs some goals are not yet implemented because they are now yet solvable or they are solved elswhere.
    * Peer - to - peer environments has too many open problems still.
    * End - to end attacks are not completely solved in Tor
    * Protocol normalization is not provided by Tor
    * Tor doesn't conceal who is connected to the network

Sources: https://css.csail.mit.edu/6.858/2022/readings/tor-design.pdf

##	
> Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey.

* Abstract and Introduction
  * The need for privacy in the internet has led to the development of anonymous communication systems.
  *  Tor is currently world's most popular anonymity network, that provides anonymity to users and supports the deployment of anonymous services (hidden services).
  * The anonymity is also being misused in many ways. Due to the misuse governments and law enforcment are interested in attacks that aim to de-anonymising the Tor network.
  * In response to these de-anonymisation attacks users expected anonymity is being strengthened by improving security and fixing known bugs.  
     
* II Background for taxonomy and the attacks discussed in the paper
  * Onion Proxy (OP) or Tor client is a software installed to user's device, enableling communication with the directory servers, connects to Tor network and handles connections from the user's applications.
  * Directory servers (DS) are trusted and known servers in the network, they produce a document about the network that the OPs can download to establish communication circuit to a destination.
  * Entry Node / Guard is the relay where client connects to and it knows the Ip address of the client. Early Tor attacks used this to de-anonymise users.
  * Exit node knows the IP address of the destination served accessed thru Tor network.
  * Hidden services known also as Onion services, can be hosted on a node inside Tor network or an external node. The anonymity provided attracts those who are envolved in criminal activity.
  * Introduction points are random nodes that HS selects to register its services, several of these are usually selected to avoid impact from Denial of Service. The introductions points don't know the IP address of the HS due to connection via complete Tor circuit.
  * Rendevous point is a random Tor node, that is selected by the client OP before connection is initialised.
  * Bridges were created mitigate a list of relays in Tor network to avoid blocking the Tor network. 

* A Standard Tor Circuit Establishment
  * A circuit thru Tor network must be established by a Tor client before communicating over network
  * Onion proxy must be installed on the device used for browsing. The OP contacts a DS and gets a list of active relays. Three relays are selected (entry, middle and exit nodes), a circiut is created incrementally by exchanging encryprion key with each node --> known also as hops.
  *  Once three hops connections has been established the user can communicate with destination server over the circuit just created. 
  
* Circuit Establishment for Tor HS (hidden service)
  * HS selects multiple introduction points from the available nodes in the Tor network and builds connections to those nodes
  * HS connects to DS and advertises a service descriptor with public key, exp.time details of selected introduction points --> owner of HS can advertise HS's onion address in multiple platforms
  * If user wants to access a HS they need the onion address

* Fig. 6. Taxonomy for Tor attacks
  * Attacks on Tor can be divided into four different categories; Network disruption, Censorship, Generic and De-anomymization attacks of which the last is looked in to more carefully.
  * De-anonymization attacks can be divided into four; side channel, entry and exit routers, OP/OR/Server ja hybrid.
  * All of these attacks can be categorized in to active and passive attacks. 

Sources: https://ieeexplore.ieee.org/ielx7/9739/9621320/09471821.pdf

## 
> Halonen, Ollikainen, Rajala 2023: PhishSticks - The Ethical Hackers tool for BadUSB

* PhishSticks can be used to malicious attacks when usb devices is plugged in, compromising you personal or company data
* On the video it was a keylogger payload, attack is visible a split second and the program installed records every keystroke made on the computer
  * Getting for example credentials to user email, the logged data is stored in the victim's temp folder
  * PhishStick sends the information to attacker via HTTP post
  * PhishStick removes the logged data after it has been sent

*No harm was caused to CEO*

Source: https://www.youtube.com/watch?v=bDzVevtZiWE

## A Install TOR browser and access TOR network
* Tried installing the tor thru terminal but that didn't work out so well, got error for torbrowser-launcher that is doesn't have any installation candidates so I think I missed some steps. 
* Went forward with downloading the package from their website
  
<img width="674" alt="image" src="https://github.com/user-attachments/assets/a6879ee7-ff33-42a9-a155-87b19abba3ee">

<img width="573" alt="image" src="https://github.com/user-attachments/assets/001d3104-a2a2-4931-9336-c0df384a51ba">

* Got the package
  
<img width="207" alt="image" src="https://github.com/user-attachments/assets/a401ca2a-a14c-48db-baf4-a35e510dabf3">

* Verifying the signature using steps in torproject.org but got stuck
  
<img width="526" alt="image" src="https://github.com/user-attachments/assets/a0fe6042-43fe-455e-86c1-359c3313b678">

<img width="377" alt="image" src="https://github.com/user-attachments/assets/0c6e0947-7aa5-46f4-a0f7-d0ce05750935">

* So resuming installing the browser, extracted the files and clicked from the files start-tor-browser

<img width="374" alt="image" src="https://github.com/user-attachments/assets/77564327-4880-4da8-8f2f-901867536563">

* And success

<img width="414" alt="image" src="https://github.com/user-attachments/assets/df637004-e58d-4100-8e46-767406556d8d">

<img width="440" alt="image" src="https://github.com/user-attachments/assets/5d662773-262a-4504-b53e-f92d3a4dafd5">

Sources: https://www.torproject.org/download/

## B Browse TOR network
* Tried searching something - went with MTV3 to check the news they have to offer
  * Accessing their page didn't work but wikipedia page about them opened up ok

<img width="263" alt="image" src="https://github.com/user-attachments/assets/d9fe9c9c-d71b-4dd0-8874-c7c2efef54a2">

<img width="409" alt="image" src="https://github.com/user-attachments/assets/e78ea505-3bae-4234-b2b4-5337c1fb1362">

* Visited EFF site

<img width="645" alt="image" src="https://github.com/user-attachments/assets/f4bfb3eb-3389-4e00-9760-9ae748219039">

## C Onion
> In your own words, how does anonymity work in TOR? How does it use: public keys, encryption, what algorithms

* TOR (The Onion Router) enables online anonymity, it directs internet traffic whrough a network of relays of which many are set up and maintained by volunteers
  * TOR circuit consist of Guard, Middle and Exit relays, in some cases there can be a bridge relay
  * Messages are protected with multiple layers of encryption, like wrapping them in several layers of security, just like an onion has many layers.
  * Traffic is allowed to pass onto or through the network through nodes that only know the node right before them and the one right after them. Its like passing a message down the line where each person only know the persons next to them.
  * The Tor browser is automatically connected to Tor Network and all requests are placed through it, ensuring autonymity. Tor browser makes all it users look the same, making it harder to indentify you. 

* Tor uses different keys with three different goals --> 1. encryption to ensure privacy, 2. authentication so clients know they are talking to relays meant to talk to, 3. signature to verify that all clients know the same set of relays
  * Connections in Tor use TLS (Transport Layer Securit) link enrycption, Tor client also establishes an ephemeral encyrption key with each relay in the circuit (the neighbour example). Also they circuit key is discarded by both sides after usage.
* The Tor software comes with a built-in list of location and public key for each directory authority
* Algorithms used AES-256 adn SHA3-256
  
Sources: 
https://portswigger.net/daily-swig/tor-security-everything-you-need-to-know-about-the-anonymity-network
https://support.torproject.org/about/key-management/

## D What kind of the threat models could TOR fit?
I am not totally sure how to look at this question so I am looking this from the viewpoint that person or company is using TOR. 
* Focus on privacy, anonymity and network security
  * Protect against surveillance or censorsip. This might not be so close to us in western countries from government side but from big companies wanting your data.
    * Tor anonymizes your browsing, making it hard to trace your activity back to you.
  * Attack tree modelling where potential attacks are described in tree like modelling.
    * If using Tor the attack tree could be used to illustrate routes the attackers might take to deanonymize users.

Sources: https://www.practical-devsecops.com/types-of-threat-modeling-methodology/

## E Don't stick that stick
> How does PhishSticks attack work? 
* USB device is used to attack with malware to a computer, they exploit human being curious and maybe having a trust to everyday devices.
  * Malware can be a keylogger as opened in the first part read and summarize, ransomware where for example application from USB device encrypts your files and ransom is demanded in order to decrypt the files. Revershell is also one, where connection from victims computer to attackers computer is established. 
> Would a typical organization be vulnerable?
* I think this depends for example company policy. To some extend in companies I think USB-memorysticks are prohibited (disable removable disks for devices).
  * Of course there is always room for human error, even though education is in place.
  * Maybe smaller organisations are more vulnerable to this where IT isn't the main thing
> Does this link to a broader category of attacks and defenses?
* With USB devices attackers can bybass traditional security defenses like antivirus and firewalls.
  * Usually computer recognise these devices as trusted like a keyboard
  * Public USB Charging stations can be compromised and when charging your company phone a malware is installed to you phone.
  * Exploit human curiosity and computer autorun functions
> How the risk could be mitigated?
* The easiest as stated in few different sources, don't plug unknown devices to your computer or mobile pohone.
* In the PhishSticks project they used powershell, that should be disabled from users and for home computers there should be different administrator privilages from daily use.
* Disable AutoRun features - prevents automatic execution of programs from USB devices
* USB Port Control for company devices to restrict which devices can be connected
* User education

Sources: 
https://github.com/therealhalonen/PhishSticks
https://www.youtube.com/@phishsticks_pentest/videos
https://www.redzonetech.net/blog-posts/bad-usb
