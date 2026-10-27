# H1_CyberScience

## Review of the article

**Gagniuc, P. A. (2026). Why educated users still click: a review on phishing and the limits of human judgment. *Computer Science Review,* 62, 101025.**\
https://doi.org/10.1016/j.cosrev.2026.101025 \
JUFO 1

The article focuses on phishing, a form of socail engineering, and aims to answer next research questions:

* RQ1. Why do advances in automated phishing detection fail to eliminate phishing attacks in real-world settings?
* RQ2. Which technical, behavioral, and contextual factors most strongly sustain phishing success across platforms and attack types?
* RQ3. Why do awareness and training interventions show limited durability and transfer to real-world user decision behavior?
* RQ4. How do methodological choices in phishing research influence the interpretation of reported detection and defense effectiveness?
* RQ5. What role can structured, human-executable decision procedures play in improving consistency and reliability in phishing defense? 

### What are the key areas being researched?

* Phishing changed over time from simple fake bank emails to cloned websites, personalised social phishing, mobile and messaging channels and ready-made phishing kits (p. 4–5).
* Types of phishing attacks, grouped by the attacker’s goal are stealing login details, financial fraud (fake invoices, business email compromise) and malware delivery (p. 6–8).
* Technical features of phishing are suspicious URLs and domains, message content (urgency, authority), hosting infrastructure, and visually similar real websites (p. 8–9).
* Automated detection methods include blacklists and reputation systems, rule-based heuristics, machine learning, deep learning and hybrid systems (p. 9–11).
* Which psychological tricks make people click, and how time pressure, workload, demographics and work context affect this (p. 11–14).
* Awareness training, serious games and phishing simulations, and how long their effects last (p. 14–15).
* Human-in-the-loop defence: browser security indicators, warnings, decision support tools and explainable systems (p. 15–17).
* Structured human-executable decision procedures, meaning clear step-by-step checks that users follow before acting (p. 17–18).
* How research methods (lab vs. real world, static vs. time-based data) change the reported results (p. 10–11, 19).

### What's widely agreed upon?

* Phishing works mainly by exploiting human decisions, rather than technical weaknesses. Simple tricks still succeed, even against experienced users (p. 1, 11).
* The strongest psychological triggers are authority, urgency and fear of loss. Other effects, such as social proof, fatigue and multitasking, make these triggers stronger (p. 12–13).
* Time pressure and routine work reduce careful checking, even among users who know about phishing (p. 13).
* Single automated detection method is not enough. Blacklists work well against known threats but are weak during the first hours or days of a new campaign, when most victims are reached (p. 10–11).
* Attackers quickly adapt to defences, so detection features lose value over time (p. 8–9, 18–19).
* Targeted attacks, such as spear phishing and business email compromise, are the hardest to detect, because they have few technical warning signs and rely on context (p. 6–7).
* Training improves recognition in the short term, but the effect fades within weeks or months. Knowing the rules does not mean users follow them under pressure (p. 14–15).
* Users get used to security warnings and start ignoring them, especially when warnings are frequent or give false alarms (p. 13–14, 16).
* Lab studies and static datasets try to make defences look better than they are in real life (p. 11, 19).
* Combining automated detection, clear user guidance and organisational rules (for example, required verification of payment requests) works better than any single defence (p. 11, 21).

### What are the open questions?

* How to detect new phishing campaigns early, before blacklist and reputation data exist (p. 10, 21).
* How to keep detection effective when attackers keep changing domains, language and infrastructure. This has been little tested in real deployments (p. 19).
* How to make training effect longer, so that safe behaviour becomes a habit rather than just knowledge (p. 15, 20).
* How to measure real-world effectiveness. Many studies use small or student samples, lab settings, short follow-up periods or simulated click rates, and there is no standard way to evaluate defences (p. 19).
* Are step-by-step decision procedures really work in real organisations over a long time. The author calls them promising but they aren't yet properly tested in the field (p. 18, 21).
* How people interact with algorithmic guidance over long periods, including trust, fatigue and over-reliance (p. 19).
* How to protect users consistently across email, chat apps, social media and voice. Attackers move to the weakest channel, and users do not easily utilize their skills between channels (p. 19).
* How to adapt defences to each user’s risk level without breaking privacy rules or ethics (p. 20).
* How AI-generated phishing, deepfake voice attacks and multi-channel campaigns change the situation. The review leaves these mostly out because there is little long-term evidence yet (p. 3, 20–21).
* The role of demographics is still an open question. Early studies linked age or technical skills to risk, but newer studies suggest that context and work role matter more (p. 13).

