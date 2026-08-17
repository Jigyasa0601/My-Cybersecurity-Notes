# ROOM: BECOME A HACKER 
**TryHackMe Link**: [BECOME A HACKER](https://tryhackme.com/room/becomeahackeroa?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a5ba5be99ab54f7c1dacca7)<BR>
**Category**: CTF <BR>
# What I Learned
## What Is Offensive Security
Offensive security is the process of breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access to them, while defensive security builds shields and monitors networks to block and respond to live threats. Together, they form a complete cybersecurity strategy.<BR>

**Offensive Security (Red Team)**<BR>
* Goal: Find flaws by acting like an attacker.
* Action: Ethical hacking and penetration testing.
* Mindset: Proactive (attack first to fix later).

**Defensive Security (Blue Team)**<BR>
* Goal: Protect data and keep intruders out.
* Action: Set up firewalls, patch software, and watch for alerts.
* Mindset: Protective and responsive (guard the system).
# How I Completed The Room
Here I,ll explain step-by-step to complete this room:<br>

**Task-1**: Read the passage and answer the question in which it is asked about when a hacker tries to find vulnerabilities in a system what does it simulate about his/her actions so the answer is `Offensive Security`.<br>

**Task-2**: In task-2, view the site and help *Mike* to find the bugs and weaknesses in his `Web Application` so he can work on it and fix the vulnerabilities of his web application and protect it from potential cyber threats before he makes it public. So by using gobuster we found the name of the hidden page i.e, `login`.<br>

To discover any hidden pages, here are some pages to try:<br>
* **sitemap** (In other words, we use the embedded browser to check if http://www.onlineshop.thm/sitemap exists.)
* **mail** (As you guessed, we check if http://www.onlineshop.thm/mail exists.)
* **login**
* **register**
* **admin**
* Using an Automated Tool: **Gobuster**

Changing the browser’s address bar is helpful if the list of pages you want to try is limited. If we have hundreds or thousands of words to try then, we need to use an automated tool. A solid tool to automatically search for hidden pages is `Gobuster`, which runs in the terminal. In the terminal, in the lower right, we need to issue the following command:<br>
`gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt`<br>

The command above is made up of the following parts:<br>

* **gobuster** is the terminal command to start Gobuster
* **dir** uses directory and file enumeration mod
* **--url http://www.onlineshop.thm/** sets the target website
* **-w /usr/share/wordlists/dirbuster/directory-list.txt** specifies the word list to use<br>

**Task-3**: In the task-3, we have to find the secret message. By using the information below we can easily find out the hidden message after performing the tasks I the secret message I got is `born_to_be_hacker`.<br>

Using an Automated Tool: **Hydra**<br>
We could do this task manually, as we only had to go through five passwords. But what if we have to go through thousands or tens of thousands of passwords? In that case, we can use a software tool such as Hydra. In the terminal, on the lower right, let’s run the following command:<br>
`hydra -l admin -P passlist.txt www.onlineshop.thm http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V`<br>

The command above is made up of the following parts:<br>
* **hydra** is the terminal command to start `Hydra`
* **-l** admin attempts to log in using the username `admin`
* **-P** *passlist.txt* specifies the password list to try
* **www.onlineshop.thm** sets the target website
* **http-post-form** indicates that this is an HTTP POST request form
* **"/login:username=^USER^&password=^PASS^:F=incorrect"** specifies the shape of the HTTP POST request and how to check if the login credentials are incorrect
* **-V** is used for verbose output

# What careers are there?

The cyber careers room goes into more depth about the different careers in cyber. However, here is a short description of a few offensive security roles:<br>

**Penetration Tester** - Responsible for testing technology products for finding exploitable security vulnerabilities.
**Red Teamer** - Plays the role of an adversary, attacking an organization and providing feedback from an enemy's perspective.
**Security Engineer** - Design, monitor, and maintain security controls, networks, and systems to help prevent cyberattacks.