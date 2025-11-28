Room: Windows Fundamentals 3  
Username: siinon  
Difficulty: Easy  

This room was all about the Windows Registry, services, and startup behavior. At first it felt kind of overwhelming, but once I got into it, it started making more sense.

I learned that the registry is basically a huge database that controls how Windows behaves. Editing it directly can mess up your system if you’re not careful, but it’s also a place attackers might hide persistence methods. I used `regedit` to open the registry and looked through some of the keys that get used during startup.

I also explored how services work. Some are essential for the OS, but others are installed by third-party programs and can be abused. The `services.msc` tool helped me see which ones were running, their startup types, and whether they were manual or automatic.

Then I learned about different places programs can set themselves up to launch automatically, not just the Startup folder, but also certain registry keys.

```
regedit                 // open registry editor  
msconfig                // manage startup settings  
services.msc            // view and manage services  
```

I didn’t expect to like this room, but it actually helped me understand how Windows boots and how both admins and attackers can manipulate startup behavior. Definitely gave me some things to watch out for.

