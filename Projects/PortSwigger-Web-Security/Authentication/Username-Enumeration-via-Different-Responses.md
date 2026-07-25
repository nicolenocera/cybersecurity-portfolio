# Username Enumeration via Different Responses

## Objective

The goal of this lab was to identify a valid username by comparing small differences in the server's responses. Once I found the valid username, I used Burp Suite Intruder again to identify the correct password and complete the lab.

---

## Tools Used

- Burp Suite Community Edition
- Burp Intruder
- PortSwigger Web Security Academy

---

## Step 1 - Capturing the Login Request

I opened the PortSwigger lab in Burp's browser and submitted a login request using random credentials.

The request appeared in HTTP History, where I could inspect it before sending it to Intruder.

At this point, I was mostly trying to get comfortable navigating Burp Suite and understanding how requests moved through the application.

![Burp HTTP History](screenshots/01-burp-http-history-test.png)

![HTTP History](screenshots/02-http-history.png)

![Captured Login Request](screenshots/03-request.png)

![Send to Intruder](screenshots/04-send-to-intruder.png)

---

## Step 2 - Troubleshooting

The first time I launched the Intruder attack, every request returned an error.

Instead of immediately starting over, I spent some time figuring out why.

I checked Burp's proxy settings, looked through the Task Log, and explored the Site Map. This helped me confirm that Burp was capturing traffic correctly, but the request and attack settings were not lined up properly.

I also learned that I needed to capture a fresh request after the lab session changed. Once I corrected the setup and used the current request, the attack worked normally.

Although it was frustrating at first, troubleshooting the problem helped me understand Burp Suite much better.

![Proxy Settings](screenshots/05-troubleshooting-proxy-settings.png)

![Task Log](screenshots/06-task-log.png)

![Site Map Troubleshooting](screenshots/07-site-map-troubleshooting.png)

![Site Map Filter](screenshots/08-site-map-filter.png)

![Expired Session Errors](screenshots/09-expired-session-errors.png)

---

## Step 3 - Username Enumeration

After fixing the setup, I configured Intruder to test the usernames provided by the lab.

I placed the payload marker around the username value and loaded the supplied username list.

Instead of looking for a successful login, I compared the response lengths returned for each username. Most of the responses had the same length, but one was slightly different.

The valid username was:

**alterwind**

![Payload Configuration](screenshots/15-payload-configuration.png)

![Lab Username List](screenshots/16-authlab-usernames.png)

![Username Enumeration Results](screenshots/10-username-enumeration-results.png)

![Valid Username Found](screenshots/11-valid-username-found.png)

---

## Step 4 - Password Attack

Once I had the correct username, I entered **alterwind** as a fixed value and moved the Intruder payload position to the password field.

I loaded the supplied password list and launched another attack.

This time, I looked for a response that was different from the others. One password returned a **302** status instead of **200**, indicating that the login was successful.

The valid password was:

**abc123**

![Password Attack Configuration](screenshots/12-password-attack-configuration.png)

![Valid Password Found](screenshots/13-valid-password-found.png)

---

## Step 5 - Lab Completed

Using the discovered username and password, I successfully logged into the account and completed the PortSwigger lab.

![Lab Solved](screenshots/14-lab-solved.png)

---

## What I Learned

- How to capture and inspect login requests using Burp Suite.
- How to send a request to Burp Intruder.
- How to configure payload positions.
- How response lengths can reveal a valid username.
- How a different HTTP status code can indicate a successful login.
- How to troubleshoot Burp when an attack does not behave as expected.
- Why it is important to use a fresh request from the current lab session.
