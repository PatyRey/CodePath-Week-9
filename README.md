# Project 9 - Pentesting Live Targets

Time spent: **8** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: Insecure Direct Object Reference (IDOR)

Description: The website’s back-end is not sanitized properly, making it vulnerable to IDOR. In the example below you can see how changing the id parameter you can easily access the different ID’s and other restrictive information at the end of the “Find a Salesperson” page 


<img src="blue-vuln1.gif">


Vulnerability #2: Session Hijacking/Fixation

Description: The Website doesn’t regenerate the session ID, this makes it vulnerable to session hijacking and session fixation attacks. I used the provided PHP script "public/hacktools/change_session_id.php" to get the session ID. I loaded the script into two different browsers (Firefox and Chrome), one for hijacking and the other one for the target. First I log in on the target browser and copy the session ID, then in the attacker browser, I pasted the session ID.  

<img src="blue-vuln2.gif">

## Green

Vulnerability #1: Username Enumeration

Description: The website has the class “failure” with the existing usernames and the class “failed” for the ones that don’t exist. It also shows the log-in message in bold when the username matches the “failure” class, and the rest of the users that fall under the “failed” class will show the message unbold.

<img src="green-vuln1.gif">


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

Description: The website’s back-end is not sanitized properly, making it vulnerable to IDOR. In the example below you can see how changing the id parameter you can easily access the different ID’s and other restrictive information that supposed to be available until September 1st.

<img src="red-vuln1.gif">

Vulnerability #1: Cross-Site Scripting (XSS)

Description:

## Bonus
Vulnerability #1: SQL Injection (SQLi)

Description: 

<img src="blue-vuln3.gif">

## Notes

Cross-site injection (XSS) was the most challenging for week 9, there was a lot of traffic on the 2 different IP addresses, which made it difficult/ impossible to show my results on the feedback page, besides that, the exercise was very entertaining and informative
