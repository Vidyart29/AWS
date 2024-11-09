Subnets: 

![subnet1](image.png)

- Subnets are group of IP address in your VPC
- A subnet reside within a single AZ.
- Subnets can pe made public and private to allow external internet access to resources within them.
- Subnets within a VPC must be within the cidr range
- subnet block size must be between a /16 and /28 
**First 4 IP address of a subnet are reserved and cannot be used👇**
```
192.168.10.0 (Network address)
192.168.10.1-192.168.10.3 (for AWS)
192.168.10.1 (VPC Router)
192.168.10.2 (DNS)
192.168.10.3 (for future use )
```
The last ip addr is reserved as the broadcast address.
```
192.168.10.255
```

