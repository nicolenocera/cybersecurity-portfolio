# TryHackMe – Hydra

## 🔓 Room Info
- Room: [Hydra](https://tryhackme.com/room/hydra)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Explored **Hydra**, a powerful tool for brute-force attacks against login services
- Learned how to target protocols like SSH, FTP, HTTP, and more using custom wordlists
- Practiced launching dictionary attacks to guess usernames and passwords

---

## 🛠️ Tools / Skills Practiced
- Using `hydra` on the command line to brute-force login pages
- Reading error messages and HTTP responses to detect login success
- Understanding timing, rate-limiting, and stealth considerations in brute-force attacks

---

## ⚙️ Common Hydra Command Examples

```bash
hydra -l admin -P rockyou.txt ftp://<target-ip>        # FTP brute-force
hydra -l root -P rockyou.txt ssh://<target-ip>         # SSH brute-force
hydra -L users.txt -P passwords.txt http-post-form "/login:username=^USER^&password=^PASS^:F=Invalid" -t 4
