# TryHackMe – Network Services 1

## 🌐 Room Info
- Room: [Network Services 1](https://tryhackme.com/room/networkservices)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Explored how common network services (like FTP and SSH) can be discovered and exploited
- Learned how to identify open ports using Nmap and service enumeration
- Practiced connecting to FTP servers and SSH services to look for misconfigurations or anonymous access
- Gained awareness of weak credentials and default service setups

---

## 🛠️ Tools / Skills Practiced
- `nmap` for port scanning and version detection
- `ftp` and `ssh` for manual service access
- Reading service banners to identify software and versions

---

## 🔍 Commands to Remember
```bash
nmap -sV -p- target-ip             # full port scan with version detection
nmap -A target-ip                  # aggressive scan with OS detection
ftp target-ip                      # connect to FTP manually
ssh user@target-ip                 # try SSH login
