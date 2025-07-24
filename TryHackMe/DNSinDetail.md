# TryHackMe – DNS in Detail

## 🌐 Room Info
- Room: [DNS in Detail](https://tryhackme.com/room/dnsindetail)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Understood the purpose and function of the **Domain Name System (DNS)**
- Learned how DNS translates human-friendly domains to IP addresses
- Explored different **DNS record types** like A, AAAA, CNAME, MX, and TXT
- Practiced DNS enumeration techniques using **nslookup** and **dig**

---

## 🛠️ Tools / Skills Practiced
- Using `nslookup` to query DNS records
- Learning how **dig** works for detailed DNS lookups
- Identifying **zone transfer vulnerabilities**
- Recognizing suspicious or misconfigured DNS entries

---

## 🧾 Common DNS Record Types

| Record | Purpose                              | Example                       |
|--------|--------------------------------------|-------------------------------|
| A      | Maps domain to IPv4 address          | `example.com → 192.168.1.1`   |
| AAAA   | Maps domain to IPv6 address          | `example.com → ::1`           |
| CNAME  | Alias of another domain              | `www → example.com`           |
| MX     | Mail exchange server info            | `mail → mail.example.com`     |
| TXT    | Arbitrary text, often for SPF/DMARC  | `"v=spf1 include:_spf.google.com"` |

---

## 🧪 Commands to Remember

```bash
nslookup example.com
dig example.com any
dig @nameserver example.com axfr  # Zone transfer attempt
