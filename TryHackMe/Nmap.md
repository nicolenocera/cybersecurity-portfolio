# TryHackMe – Nmap

## 🔍 Room Info
- Room: [Nmap](https://tryhackme.com/room/nmap)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Learned how to use **Nmap**, the most common tool for network discovery and port scanning
- Explored the differences between scanning types: SYN (`-sS`), full connect (`-sT`), UDP (`-sU`)
- Practiced identifying open ports, services, versions, and even OS detection

---

## 🛠️ Tools / Skills Practiced
- Using `nmap` with different flags for stealth, speed, and verbosity
- Interpreting scan results to find running services
- Basic enumeration of targets before exploitation

---

## ⚙️ Common Nmap Commands

```bash
nmap -sS target-ip              # SYN scan (stealthy)
nmap -sV target-ip              # Version detection
nmap -O target-ip               # OS detection
nmap -p- target-ip              # Scan all 65535 ports
nmap -A target-ip               # Aggressive scan (OS, scripts, traceroute)
