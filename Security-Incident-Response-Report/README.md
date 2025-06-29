
# 🛡️ Security Incident Response: Website Compromise & Remediation

## Project Overview

This project simulates the role of a cybersecurity analyst responding to a website compromise. I investigated a scenario where a client's cooking website — **yummyrecipesforme.com** — was compromised. Users began receiving strange prompts to download a file, were redirected to a malicious domain (**greatrecipesforme.com**), and noticed a slowdown in their systems.

My goal was to investigate the issue using network traffic logs (`tcpdump`), identify the attack method and protocols involved, document the full incident, and recommend a security control to help prevent this type of breach in the future.

---

## 🔍 Key Skills Practiced

- **Incident Response & Investigation**  
  Simulated real-world analysis of a compromised system based on user reports and network behavior.

- **Network Protocol Analysis**  
  Interpreted `tcpdump` logs to trace DNS requests, HTTP activity, and redirection behavior.

- **Vulnerability Assessment**  
  Identified key weaknesses: use of a default admin password and lack of brute-force prevention.

- **Malware Flow Tracking**  
  Tracked redirection and download behavior initiated by malicious JavaScript.

- **Technical Documentation**  
  Wrote a structured, factual security incident report based on collected evidence.

- **Security Strategy**  
  Recommended a preventative measure (Multi-Factor Authentication) to reduce risk from future brute force attacks.

---

## 🧪 How I Approached the Incident

### Initial Alert & Context

Reports came in from website visitors experiencing unwanted downloads, redirections, and system slowdowns. The site owner was locked out of the admin panel.

### Testing in a Safe Environment

I recreated the behavior in a sandbox and immediately saw a download prompt labeled as a browser update — a clear red flag.

### Network Log Analysis with `tcpdump`

- DNS request to `yummyrecipesforme.com`
- HTTP GET request for the main site
- File download triggered by JavaScript
- Follow-up DNS and HTTP traffic to `greatrecipesforme.com`

---

## 🧩 What I Discovered

- A successful brute force attack allowed a former employee to gain control of the site.
- Malicious JavaScript redirected users to a second website and prompted them to download malware.
- **Key protocols involved**: DNS, HTTP, and TCP.
- The attacker changed the admin password, locking out the legitimate site owner and maintaining control of the site.

---

## 🔐 Remediation Recommendation

I recommended implementing **Multi-Factor Authentication (MFA)** for all admin accounts.  
MFA greatly reduces the risk of brute force attacks by requiring a second form of verification — something the attacker is unlikely to have.

---

## 📄 What's in This Repository

- `Security Incident Report.pdf` — Full incident report with investigation timeline, analysis, and recommended actions.
- `README.md` — This overview of the project, approach, and learning objectives.
