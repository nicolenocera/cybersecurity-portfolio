### Dancing

For Dancing, I scanned the machine and found that SMB was running. I used basic enumeration to check the available shares and saw that one of them could be accessed without any credentials. I connected to that share, looked through the folders, and found the flag inside. This room showed how exposed an SMB share can be if it is not locked down, because anyone on the network can browse it and grab whatever is stored there.