## Threat modelling quickrun

NetStore, a large online and offline store that sells electronics and home appliances. It has about 800 employees, 2 million registered customers and a yearly revenue of about 500 million euros. Most sales happen online.

### Crown jewels
* **Data:** Customer database (names, addresses, phone numbers, order history). Online payments go through an external payment provider.
* **Business continuity:** Online store, CRM and ERP systems must be running. One day offline costs about 1.4 million euros in lost sales.
* **Reputation:** customers trust the company their personal data. A data leak would damage trust and make customers consider buying from competitors or send directly to them.
* **Money:** company bank accounts and payments to suppliers.

### Bad guys
Cybercriminals who want to get customer data to sell or to damage the company, or get money through fake invoices.

* **Capability:** high. Phishing kits and “phishing-as-a-service” make attacks cheap and easy.
* **Opportunity:** employee names and roles are easy to find in LinkedIn or other open channels. Customer service and finance department daily handle large amounts of emails and and some employee accounts don't have phishing-resistant multi-factor authentication (MFA).
* **Intent:** profit.
* **Why NetStore?** NetStore is a well-known brand with millions of customers’ personal data. Stolen data is rich and valuable and the public reaction makes extortion more likely to succeed.
  
### Risks (likelihood x impact = expected value per year)

1. Phishing steals an employee’s credentials, attacker then accesses the customer database, which leads to data leak.\
The impact would include incident response, lost customers and GDPR fine.\
10 % x 8 000 000 € = 800 000 €
2. Fake invoice. An attacker pretends to be a known supplier and requests finance to pay to a new bank account.\
20 % x 300 000 € = 60 000 €

Biggest is the Risk 1, the phishing based data leak. It's expected value would be 800 000 € per year.

### META
#### Mitigate
* Phishing-resistant MFA for all staff
* Customer service sees only the data it needs.
* Alerts when unusually big amount of customer data is downloaded.

As an expected outcome, Likelihood decreases from 10 % to 3 %, so the expected value falls from 800 000 € to 240 000 € per year.
#### Transfer
Insurance covers part of the incident response. Fines and reputation damage can't be transferred.
#### Eliminate
Partily solves the problem: delete data of customers who are inactive for over 3 years. Data that is not stored can’t leak.
#### Accept
The remaining risk of about 240 000 € per year.\

## Voluntary Bonus Tasks

### Email alert
I set the alert using Google Scholar alerts.

### Installing Linux on a virtual machine.
- Downloaded UTM Virtual machine software: https://getutm.app/
- Downloaded Kali Installer Image for x86_64: https://www.kali.org/get-kali/#kali-installer-images
- Installed UTM and then created virtual machine from Kali image.

### Technical puzzle
I have seen and used such symbol sequences before. I thought that this must be a string encoded with Base64, so I used a command line to decode it:
```
echo -n "==gCh8mclRFIs8GbsVGS" | base64 -d
```
Decoding didn't succeed:
```
base64: stdin: (null): error decoding base64 input stream
```
Typically two equal signs `==` appear at the end of the line and I thought that this particular line is probably reversed, so I decided to flip it before applying decoding again:
```
echo "==gCh8mclRFIs8GbsVGS" | rev
```
The output then was
```
SGVsbG8sIFRlcm8hCg==
```
Decoding this string
```
echo -n "SGVsbG8sIFRlcm8hCg==" | base64 -d
```
then returned 
```
Hello, Tero!
```