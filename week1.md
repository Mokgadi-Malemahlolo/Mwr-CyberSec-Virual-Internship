# Week 1: Burp Suite Fundamentals

**Focus:** Getting familiar with Burp Suite – the most commonly used tool for web application hacking.  
**Goal:** Understand where and when to use each component, not just answer questions.

---
## Link to room:[ https://tryhackme.com/jr/MWR-CyberSec-Week-1-8w-9ypa]  
## 📌 Workshop Topics Covered
- What is Burp Suite? (Editions, features)
- Burp Community features (Proxy, Repeater, Intruder, Decoder, Comparer, Sequencer)
- Burp Options (Global vs Project settings)
- Target & Proxy workflows
- Intruder attack types
- Repeater & Inspector
- Decoder & encoding
- Comparer & Sequencer basics

---

## ❓ Questions & Answers
### Task 1 : Introduction

**Q1:** From which primary tool or plartform do experienced AppSec proffesionals conduct most of their web application testing?
**A:** Burp Suite

### Task 2: What is Burp Suite?

**Q1:** Which edition of Burp Suite runs on a server and provides constant scanning for target web apps?  
**A:** Burp Suite Enterprise

**Q2:** Burp Suite is frequently used when attacking web applications and ______ applications.  
**A:** Mobile

**Q3:** What company made BurpSuite?  
**A:** Portswigger

**Q4:** If you want to learn more about application security from PortSwigger, what of their offerings would you use?  
**A:** Web Security Academy

---

### Task 3: Features of Burp Community

**Q1:** By default what IP address and port does the Burp Proxy make use of?  
**A:** 127.0.0.1:8080

**Q2:** What is the hotkey to send a request to the Repeater?  
**A:** CTRL + R

**Q3:** What is the hotkey to send a request to the Intruder?  
**A:** CTRL + I

**Q4:** What decoding scheme is pink?  
**A:** binary

**Extra Credit:** When testing for Race conditions you want to effectively send a number of requests at the same time, this is often done using a "Last-byte sync" attack. Where would you send this type of attack in Burpsuite? (Format: Component -> Button -> Option)  
**A:** Repeater -> Send -> Send Group in Parallel

---

### Task 4: Options

**Q1:** In which category can you find a reference to a "Cookie jar"?  
**A:** Sessions

**Q2:** In which base category can you find the "Updates" sub-category, which controls the Burp Suite update behaviour?  
**A:** Suite

**Q3:** If we have uploaded Client-Side TLS certificates, can we override these on a per-project basis (yea/nay)?  
**A:** yea

---

### Task 5: Burp Target and Proxy

**Q1:** Where can I see all requests proxied through Burp?  
**A:** HTTP History

**Q2:** What tool allows me to see all the endpoints in an application (that I know of)?  
**A:** Site Map

**Q3:** What functionality do I use to make Burp avoid intercepting or logging requests from a specific domain?  
**A:** Scope

**Q4:** Where can I find some Application Security vulnerability knowledge in Burp?  
**A:** Issues

**Q5:** Is it better to use the in-built browser or the Burp Browser?  
**A:** Personal Preference

---

### Task 6: The Intruder

**Q1:** What attack type cycles through the payloads inserting one payload at a time into each position defined in the request?  
**A:** Sniper

**Q2:** What attack type can be used to test for race conditions?  
**A:** Battering Ram

**Q3:** What is the maximum number of payload sets we can load into Intruder in Pitchfork mode?  
**A:** 20

**Q4:** We have three payload sets. The first set contains 100 lines, the second contains 2 lines, and the third contains 30 lines. How many requests will Intruder make using these payload sets in a Cluster bomb attack?  
**A:** 6000 (100 × 2 × 30)

**Q5:** Which Payload processing rule could we use to add characters at the end of each payload in the set?  
**A:** Add suffix

**Q6:** What symbol defines the start and the end of a payload position?  
**A:** `$` (dollar sign) – *Note: In modern Burp, it's often `§`, but your answer key says `$`*

---

### Task 7: Repeater

**Q1:** Which section gives us a more intuitive control over our requests?  
**A:** Inspector

**Q2:** Which section in Inspector is specific to POST requests?  
**A:** Body Parameters

**Q3:** Which option allows us to visualize the page as it would appear in a web browser?  
**A:** Render

**Q4:** Which view will populate when sending a request from the Proxy module to Repeater?  
**A:** Request

**Q5:** Did you know that you can double click the tab number in repeater to rename the tab and you can create groups for sorting requests?  
**A:** No answer needed

---

### Task 8: Decoder

**Q1:** Base64 encode the phrase: `Let's Start Simple`. What is the base64 encoded version?  
**A:** `TGV0J3MgU3RhcnQgU2ltcGxl` (you can verify, but use your actual answer)

**Q2:** URL Decode this data: `%4e%65%78%74%3a%20%44%65%63%6f%64%69%6e%67`. What is the plaintext?  
**A:** `Next: Decoding`

**Q3:** Decode this: `ZW5jb2RpbmcgaXMgdmVyeSBrZXdsCg==`  
**A:** `encoding is very key` (trailing newline)

**Q4:** What Linux tool allows you to perform base64 encoding and decoding?  
**A:** `base64` command

**Q5:** Encode this phrase: `Encoding Challenge`. Start with base64 encoding. Take the output and convert it into ASCII Hex. Finally, encode the hex string into octal. What is the final string?  
**A:** `24034214a720270024142d541357471232250253552c1162d1206c` (from your screenshot)

**Q6:** What characters used in base64 encoding are stripped in JWTs?  
**A:** `+`, `=`, `/`

---

### Task 9: The Comparer

**Q1:** What similar Linux utility exists?  
**A:** `diff` (common answer – fill in from your actual assignment if different)

---

### Task 10: The Sequencer

**Q1:** What does Sequencer allow us to evaluate?  
**A:** The randomness of tokens (e.g., session cookies, CSRF tokens)

---

## 🛠️ Key Takeaways
- Burp Suite is the industry standard for web app pentesting.
- **Proxy + Repeater** are the most frequently used tools for manual testing.
- **Intruder** is powerful but rate-limited in Community Edition.
- **Decoder** and **Comparer** are excellent for quick transformations and diffs.
- Always check **Scope** to avoid intercepting irrelevant traffic.

## 📚 Resources Used
- TryHackMe Burp Suite rooms
- PortSwigger Web Security Academy
- In-lab demonstrations


*End of Week 1*

