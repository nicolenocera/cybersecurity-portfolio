# TryHackMe – Vulnversity

## 💻 Room Info
- Room: [Vulnversity](https://tryhackme.com/room/vulnversity)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Walked through a full **CTF-style vulnerability assessment**
- Used **Nmap** to discover open ports and services
- Identified an **upload vulnerability** in a web application and exploited it to gain a foothold
- Gained basic **reverse shell access**, did **local enumeration**, and retrieved a flag

---

## 🛠️ Tools / Skills Practiced
- `nmap` for service detection
- Directory brute-forcing with `gobuster`
- Manual file upload abuse
- Reverse shell via `bash`, `nc`, or `python`
- Basic Linux post-exploitation enumeration

---

## ⚙️ Tools & Commands Used

```bash
nmap -sV -p- target-ip
gobuster dir -u http://target-ip -w /usr/share/wordlists/dirb/common.txt
nc -lvnp 4444
python3 -c 'import pty; pty.spawn("/bin/bash")'
