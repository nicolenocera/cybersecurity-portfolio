Room: Windows Fundamentals 2
Username: siinon
Difficulty: Easy

This room focused a lot more on understanding user accounts and how access is handled in Windows. I started learning how accounts are stored and managed, especially the difference between local and domain accounts. I also learned how passwords are stored and that hashes are used instead of saving them as plain text.

One of the tools I used was net user, which let me look at account info and user properties. I also got more familiar with the net localgroup command and how it shows which users are in which groups. This helped me understand how attackers might try to escalate privileges if they get into a system.

Another topic that came up was running tasks and monitoring processes. I used tasklist to see what's running on the machine, and it showed how much info you can get just from the command line without needing Task Manager. I also tried out taskkill to shut down a process by its PID.

arduino
Copy
Edit
net user
net localgroup
tasklist
taskkill /PID [process ID] /F
This room made me more comfortable with how user accounts are structured in Windows, and it gave me a better idea of how attackers might take advantage of misconfigured permissions or leftover accounts. I'm going to remember this stuff as I move further into blue team topics.
