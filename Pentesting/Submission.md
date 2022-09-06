## Week 16 Homework Submission File: Web vulnerabilities and Hardening 


Web Application 1: Your Wish is My Command Injection


1. Deliverable: Take a screen shot confirming that this exploit was successfully executed and provide 2-3 sentences outlining mitigation strategies.


![command_injection](images/Command_injection.png)

![command_injection2](images/Command_injection2.png)



The main problem with command injection are web applications that are not set up with user input validation protocols. Security professionals can use a whitelisting approach to validate user input only allowing certain IP addresses and search queries in the search bar on your web application. Anything beyond the approved list will be denied. Also if sensitive files are hosted on a segregated network is another mitigation strategy. Source: https://resources.infosecinstitute.com/topic/how-to-mitigate-command-injection-vulnerabilities/










    Web Application 2: A Brute Force to Be Reckoned With


2.Deliverable: Take a screen shot confirming that this exploit was successfully executed and provide 2-3 sentences outlining mitigation strategies.




![Burpsuite](images/burp_intruder5.png)



Captured the POST request in burpsuite sent it to intruder to isolate the username and password fields. Entered the payloads for field 1 and 2 from the breached intel. 


![burpintruder](images/burp_intruder4.png)





The attack did result in a sucessful login for tonystark and I am Iron Man


![intruder_render](images/burp_intruder2.png)


![intruder_raw](images/burp_intruder3.png)





Mitigation strategies are multifactor authentication. Stronger lockout guidelines that requre passwords to be changed after a shorter time period and require a more complex combination of letters, numbers, and special characters. Enable lockout requirements that only allow a certain number of failed login attempts. 

















    Web Application 3: Where's the BeEF?



3. Deliverable: Take a screen shot confirming that this exploit was successfully executed and provide 2-3 sentences outlining mitigation strategies.


Was able to inject malicious code into the message field on http://192.168.13.25/vulnerabilities/xss_s/. By inspect the HTML code I deleted the max field parameter of 50. Created a zombie of the web application. 


![xxs](images/xxs.png)





With my new zombie browser I sent the command to create a fake facebook login to attempt to obtain credentials. 


![facebook](images/facebook_login2.png)





Sent the command to create a fake popup bar. 



![popup](images/popup.png)






Sent a command to obtain the users home location.



![geo](images/geolocation.png)





Sent a fake adobe flash popup to potential install a keylogger or ransomware.


![adobe](images/adobe_flash_popup.png)







Mitigation strategies 

    Again content validation for any search fields to deny any file types being entered in a search field not expected to receive files or code. Content security policy needs to prevent browser exploitation attacks. 





