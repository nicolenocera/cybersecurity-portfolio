# Username Enumeration via Different Responses

## Objective

Use Burp Suite Intruder to find a valid username by comparing the server's responses, then find the correct password and complete the lab.

---

## Tools Used

- Burp Suite Community Edition
- Burp Intruder
- PortSwigger Web Security Academy

---

## Step 1 - Capture the Login Request

I opened the lab in Burp's browser and tried logging in with random credentials.

The login request appeared in HTTP History, so I sent it to Intruder.

I was still learning Burp at this point, so I spent some time looking through the request before moving on.

![Burp HTTP History](screenshots/01-burp-http-history-test.png)

![HTTP History](screenshots/02-http-history.png)

![Login Request](screenshots/03-request.png)

![Send to Intruder](screenshots/04-send-to-intruder.png)

---

## Step 2 - Troubleshooting

My first Intruder attack didn't work.

I checked the proxy settings, Task Log, and Site Map to figure out what was wrong.

After some troubleshooting, I realized I needed to capture a new login request from the current lab session. Once I did that, everything worked correctly.

This ended up helping me understand Burp Suite a lot better.

![Proxy Settings](screenshots/05-troubleshooting-proxy-settings.png)

![Task Log](screenshots/06-task-log.png)

![Site Map](screenshots/07-site-map-troubleshooting.png)

![Site Map Filter](screenshots/08-site-map-filter.png)

![Expired Session Errors](screenshots/09-expired-session-errors.png)

---

## Step 3 - Find the Username

I configured Intruder to test the usernames provided by the lab.

Instead of looking for a successful login, I compared the response lengths.

One username had a different response length than the rest.

The valid username was:

alterwind

![Payload Configuration](screenshots/15-payload-configuration.png)

![Username List](screenshots/16-authlab-lab-usernames.png)

![Username Results](screenshots/10-username-enumeration-results.png)

![Valid Username](screenshots/11-valid-username-found.png)

---

## Step 4 - Find the Password

After finding the username, I changed the payload position to the password field.

I loaded the password list and ran another Intruder attack.

This time I looked for a different status code. One response returned 302 instead of 200, showing the correct password.

The valid password was:

abc123

![Password Configuration](screenshots/12-password-attack-configured.png)

![Valid Password](screenshots/13-valid-password-found.png)

---

## Step 5 - Complete the Lab

I logged in with the username and password I found and completed the lab.

![Lab Solved](screenshots/14-lab-solved.png)

---

## What I Learned

- How to capture requests in Burp Suite
- How to send requests to Intruder
- How to configure payload positions
- How response lengths can identify a valid username
- How different status codes can identify a successful login
- Why it's important to capture a new request if a lab session changes
