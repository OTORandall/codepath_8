# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection
                  When we put the script " ' OR SLEEP(5)=0--' " in the url the website will pause for 5 seconds.

Vulnerability #2: Session Hijacking/Fixation
                  When the target log in the the blue website, we get the session ID from it. We open another blue website in other brower and we haven't log in yet. Now we set the session ID we acquire from the loged in website in the new blue website throuht the link "public/hacktools/change_session_id.php" and then when we go back to the website we now log in already.


## Green

Vulnerability #1: Username Enumeration;
                  In other color websites, when we enter the correct username and wrong pwd, it will show the error message in bold. And when we enter wrong username and wrong pwd, the error message is also bold. But in green, correct username and wrong pwd will result in bold error message but wrong username and wrong pwd will result in NOT bold error message. 

Vulnerability #2: Cross-Site Scripting;
                  When we insert the script into the comment in the feedback page and log in the check the comment, the scriipt is not filtered and the comment will be blank. However, other websites will filter the script out the just print out the script.


## Red

Vulnerability #1: Insecure Direct Object Reference;
                  In the red website, through manipulating the "id" parameter in the url we can access the details of the saleperson Testy McTesterson whose id is 10 and Lazy Lazyman whose id is 11, which is not supposed to be shown because it is secret. In other websites, we cannot access these pages. They will redirect us back to find a salesperson page.

Vulnerability #2: Cross-Site Request Forgery
                  


## Notes

Describe any challenges encountered while doing the work
