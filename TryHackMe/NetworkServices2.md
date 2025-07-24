# TryHackMe – Network Services 2

## 🌐 Room Info
- Room: [Network Services 2](https://tryhackme.com/room/networkservices2)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Built on previous service enumeration knowledge with more complex services like **SMTP** and **MySQL**
- Practiced identifying and exploiting misconfigured databases and mail servers
- Learned how to connect to services manually to test for open authentication or leaked data

---

## 🛠️ Tools / Skills Practiced
- `telnet` and `nc` (netcat) to connect to SMTP manually
- `mysql -u` to access open database servers
- Banner grabbing and manual enumeration techniques

---

## ⚙️ Useful Commands

```bash
telnet target-ip 25                     # connect to SMTP
nc -nv target-ip 3306                   # check MySQL service
mysql -h target-ip -u root -p           # attempt MySQL login
