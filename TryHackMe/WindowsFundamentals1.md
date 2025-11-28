Room: Windows Fundamentals 1  
Username: siinon  
Difficulty: Easy  

I started getting comfortable with how Windows works behind the scenes. Most of this room was about understanding the NTFS file system and navigating the OS through both the graphical interface and the command line. I used the TryHackMe Windows virtual machine for all of this.

I learned about UAC (User Account Control) and how it plays a role in limiting access unless you're running something as admin. It was also a good intro to permissions, how Windows handles access to files and folders depending on the user level.

I used File Explorer to poke around and get more familiar with common folders and structure. But what really helped was the command prompt. A few commands I used throughout:

```
whoami       // shows current user  
ipconfig     // shows IP info  
dir          // lists directory contents  
cd ..        // move up one directory  
```

This room helped me get more confident with navigating a Windows environment without just relying on the UI. It also emphasized how important patching and updates are from a security standpoint, which I’ll keep in mind as I go further into blue team stuff.
