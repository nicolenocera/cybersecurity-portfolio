Room: DNS in Detail  
    Username: siinon  
    Difficulty: Easy  

This room helped me understand how the Domain Name System (DNS) works behind the scenes. I got familiar with the role of DNS in translating domain names into IP addresses, which is what lets users access websites with easy-to-remember names instead of numeric IPs.

I worked with tools like `nslookup` and `dig` to explore DNS records. I learned how to look up different types of records, like A, AAAA, MX, NS, and TXT. One important thing I picked up was how DNS requests and responses can reveal a lot about how a network is structured.

I also learned about common attacks related to DNS, like DNS poisoning and spoofing, and how misconfigurations can lead to information leakage. The zone transfer lab showed me that if a server allows AXFR (zone transfer) requests from any IP, it can expose internal domain data — something that shouldn’t be publicly accessible.

Overall, this room gave me a better grasp on how DNS fits into both networking and security. It’s something I’ll pay more attention to when scanning or setting up a network.
