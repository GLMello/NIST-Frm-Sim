<h1>Simulation - Responding to a cybersecurity incident using the NIST Framework</h1>

 ### You can also read this in: [Português](https://github.com/GLMello/Sim-NIST-Frm)

<h2>Description</h2>
In this simulation I was tasked with analyzing a DDoS attack and creating an incident report by making use of the National Institute of Standards and Technology's Cybersecurity Framework (NIST CSF).

<br />


<h2>Scenario</h2>
You are a cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses. Your organization recently experienced a DDoS attack, which compromised the internal network for two hours until it was resolved.

During the attack, your organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack. 

To address this security event, the network security team implemented: 

· A new firewall rule to limit the rate of incoming ICMP packets

· Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets

· Network monitoring software to detect abnormal traffic patterns

· An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics

As a cybersecurity analyst, you are tasked with using this security event to create a plan to improve your company’s network security, following the National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF). You will use the CSF to help you navigate through the different steps of analyzing this cybersecurity incident and integrate your analysis into a general security strategy:

· **Identify** security risks through regular audits of internal networks, systems, devices, and access privileges to identify potential gaps in security. 

· **Protect** internal assets through the implementation of policies, procedures, training and tools that help mitigate cybersecurity threats. 

· **Detect** potential security incidents and improve monitoring capabilities to increase the speed and efficiency of detections. 

· **Respond** to contain, neutralize, and analyze security incidents; implement improvements to the security process. 

· **Recover** affected systems to normal operation and restore systems data and/or assets that have been affected by an incident. 

<h2>Resources </h2>

 ### [TCP/HTTP log](https://docs.google.com/document/d/1mLq-qSedt4ZS8SSAQMWuOQ2djibob38wkUJZS3zTCrw/template/preview?usp=sharing&resourcekey=0-yvXQeSsKts64mfpFG8Jm3Q)

<h2>Walk-through</h2>

<p align="left">
By analyzing the log I noticed the following connection attempts:
  <br/><br />
<img src="https://i.imgur.com/mb3ijXT.png" height="55%" width="55%" alt="Abnormal connections"/>
<br /><br />
This behavior goes on until the web server gets overloaded and ends up unable to respond to any connections.
<br /><br />
<img src="https://i.imgur.com/GbTdY1T.png" height="55%" width="55%" alt="Agravação"/>
<br /><br />
Following that, I decided to analyze the abnormal logs individually.
I was then able to notice two common factors between them: The origin IP address and the kind of packet that was sent. 
  <br/><br />
<img src="https://i.imgur.com/4EzNKAl.png" height="55%" width="55%" alt="Padrão"/>
<br /><br />
Henceforth, I was able to deduce that the attack was of the DoS SYN flood attack, since it originated from a single IP address and used exclusevely SYN requests.
<br/><br />
The final step was to come up with a report by using the deducted data along with the scenario information.
<br /><br />
<img src="https://i.imgur.com/yr793sv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h2>Note</h2>

 This project was part of the course [Google Cybersecurity Professional Certificate.](https://www.coursera.org/professional-certificates/google-cybersecurity) <br />
