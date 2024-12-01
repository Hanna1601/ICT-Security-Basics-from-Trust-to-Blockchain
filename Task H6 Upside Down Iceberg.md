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
     
* II Background (to the end of "B. Circuit Establishent for Tor HS")
* 
* Fig. 6. Taxonomy for Tor attacks (Just the figure on page 2330.)

Sources: https://ieeexplore.ieee.org/ielx7/9739/9621320/09471821.pdf

## 
> Halonen, Ollikainen, Rajala 2023: PhishSticks - The Ethical Hackers tool for BadUSB

Source: 
