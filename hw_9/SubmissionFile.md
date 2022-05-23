## Week 9 Homework Submission File: Networking Fundamentals II 

Please edit this file by adding the solution commands on the line below the prompt.

Save and submit the completed file for your homework submission.

---

Mission 1

Determine and document the mail servers for starwars.com using NSLOOKUP.

![nslookup_typeMX](image/nslookup_type=MX.png)


Explain why the Resistance isn't receiving any emails.

        The correct primary and secondary email servers for starwars.com are asltx.l.google.com and asltx.2.google.com

Document what a corrected DNS record should be.

        server: 8.8.8.8
        address: 8.8.8.8#53

        Non-authoritative answer: 
        starwars.com mail exchanger = asltx.l.google.com starwars.com mail exchanger = asltx.2.google.com


Mission 2

Determine and document the SPF for theforce.net using NSLOOKUP.


![nslookup_typetxt4spf](image/nslookup_type=txt4spf.png)



Explain why the Force's emails are going to spam.

        The mail exchange server has listed theforce.net IP address of 45.23.176.21 on a list of known spam senders. 

Document what a corrected DNS record should be.

    Server:		8.8.8.8
    Address:	8.8.8.8#53

    Non-authoritative answer:
    google.com	text = "v=spf1 include:_spf.theforce.net ~all"


Mission 3

Document how a CNAME should look by viewing the CNAME of www.theforce.net using NSLOOKUP.

![nslookup_q=cname](image/nslookup_q=CNAME.png)



Explain why the sub page of resistance.theforce.net isn't redirecting to theforce.net.

    The resistance.theforce.net is not listed as a cname for theforce.net in the nds server so queries for that site is not being forwarded to theforce.net. 


Document what a corrected DNS record should be.

    
    www.resistance.theforce.net CNAME theforce.net

 Mission 4

Confirm the DNS records for princessleia.site.

![DNS2](image/NSLOOKUP_NSSERVER2.png)





Document how you would fix the DNS record to prevent this issue from happening again.  

Add a secondary server

princessleia.site nameserver = ns26.domaincontrol.com                
princessleia.site nameserver = ns25.domaincontrol.com
princessleia.site nameserver = ns2.galaxybackup.com


Mission 5

View the Galaxy Network Map and determine the OSPF shortest path from Batuu to Jedha.

![Networking](image/Mission5.png)

Mission 6

Figure out the Dark Side's secret wireless key by using Aircrack-ng.

![Aircrack-ng](image/Aircrack-ng.png)



Use the Dark Side's key to decrypt the wireless traffic in WiresharkA.

Once you have decrypted the traffic, figure out the following Dark Side information:
Host IP Addresses and MAC Addresses by looking at the decrypted ARP traffic.


Document these IP and MAC Addresses, as the resistance will use these IP addresses to launch a retaliatory attack.


![ARP_Poisoning2](image/ARP_Poisoning2.png)


Mission 7

Follow the steps from the TXT record.


Note: A backup option is provided in the TXT record (as a website) in case the main telnet site is unavailable



Take a screen shot of the results.

![star_asciimation](image/STAR_ASCIIMATION.png)

![star2](image/STAR_ASCIIMATION2.png)







