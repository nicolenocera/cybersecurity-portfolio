### Meow

For Meow, I started by running a quick scan and saw that telnet was open. Since telnet doesn’t use authentication by default, I was able to connect straight into the machine without any resistance. Once I was in, I moved around the file system, checked a few directories, and found the flag sitting in the root folder. This box showed how risky it is to leave old services like telnet exposed, because anyone can connect and access whatever is on the system.
