# Attacking-Documentation-
Lab testing: Phising and Credential Harvesting
#AUTHOR
Charles Adedeji Adeola; Offensive Security Focus

#PROJECT OVERVIEW

This documentation explains how I planned, executed, and analyzed a phishing attack using Zphisher, a phishing toolkit used for cybersecurity training and awareness.
The goal of this project is to demonstrate how attackers create social engineering traps.

1. Understanding the Objective

Phishing attacks rely on:

-Creating a convincing fake login page

-Sending a deceptive link to a target

-Collecting whatever credentials the victim enters

-Zphisher makes this easier by providing:

-Prebuilt website clones (Facebook, Gmail, Instagram, etc.)

-Automatic hosting (local or via tunnels)

-Credential capture logging

>Key Point:

-Zphisher works ONLY when the victim clicks the link and enters information.

2. How the Attack Was Performed

For this project, I first performed generated a phishing page using Zphisher and sent the link to my defensive partner to simulate a real attack.

My Attack Plan:

-Perform Social Engineering about my target 
<img width="1366" height="720" alt="first pic" src="https://github.com/user-attachments/assets/4dfa2818-fa7b-4306-8dcc-699052521335" />

-Clone a login page of LinkedIn us
<img width="556" height="494" alt="523478983-c3b14b20-36b0-4203-a586-5169dedb33c3" src="https://github.com/user-attachments/assets/f6c8406a-df0a-4b7d-b1be-434fc20dc473" />
ing Zphisher

-Host it using a tunneling service
<img width="379" height="118" alt="523479109-68ff5315-9adb-4fa2-a4e7-5ebb99f7ebfa" src="https://github.com/user-attachments/assets/13b8865f-e4a4-45bf-8c0c-58ee480b0bf3" />

-Create a urgent believable message to trick the victim
<img width="1366" height="720" alt="pic 2" src="https://github.com/user-attachments/assets/bd7a4ee6-b4f2-4da4-bf1f-3d9a89919f6f" />

-Wait for any interaction
<img width="432" height="78" alt="523479185-b7451228-52d2-46bc-a04c-d0693f62f751" src="https://github.com/user-attachments/assets/d78534cf-2f5d-415e-b82a-ee889acd7dcc" />

-Capture entered test credentials if my victim does put is credentials 

>Why Zphisher?

-It is simple and fast

3.1 Choosing the Hosting Method

I used one of Zphisher’s tunneling options from this:

ngrok / cloudflared / localhost

I used a localhost for this.

This allowed my phishing page to be accessible over the internet during the exercise.

3.2 Preparing the Phishing Message

I crafted a short, urgent message to increase the chance of a click:

“Unusual login detected — confirm your identity.”

Similar messages are:

“Session expired, please log in again.”

“Security verification required.”
These types of messages exploit human behavior.

3.3 Deploying the Attack

I sent the phishing link to the defender.

Zphisher then started tracking:

IP address of the visitor

Time of visit

Any credentials typed

Device info (if available)

No real accounts were used — only lab-based testing.

4. What Zphisher Captured

During the testing phase, Zphisher recorded:

The test device accessed the link

Attempted interactions

HTML requests

Timestamp logs

Even though my partner didn’t fall for the trap, the toolkit still logged:

Page visits
/home/prince/Pictures/Screenshot_2025-10-29_07-03-41.png
Failed attempts

Redirect attempts

This provided insight into how users behave during simulated phishing scenarios.

5. Attack Analysis

From my perspective as the attacker:

What Worked Well

The cloned login page looked convincing

The urgent message increased alarm and sense of urgency 

Tunneling made the link accessible

What Didn’t Work

Defender inspected the URL carefully

Lack of HTTPS exposed the fake page

The domain clearly wasn’t legitimate

Browser warnings reduced believability

This shows that trained defenders can catch phishing attacks quickly.

6. Lessons Learned (Attacker POV)

This exercise improved my understanding of:

How phishing kits generate fake pages

How tunneling services help attackers

How users can be tricked psychologically

What clues defenders look for

How important URL and certificate checks are

Most importantly, it showed that user awareness is the strongest defense.

7. Ethical Notice

This attack was performed ONLY in a controlled cybersecurity lab environment.
No real users, accounts, or external systems were involved.
