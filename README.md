# Attacking-Documentation-
Simulated Phising and Credential Harvesting
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

For this project, I generated a phishing page using Zphisher and sent the link to my defensive partner to simulate a real attack.

My Attack Plan:

-Clone a login page of LinkedIn using Zphisher

-Host it using a tunneling service

-Create a urgent believable message to trick the victim

-Wait for any interaction

-Capture entered test credentials

>Why Zphisher?

-It is simple and fast

3.2 Choosing the Hosting Method

I used one of Zphisher’s tunneling options from this:

ngrok / cloudflared / localhost.run

I used cloudflared for this.

This allowed my phishing page to be accessible over the internet during the exercise.

3.3 Preparing the Phishing Message

I crafted a short, urgent message to increase the chance of a click:

“Unusual login detected — confirm your identity.”

Similar messages are:

“Session expired, please log in again.”

“Security verification required.”
These types of messages exploit human behavior.

3.4 Deploying the Attack

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
