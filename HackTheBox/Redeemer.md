### Redeemer

For Redeemer, I scanned the machine and noticed that a Redis service was open. Redis does not require authentication by default, so I connected to it and checked the available keys in the database. One of the keys stored the flag, and I was able to pull it directly from the running instance. This room showed how risky it is to leave Redis exposed to the internet, because anyone can connect and read whatever data is sitting in memory.
