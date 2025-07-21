# rlogin Vulnerability - Port 513

## 🔍 Overview
`rlogin` (Remote Login) is a legacy service that allows users to log in to another host over the network. It is known for poor authentication mechanisms, especially when `.rhosts` files are misconfigured to allow passwordless access.

In this assessment, we exploited an `rlogin` vulnerability on **Metasploitable2** using **OpenVAS** and manual login attempts.

---

## 🎯 Target Information
- **Target IP**: `10.36.13.230`
- **Service**: rlogin
- **Port**: `513/tcp`
- **Vulnerability**: Passwordless root login due to misconfigured `.rhosts`

---

## 🧪 Exploitation Steps

1. **OpenVAS Scan Findings**:
   - Identified `rlogin` service running on port `513`
   - Marked as a high-risk vulnerability due to passwordless login

2. **Manual Exploitation**:
   - Command:  
     ```bash
     rlogin 10.36.13.230 -l root
     ```
   - Result: Logged in **without needing a password**
   - System: Metasploitable2 (Ubuntu 8.04 Server)

3. **Post Login Access**:
   - Verified root privileges
   - Able to read sensitive files (e.g., `/etc/passwd`, `/etc/shadow`)
   - Demonstrated total system compromise

---

## ⚠️ Security Risk

- Unauthenticated remote access as **root**
- Full privilege escalation
- Total system compromise

---

## 🛡️ Mitigation

- Disable `rlogin` service permanently
- Remove all `.rhosts` files from user home directories
- Use secure alternatives like SSH with key-based authentication

---

## 📸 Evidence

> *(Include screenshot or terminal log here if possible)*

---

## 📚 References
- [CERT Advisory CA-1996-21](https://www.cisa.gov/news-events/alerts/1996/10/16/rlogin-and-rsh-are-insecure)
- [OpenVAS CVE report if applicable]
