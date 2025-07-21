# 🔍 Vulnerability Assessment Lab

**Hands-on Vulnerability Assessment using OpenVAS, Metasploit, and Metasploitable2**

This lab documents real exploitation of legacy services using ethical hacking techniques.

---

## 📚 Table of Contents
- [Overview](#overview)
- [Objectives](#objectives)
- [Tools Used](#tools-used)
- [Explored Vulnerabilities](#explored-vulnerabilities)
- [Screenshots](#screenshots)
- [How to Reproduce](#how-to-reproduce)
- [Resources](#resources)

---

## 🧠 Overview
This repository is a personal learning project where I explore vulnerable services on Metasploitable2 using OpenVAS and Metasploit.

---

## 🎯 Objectives
- Identify open ports and weak services
- Exploit insecure protocols (`rlogin`, `rexec`, `ingreslock`)
- Document security findings and exploit steps
- Practice ethical hacking techniques

---

## 🛠️ Tools Used
- OpenVAS / GVM (for scanning vulnerabilities)
- Metasploit Framework (for exploitation)
- Nmap (for service enumeration)
- VirtualBox (for hosting VMs)
- Kali Linux (attacker machine)
- Metasploitable2 (target machine)

---

## 💥 Explored Vulnerabilities

### 1. `rlogin` (Port 513)
- Weak authentication
- Gained root access without password (trust-based access)

### 2. `rexec` (Port 512)
- Remote command execution
- Discovered via OpenVAS, tested using Metasploit

### 3. `ingreslock` (Port 1524)
- Backdoor shell from old `inetd` configuration
- Investigated for post-exploitation

---

## 🖼️ Screenshots
(Coming Soon)

---

## 🧪 How to Reproduce
1. Set up Kali Linux and Metasploitable2 in VirtualBox
2. Ensure both VMs are on Host-Only or Bridged network
3. Run `nmap -sV <target-ip>` to find open services
4. Scan with OpenVAS
5. Exploit vulnerabilities using Metasploit

---

## 📘 Resources
- [OpenVAS Docs](https://greenbone.github.io/)
- [Metasploit Unleashed](https://www.offensive-security.com/metasploit-unleashed/)
- [Metasploitable2 Download](https://sourceforge.net/projects/metasploitable/)
- [Nmap Guide](https://nmap.org/book/)

---

> ⚠️ For educational purposes only. Always hack in legal environments.
