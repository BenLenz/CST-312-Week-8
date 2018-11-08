# CST-312-Week-8
<b>CST 312 Week 8 Codepath
Pentesting Live Targets Challenge- Globitek</b>

Exploits Required:
1. Username Enumeration
2. Insecure Direct Object reference
3. SQL Injection
4. Cross-Site Scripting
5. Cross-Site Request Forgery
6. Sesssion Hijacking

<b>Blue Target:</b>
<br>
Vulnerability #1: An SQL injection is possible on the blue target using the saleperson URL. For example, I added ' OR SLEEP(5)=0--' to the end of the URL which succeeded and put the website to sleep for the time inside the bracket before loading again.
<a href="https://imgur.com/3vkqmY2"><img src="https://i.imgur.com/3vkqmY2.png" title="source: imgur.com" /></a>
<br>
Vulnerability # 2: There is a Session Hijacking vulnerability inside the blue target. There is a php form hidden that can be used to change the session ID. Using this form, you can session hijack the blue target and log in from anywhere given that session ID.<br>
<a href="https://imgur.com/4qQUWns"><img src="https://i.imgur.com/4qQUWns.png" title="source: imgur.com" /></a>
 
 
<b>Red Target:</b>
<br>
Vulnerability #1: There is an insecure direct object reference exploit that allows unlisted users to be found. The salesperson URL gives the user ID inside and from there simply changing the ID number can allow an attacker to access private user profiles that should not be available. 
<a href="https://imgur.com/DuRHrj7"><img src="https://i.imgur.com/DuRHrj7.png" title="source: imgur.com" /></a>
<br>
Vulnerability #2: It is possible to create a hidden form in the red target resulting in a cross-site request forgery exploit. The form created can automatically change salesperson data  which is highly illegal. Below is the hidden form: 
<a href="https://imgur.com/b0n41N6"><img src="https://i.imgur.com/b0n41N6.png" title="source: imgur.com" /></a>
<br>
 

<b>Green Target: </b>
<br>
Vulnerability #1: There is a small user enumeration vulnerability in the green site. On the other sites, there is no way to tell if you have a correct username with a password, however on the red site when you enter a correct username, the message displayed is in bold allowing an attacker to determine who is actually a user.
<a href="https://imgur.com/gR3z9hm"><img src="https://i.imgur.com/gR3z9hm.png" title="source: imgur.com" /></a>
<br>
Vulnerability #2: There is a way to store an XSS attack in the green target site. In the contact page, you can insert code such as <script>alert(‘still works’);</script> which simply shows a pop up box, but could potentially used to exploit the entire site. When a logged in user clicks on the feedback page, the stored XSS attack will activate.
<a href="https://imgur.com/9HE7EqF"><img src="https://i.imgur.com/9HE7EqF.png" title="source: imgur.com" /></a>

 
