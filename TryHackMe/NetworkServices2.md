Room: Network Services 2  
    Username: siinon  
    Difficulty: Easy  

This room continued where the first one left off by diving into more services like SMB, HTTP, and NFS. I learned how these services work and how they can be misconfigured in ways that make them vulnerable to attacks.

I practiced using tools like `smbclient`, `enum4linux`, and `showmount` to gather information. With SMB, I learned how file shares can leak sensitive data if access controls aren’t set properly. NFS was similar — if a directory is exported without restrictions, anyone on the network might be able to mount it and see what's inside.

There was also some light web enumeration using `curl` and `dirb`, which helped me start thinking about how HTTP services can reveal information even without a visible website.

This room made me realize how common it is to find these services on networks and how important it is to test them for default settings or loose permissions.
