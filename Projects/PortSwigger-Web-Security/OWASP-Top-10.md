# OWASP Top 10 (2025)

The OWASP Top 10 is a list of the biggest web application security risks. It doesn't cover every vulnerability, but it highlights the ones that are most common and important to know.

## Why it matters

- Gives me a good starting point for learning web security.
- Helps me know what to look for when testing websites.
- These topics come up often in cybersecurity jobs and interviews.
- Many PortSwigger labs are based on these vulnerabilities.

## A01 - Broken Access Control

Users can access things they shouldn't.

Example: A user changes a URL and is able to see another user's account.

How to prevent: Check user permissions on the server, give users only the access they need, don't trust user input.

## A02 - Security Misconfiguration

The application isn't set up securely.

Examples: Default passwords, open admin pages, debug mode left on.

How to prevent: Remove anything you don't need, keep software updated, use secure settings.

## A03 - Software Supply Chain Failures

Problems caused by software or libraries the application depends on.

Examples: Using outdated packages or installing vulnerable third-party software.

How to prevent: Keep dependencies updated, only use trusted software, watch for security updates.

## A04 - Cryptographic Failures

Sensitive information isn't protected properly.

Examples: Weak passwords, passwords stored in plain text, or weak encryption.

How to prevent: Use strong encryption, hash passwords, always use HTTPS.

## A05 - Injection

Attackers get the application to run commands it wasn't supposed to.

Examples: SQL Injection, NoSQL Injection, and OS Command Injection.

How to prevent: Validate user input, use parameterized queries, and don't build commands directly from user input.

## A06 - Insecure Design

The application was designed in a way that makes security problems easier to exploit.

## A07 - Authentication Failures

Problems with logins, passwords, or user sessions.

Example: Weak passwords,, sessions that never expire.

How to prevent: Strong password policies, MFA, secure session handling, and rate limiting.

## A08 - Software or Data Integrity Failures

The application trusts software, updates, or data that it shouldn't.

Example: Installing an update from untrusted source.

How to prevent: Verify updates, use trusted sources, check software integrity.

## A09 - Security Logging and Alerting Failures

Attacks happen but no one notices because they aren't logged or monitored.

Example: Multiple failed login attempts aren't recorded.

How to prevent: Log important security events and monitor them for suspicious activity.

## A10 - Mishandling Exceptional Conditions

The application doesn't safely handle unexpected errors or situations.

Example: An error message reveals sensitive system information.

How to prevent: Handle errors safely, don't expose sensitive information, and test how the application reacts to unexpected situations.
