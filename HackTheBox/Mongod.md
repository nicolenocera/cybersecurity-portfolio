### Mongod

For Mongod, I scanned the machine and found that a MongoDB service was open without any authentication. I connected to it, listed the available databases, and looked through the collections to see what was stored. One of the collections contained the flag, and I was able to read it directly from the database. This room showed how insecure a database can be when it is exposed to the network with no login required, because anyone can connect and view the data.
