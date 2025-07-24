# TryHackMe – HTTP in Detail

## 🌐 Room Info
- Room: [HTTP in Detail](https://tryhackme.com/room/httpindetail)
- Username: siinon
- Difficulty: Easy

---

## 🧠 What I Learned
- Broke down how the **HTTP protocol** works and its role in web communication
- Learned about **HTTP request methods** like GET, POST, PUT, DELETE
- Explored **HTTP response status codes** (200 OK, 404 Not Found, 403 Forbidden, etc.)
- Saw how headers and cookies are used in client-server communication

---

## 🛠️ Tools / Skills Practiced
- `curl` to manually send HTTP requests
- Interpreting HTTP headers and response codes
- Understanding how login forms and web sessions work

---

## 🧾 Common HTTP Methods

| Method | Purpose                                |
|--------|----------------------------------------|
| GET    | Retrieve data (default in browsers)    |
| POST   | Submit data (used in forms)            |
| PUT    | Update/replace a resource              |
| DELETE | Remove a resource                      |

---

## 🔍 Commands to Remember
```bash
curl -I http://target               # Show only HTTP headers  
curl -X POST -d "user=admin" http://target/login  
