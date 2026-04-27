# lab2-information-gathering-webgoat-attacks
Information gathering and web application security testing using DNS analysis, Nmap scanning, and WebGoat vulnerability exploitation (XSS, SQL Injection, CSRF, Buffer Overflow).

---

## Analyst Information

- **Name:** Denish Adhikari  
- **Role:** Cybersecurity Student | Junior Penetration Tester (Training Lab)  
- **Environment:** Kali Linux  
- **Tools Used:** Nmap, nslookup, WebGoat  

---

## Objectives

- Perform DNS reconnaissance and infrastructure analysis  
- Conduct network scanning and service enumeration  
- Understand attacker methodology in information gathering  
- Exploit common web application vulnerabilities  
- Analyze security weaknesses and their real-world impact  

---

## Tools & Technologies

- DNS Reconnaissance: nslookup  
- Network Scanning: Nmap  
- Web Application Testing: WebGoat (OWASP)  
- Environment: Kali Linux  

---

## Phase 1: Information Gathering (Reconnaissance)

### DNS Enumeration

Performed DNS queries on `google.com` to extract:

- A / AAAA records (IP addresses)  
- MX records (mail servers)  
- NS records (name servers)  
- TXT records (verification and metadata)  

### Security Insight

DNS information can expose:

- Mail servers → phishing/spam targeting  
- Infrastructure layout → attack surface mapping  
- Domain verification data → reconnaissance intelligence  

---

### Network Scanning

Performed scan on target: `129.120.210.235` using Nmap.

**Findings:**
- Open Port: 53 (DNS service)  
- Service identification successful  
- OS detection attempted  

### Security Insight

Nmap enables attackers to:

- Identify open ports and running services  
- Map network infrastructure  
- Identify potential entry points for exploitation  

---

## Phase 2: Web Application Exploitation

Using WebGoat (intentionally vulnerable application), multiple attacks were executed:

---

### 1. Cross-Site Scripting (XSS)

**Payload Used:**  
`<script>alert("XSS");</script>`

**Result:**
- Script executed successfully in browser  

**Impact:**
- Client-side code execution  
- Session hijacking potential  
- Credential theft risk  

---

### 2. SQL Injection

**Payload Used:**  
`1 OR 1=1--`

**Result:**
- Authentication bypass achieved  
- Unauthorized access to sensitive data  

**Impact:**
- Data exposure  
- Database compromise  
- Privilege escalation  

---

### 3. Cross-Site Request Forgery (CSRF)

**Method:**
- Crafted malicious request using hidden form  

**Result:**
- Unauthorized action executed on behalf of user  

**Impact:**
- Account manipulation  
- Unauthorized transactions  
- Session abuse  

---

### 4. Buffer Overflow

**Method:**
- Input of excessive data (6000+ characters)  

**Result:**
- Memory overflow behavior observed  

**Impact:**
- Application crash  
- Potential remote code execution  
- System instability  

---

## Attack Chain (Real-World Perspective)

This lab demonstrates how an attacker can progress through stages:

1. Perform reconnaissance using DNS tools (nslookup)  
2. Identify open services using Nmap  
3. Target exposed web applications  
4. Exploit vulnerabilities (XSS, SQL Injection, CSRF)  
5. Gain unauthorized access to systems or data  
6. Potentially escalate privileges or maintain persistence  

---

## Recommended Mitigations

### Input Validation & Application Security
- Implement strict input validation and sanitization  
- Use parameterized queries to prevent SQL Injection  
- Encode output to mitigate XSS  

---

### Authentication & Session Security
- Implement CSRF tokens  
- Enforce secure session handling  
- Use multi-factor authentication where possible  

---

### Network Security
- Restrict unnecessary open ports  
- Use firewalls to limit exposure  
- Monitor network activity  

---

### Secure Development Practices
- Follow OWASP Top 10 guidelines  
- Perform regular security testing  
- Conduct code reviews and vulnerability scans  

---

## Screenshots

### DNS Reconnaissance
![DNS](dns.png)

### Nmap Scan
![Nmap](nmap.png)

### XSS Attack
![XSS](xss.png)

### SQL Injection
![SQL](sql.png)

### CSRF Attack
![CSRF](csrf.png)

### Buffer Overflow
![BOF](buffer.png)

---

## Security Outcome

This lab demonstrates:

- How attackers gather intelligence before exploitation  
- How insecure input handling leads to critical vulnerabilities  
- How multiple vulnerabilities can be chained into full compromise  

---

## Key Learnings

- Understood reconnaissance techniques using DNS and network scanning  
- Learned exploitation of OWASP Top 10 vulnerabilities  
- Gained insight into attacker methodology and attack chains  
- Recognized importance of secure coding and input validation  
- Developed foundational penetration testing skills  

---

## Skills Demonstrated

- DNS Enumeration & Reconnaissance  
- Network Scanning (Nmap)  
- Web Application Penetration Testing  
- Vulnerability Exploitation (XSS, SQL Injection, CSRF)  
- Basic Exploit Development Concepts (Buffer Overflow)  
- Security Analysis & Threat Modeling  

---

## Conclusion

This project demonstrates a full attack lifecycle—from reconnaissance to exploitation—highlighting how insecure configurations and poor input validation can lead to system compromise.

It reflects practical skills required in:
- Penetration Testing  
- Web Application Security  
- Security Operations (SOC Analysis)  

---

## Author

**Denish Adhikari**  
Cybersecurity Student | Aspiring Security Analyst  
