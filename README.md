# eCPPTv3-Review

![eCPPTv3-1](https://github.com/user-attachments/assets/b53e3ede-8b8a-4f21-a91e-8284f5e917bd)


**Review on eCPPTv3: My Path to Becoming a Certified Professional Penetration Tester**

On March 26th, I achieved the **eLearnSecurity Certified Professional Penetration Tester (eCPPTv3)** certification, a milestone in my cybersecurity journey. This certification process was both challenging and insightful, with a strong focus on **Active Directory (AD) exploitation**. While the experience did not fully align with my initial expectations, it provided valuable lessons and opportunities for growth.

In this post, I’ll share my thoughts on the exam, its strengths and weaknesses, my preparation strategy, and key takeaways from my first attempt.

---
## **Exam Experience: Strengths and Weaknesses**

### **What Stood Out**
- **Minimal Public Information:** With limited details available online, the exam remained an authentic and engaging challenge.
- **Multiple Exploitation Paths:** Many machines offered different approaches to achieving the objective, encouraging strategic thinking.
- **Active Directory Integration:** The inclusion of **Active Directory attacks** made the exam more relevant to real-world penetration testing scenarios.

### **Areas for Improvement**
- **Lack of Reporting Requirement:** Unlike other penetration testing certifications, this exam did not include a **final report**, missing an essential aspect of real-world engagements.
- **Absence of Pivoting:** The exclusion of **network pivoting** was unexpected, as it is a crucial skill for professional penetration testers.
- **Excessive Brute Forcing:** The reliance on **brute-force attacks** felt unrealistic compared to actual penetration testing environments.
- **Ambiguous Questions:** Some questions were unclear, including one referencing a non-existent user, which created unnecessary confusion.
- **Insufficient AD Training in the INE Course:** The **INE training** provided for the exam did not adequately cover **Active Directory exploitation**, which required me to seek additional resources from **Hack The Box (HTB) and TryHackMe (THM)**.

---
## **Exam Format and Requirements**

The **eCPPTv3 exam** consists of **45 questions** to be completed within **24 hours**. Candidates must assess a network environment that includes:
- **A Linux host**
- **Multiple Windows hosts, including domain controllers (DCs)**
- **A web-based attacking machine**

The exam follows a **Letter of Engagement**, outlining the scope and objectives of the penetration test. To succeed, candidates should have prior knowledge of:
- **Web application security**
- **Linux exploitation**
- **Active Directory attacks**
- **A widely used CMS**

---
## **Recommended Wordlists for Brute-Force Attacks**

Given the role of brute-forcing in the exam, I found the provided wordlists ineffective. Instead, I suggest using:

- `common_corporate_passwords.lst`
- `seasons.txt`
- `months.txt`
- `xato-net-10-million-passwords-1000.txt`
- `xato-net-10-million-passwords-10000.txt`
- `rockyou.txt`

---
## **Essential Tools for the Exam**

### **Active Directory Enumeration & Attacks**
- `kerbrute`, `crackmapexec`, `evil-winrm` 
- `xfreerdp`, `bloodhound-python`, `smbclient`, `rpcclient`

### **Windows Built-in & Enumeration Tools**
- `Enter-PSSession`, `net`
- `powerview.ps1`, `winpeas.exe`

### **Metasploit Framework**
- `msfvenom`, `msfconsole`
- `post/multi/recon/local_exploit_suggester`
- `exploit/multi/handler` (payload: `windows/meterpreter/reverse_tcp`)

### **Meterpreter & Impacket**
- `kiwi`, `hashdump`, `creds_all`
- `GetNPUsers.py`, `psexec.py`, `wmiexec.py`

### **Additional Tools**
- `wpscan`, `hydra`, `hashcat`, `john`
- `nmap` (with scripts), `GTFObins`

---
## **Study Strategy & Recommended Resources**

Since the **INE course did not provide sufficient depth for Active Directory exploitation**, I relied on **Hack The Box (HTB) and TryHackMe (THM)** to fill the gaps. Below are the resources that helped me the most:

### **HTB Academy Courses:**
- [Introduction to Active Directory](https://academy.hackthebox.com/course/preview/introduction-to-active-directory)
- [Active Directory Enumeration & Attacks](https://academy.hackthebox.com/course/preview/active-directory-enumeration--attacks)
- [Hacking WordPress](https://academy.hackthebox.com/course/preview/hacking-wordpress)

### **HTB Labs:**
- Completed **all easy machines** in the **Active Directory 101 track**

### **TryHackMe (THM):**
- [Attacking Kerberos](https://tryhackme.com/room/attackingkerberos)
- [Breaching Active Directory](https://tryhackme.com/room/breachingad)
- [Exploiting Active Directory](https://tryhackme.com/room/exploitingad)
- [Linux Privilege Escalation](https://tryhackme.com/room/linprivesc)
- [Windows Privilege Escalation](https://tryhackme.com/room/windowsprivesc20)
---
## **Key Exam Strategies and Lessons Learned**

- **Meticulous Note-Taking:** Document every **command, credential, and vulnerability** systematically. Since machines are interconnected, well-organized notes are essential.
- **Step-by-Step Approach:** Avoid moving on to another machine before fully exploring the previous one, as this can lead to confusion.
- **Command Re-Execution After Lab Resets:** If you reset the lab, ensure that you **rerun all previously executed commands**, as failure to do so may result in incorrect scoring for related questions.
- **xfreerdp Connection Issues:** I faced difficulties using `xfreerdp`. The format that worked for me was:
  ```bash
  xfreerdp /u:username /p:password /v:ip_address
  ```

---
## **Final Verdict: Is eCPPTv3 Worth It?**

For those considering the eCPPTv3 certification, here’s my assessment:

- **Ideal for students or aspiring penetration testers** who cannot afford **OSCP** but want to demonstrate their **Active Directory expertise**.
- **A solid certification** for those seeking a challenge that is **less CTF-like** and closer to real-world scenarios.
- **Needs improvements**, particularly in the inclusion of **pivoting and reporting**, to enhance its industry relevance.
- **INE’s training does not fully cover AD exploitation**, so additional self-study is required.

Would I recommend it? **Yes, with the right expectations.** If you plan to take the eCPPTv3, focus on **Active Directory exploitation, enumeration techniques, and structured note-taking**.

---

