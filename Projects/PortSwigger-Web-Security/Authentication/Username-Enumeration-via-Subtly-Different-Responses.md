# Username Enumeration via Subtly Different Responses

## Objective

Find a valid username by comparing login responses, then use it to identify the correct password and solve the lab.

---

## Tools Used

- Burp Suite Community Edition
- Burp Intruder
- PortSwigger Web Security Academy

---

## Steps Taken

1. Captured the `POST /login` request in Burp Suite.
2. Sent the request to Intruder.
3. Used a Sniper attack with the username as the payload.
4. Loaded the candidate usernames wordlist.
5. Sorted the results by response length, but nothing stood out.
6. Used Grep Match and Grep Extract to compare the error messages.
7. Found that the username **anaheim** returned:

   ```
   Invalid username or password
   ```

   while every other username returned:

   ```
   Invalid username or password.
   ```

8. Fixed the username as **anaheim** and moved the payload to the password field.
9. Loaded the candidate passwords wordlist and ran a second attack.
10. Found that **robert** returned a **302** status code.
11. Logged in with:

   Username: anaheim

   Password: robert

12. Solved the lab.

---

## What I Learned

- Small response differences can reveal valid usernames.
- Grep Extract makes subtle response differences easier to spot.
- A 302 response can indicate a successful login.
- Burp Intruder makes username and password enumeration much faster.

---

## Screenshots

### Grep Match

![Grep Match](screenshots/17-grep-match.png)

Configured Grep Match while comparing responses.

---

### Grep Extract

![Grep Extract](screenshots/18-grep-extract.png)

Configured Grep Extract to compare the login error messages.

---

### Valid Username

![Username Found](screenshots/19-username-found.png)

Found the valid username **anaheim** after noticing the missing period in the response.

---

### Password Attack

![Password Search](screenshots/20-password-search.png)

Configured the password attack using the valid username.

---

### Valid Password

![Password Found](screenshots/21-password-found.png)

The password **robert** returned a **302** response.

---

### Lab Complete

![Lab Completed](screenshots/22-lab-completed.png)

Successfully logged in and solved the lab.
