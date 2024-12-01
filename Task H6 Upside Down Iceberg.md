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
    * Ent - to end attacks are not completely solved in Tor
    * Protocl normalization is not provided by Tor
    * Tor doesn't conceal who is connected to the network

Sources: https://css.csail.mit.edu/6.858/2022/readings/tor-design.pdf

##	
> Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey.

* Abstract and Introduction
  * The need for privacy in the internet has led to the development of anonymous communication systems.
  *  Tor is currently world's most popular anonymity network, that provides anonymity to users and supports the deployment of aononmyous services (hidden services).
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
