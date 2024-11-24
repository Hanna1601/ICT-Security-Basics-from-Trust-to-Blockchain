# H5 Watch and Summarice - Helsec

## Jos Helmich - Industrial Cyber Security
> Jos Helmich works at Konecranes and is member of ENISA (European Union Agency for Cybersecurity)

* The EU directives and laws that affect his company
  * Machinery directive - ensures common safety lavel in machinery   
  * RED - Radio Eqiplment Directive - Regulation of radio equiplment in the European union
  * GDPR - Data protection
  * NIS-2 - Network Inormation and systems, organizations are cyber resilient
    * The requirement are about the organisation's cybersecurity
    * If company has incident in this area they report to national authorities.
    * Keep your house in order and don't buy vaque stuff
  * CRA - Cyber resilience Act, digital products are cyber secure
    * If company has incident in this area the reports go to ENISA and not national level
    * Don't mess up someone else's house and don't sell bad stuff to the customer
    * Customer should ask that are the products you are selling cybersecure
  * AIA - Artificial Intelligence Act, rights and product requirements are taken into account by maker of AI product
 
 As they work in manufacturing indistry they also have cloud applications like fleet management and diagnostics. For office cloud the applications could be finance, trave, HR. 
 * They both have DM-zones that are a bit different
 * Other boxes he used were Dilbert Space and Industrial zone.
   * In DS are the workstations and the office nework, what is connected to the internet and protected with firewall
   * DMZ is the industrial network and it is protected by two different firewalls
   * The Industrial Zone is the ideal (which the speaker stated that really never happens) and it has no connection to the internet
 
 The presentor went thru quite extensively EU Legislation, the new legistlative framework in EU is modular. He also priefly touched on the US legislation that they need take into account when working in that market. 

## Heikki Juva - State of Union
> Heikki Juva works at Traficom, he tests consumer hardware and measure how these applications apply to regualtions
In his presentation he went thru the regulation RED and a case how he studies a consumer hardware

I think this presentation was quite interesting as it was more relatable to me. 

Timeline of legistaltion and regulations
* 11/2019 - Launch of the Traficom IoT Cybersecurity label
* 1/2022 -  RED standard work starts
* Q2 2024 - CRA standard work starts
* 08/2025 - RED is enforced
* ?/2026 - CRA vulnerability notification starts
* ?/2027 - CRA is enforced

The RED is in three parts
* 1: Network security
* 2: Protecting personal information of the user
* 3: Financial misuse

Test cases he selects are 10 most bought devices from webstores. The cireteria: Consumer-market, connected to internet, popular, blackbox testing (no access to its internal source code)
Is the device connected to network (RED 1), Does the device collect personal information, is is a smart toy or childcare quipment (RED 2), Does the device handle financial assets (RED 3). 
* Some questions when looking into the devices: Are software updates enforced, is device storage secure, no vulnerabilities, passwords are unique and strong.
* All the three different parts of RED had their own questions to look into when analyzing the device

* Most common issues with devices
  * Data is not removed
  * Sharing privacy information with 3rd part
  * Compex manufacturing, seller does not know how device works (R&D is outsourced)
* Some good findings
  * 90% use TLS and cert pinning (https://www.ssl.com/blogs/what-is-certificate-pinning/)
  * 80% implemented on baremetal (no operating system)
  * 66% use wifi for communication
  * 90% are online only temporarily, which makes it harder to hack as the device is not connected to network 24/7

There was few points to reminding you to read the legal text before start using the device. Maybe you should do this even before buying?
* For example data gathred, even if you empty the device you cannot be sure that it is not stored in the cloud. What are they doing with the data?
* Even after wiping the device, some data can be still stored for example one case still stored Wifi password. 

>**More on Heikki's thoughts on RED-CRA you can read [here](https://github.com/Zokol/RED-CRA)**
 
 
