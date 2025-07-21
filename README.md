# 🔒 Vulnerability Assessment Lab – Hands-on with OpenVAS, Metasploit & Metasploitable2

"Hands-on Vulnerability Assessment and Exploitation Lab using OpenVAS, Metasploit, and Metasploitable2. Ethical hacking practice and exploitation notes."

---

## 📚 Table of Contents
- [Tools Used](#tools-used)
- [Objectives](#objectives)
- [Explored Vulnerabilities](#explored-vulnerabilities)
- [Next Targets](#next-targets)
- [References](#references)

---

## 🛠️ Tools Used

- **OpenVAS** (Greenbone Vulnerability Manager)
- **Metasploit Framework**
- **Metasploitable2 VM**
- **Nmap**, `netcat`, and other terminal tools

---

## 🎯 Objectives

- Identify vulnerable ports and services using OpenVAS
- Exploit legacy protocols like `rlogin`, `rexec`, and `ingreslock`
- Learn vulnerability report writing
- Improve practical ethical hacking & cybersecurity skills

---

## 🧪 Explored Vulnerabilities

### 1. `rlogin` (Port 513)
- **Type**: Remote Login Service
- **Issue**: Passwordless `root` login allowed
- **Impact**: Full shell access as root
- **Status**: ✅ Successfully exploited

### 2. `rexec` (Port 512)
- **Type**: Remote Execution Protocol
- **Issue**: Remote command execution without strong authentication
- **Tool Used**: OpenVAS & Metasploit (`rexec_login` scanner)
- **Status**: ⚠️ Exploitation attempted, further testing needed

### 3. `ingreslock` (Port 1524)
- **Type**: Backdoor (root shell)
- **Issue**: Grants direct root shell without credentials
- **Command Used**: `nc <target-ip> 1524`
- **Status**: ✅ Exploited successfully (root access confirmed)

---

## 🚀 Next Targets (Coming Soon)

- Apache Tomcat (Port 8009) - Investigating AJP vulnerability
- FTP Anonymous Login - Test default misconfigurations
- Samba Shares - Check for `null` session or write access
- Telnet Access - Legacy protocol scan

---

## 📚 References

- [OpenVAS Documentation](https://greenbone.net/documentation/)
- [Metasploit Modules Reference](https://docs.rapid7.com/metasploit/)
- [Metasploitable2 Info](https://docs.rapid7.com/metasploit/metasploitable-2/)
- `man` pages: `nc`, `nmap`, `whois`, `netstat`

---

> 🧠 _Note_: All activities were performed in an isolated virtual lab for ethical research and learning purposes only.
