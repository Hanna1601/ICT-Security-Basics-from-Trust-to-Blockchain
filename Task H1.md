# H1 Summary of the articles and darknet diaries

## Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains

APTs (Advanced Persistent Threats) represent a significant risk to organizations, characterized by targeted intrusions that exploit vulnerabilities for economic or military gain. Traditional defenses often fail against these threats

**APT attack phases:**

1. Reconnaissance: Gathering information about the target.
2. Weaponization: Creating a deliverable payload 
3. Delivery: Transmitting the weapon to the target 
4. Exploitation: Triggering the payload to gain access.
5. Installation: Establishing a foothold in the system
6. Command and Control : Maintaining communication with the compromised system.
7. Actions on Objectives: Executing the intended goals, such as data exfiltration.

**The defender phases**
* Detect
* Deny
* Disrupt
* Degrade
* Deceive
* Destroy
  
The intrusion kill chain (attacker) need to be reconstructed , the analysis of the attack help to develope security measures by understanding the attackers tactics and techniques. 

*This took for me some while to read the article on to this as the IT Security is quite new topic when going to detail and the lingo of ITSec.*  
	
#### Sources: Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains

## Darknet Diaries - Episode 125: Jeremiah
	
* A penetration tester Jeremiah tells his experience conducting physical security assessments for a government contractor.
* The goal of a pen test is to identify as many exploitable vulnerabilities or findings as you can, and then present that and have them fixed as much as they can be fixed.
* The podcast starts by this guy telling how he was able to go to Buckingham Palace by climbing a drain pipe to a window and just going in. He was able to walk around the palace, drink some wine and not getting caught, going back the same way he came in. Just to make it more crazy he was able to do it again the same way.
* Jeremiah finds security holes in companies, trying to break into their buildings or networks. He is specialized in governmental parties
* Penetration test was done on a remote office that handled sensitive government work. This because attackers don't always attack straight to government but might attack contractor and thru that gain access to government network.
* Jeremiah found a contractor that did a lot of governmental work and he did a penetration test to the office to see if it is vulnerable.
* The test had specific constraints, such as not installing malware or backdoors, to minimize potential damage while still demonstrating possible security risks.
*  Reconnaissance: They did extensive research on the target location, including studying satellite images and street views. (Google). Who work there, what was the employee schedule
*  The team arrived at the location early in the morning, observed employee behaviors, when they started and ended their workday, where did they smoke.
*  He successfully entered the building by a faulty open door nobody checked. They dressed business casual like the other employees to blend in. To access office spaces they would need a key card
*  On the office floors they were able to scout people entering office spaces and see what could be their opportunity to enter them.
*  They also we able to use a computer in the lobby to get into the operating system. The computer was used for quest to sign in and it was designed to only have that one particular software open / in use.
*  After the lobby they wanted to see if they can access the office spaces and at least on that day the door was open for them to walk right in. The door has a keycard reader but it wasn't in use.
*  They were able to walk around the office, have a cup of coffee without anyone interrupting them. They could also see a lot of information that was on whiteboards and visible just walking around the office.
*  Using printers and ethernet cables they were able to access the network. 

*I think this was quite interesting penetration testing, I was once also listening to presentation of similar cases of ethical hacker. The security measures in companies aren't always that high, maybe in nowadays companies think about the physical locations more carefully.*

#### Sources: https://darknetdiaries.com/episode/125/

## "Tactic", "Technique" and "Procedure" in context of ATT&CK

* Tactic is the why of an attack technique, it is the attacker's tactical goal, the reason why is the attacker  performing this action. What is the attacker trying to achieve and what is the purpose of this phase in their attack. The purpose could for example be gather personal and sensitive data to do target attackers for example company personnel.
* Technique  is the “how” an attacker achieves a tactical goal by performing an action. How attackers are achieving their tactical goal and what specific action are attackers taking. In the tactic part the attacker gathered personal data to target attack, in this phase attacker can use the information gathered to get users open malicious file for example. This is phishing for example.
* Procedure are specific techniques the attackers use in attack. What are the steps attacker takes and what tools or commands attacker uses. In phishing the attackers can use spam campaings or target victims with more specific and personal emails that can feel more trusted. 

*I tried to choose examples from the site that would open up the topics more for me, for the not so technical person. The social targeting and phishing emails are starting to be quite familiar topic for most companies.* 
	
#### Sources: https://attack.mitre.org/resources/faq/ and https://attack.mitre.org/techniques/T1566/

## Additional questions A and B

A) How would you compare Cyber Kill Chain and ATT&CK Enterprise matrix? Who do you think could benefit from these models?
* I think the ATT&CK Enterprise matrix is more comprehensive, as the Cyber Kill Chain has 7 steps and describes things from the attackers point of view and more from high level. If I think company leadership the Cyber Kill Chain model is more easier to follow and understand. Going thru the ATT&CK site and the Enterprise matrix you have high number of models, examples of cases, I would see this more use for developers.

B) Pick a security incident and learn about it. Write briefly about it. Point out the concepts of threat actor, exploit, vulnerability and (business) impact. (You can find writeups about security incidents from Darknet Diaries and Krebs)
* I use the same case in this tasks that I opened up previously. Threat actor: In this case it was the penetrator testes, that posed as an attacker trying to get physical access to governmental contractor offices and also networks. They exploited human behavior, the followed their behavior to gain access and pretending to be an employee with no questions asked. There were vulnerabilities like weak or non-existing controls for physical access,  lack of employee awareness to challenge unfamiliar people, moving in the office and access to network was easy, lack of guidance employees left their computers unlocked, gaining control of kiosk- computer in the lobby, sensitive information visible to anyone. As this was a test the business impact could have been: compromised classified information and data, damage to company and loss of contracts. 


