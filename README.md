# subnetting

Task:

193.16.20.35/29

What is the Network IP, number of hosts, range of IP addresses and broadcast IP from this subnet?

Instruction: Submit all your answer as a markdown file in the folder for this exercise.

Steps:
To solve the above task, we have to get the subnet mask from the given CIDR (/29)


>NOTE: CIDR/Subnet - CIDR is known as CIDR notation, it simply identifies the size of a subnet. Another way to define the size of a subnet is called subnet mask. you will need to know how to convert between subnet mask and cidr notation or >essentially the number of IP addresses in each subnet

From the given IP above, the subnet mask in binary will be:
Subnet Mask in binary format=11111111.11111111.11111111.11111000

>Note: Network Portion is 1s while Host Portion is 0s

Haven gotten the subnet mask in binary, lets convert to decimal format using the formula below;

 | Group Size Derivation | $2^7$                                                           | $2^6$ | $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ |
|-----------------------|-----------------------------------------------------------------|-------|-------|-------|-------|-------|-------|-------|
| Group Size            | 128                                                             | 64    | 32    | 16    | 8     | 4     | 2     | 1     |

Add the above Group size to get the total number of subnet mask in decimal format
```
128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 + 0 = 255
```
using the group size above, lets calculate the subnet mask derived from the given IP

**First Subnet mask:**

 | Group Size | 128                                                           | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----------------------|-----------------------------------------------------------------|-------|-------|-------|-------|-------|-------|-------|
| First Subnet Mask            | 1                                                           | 1   | 1  | 1   | 1     | 1    | 1    | 1     |

Total subnet mask=255

---
**Second subnet Mask:**

 | Group Size | 128                                                           | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----------------------|-----------------------------------------------------------------|-------|-------|-------|-------|-------|-------|-------|
| Second Subnet Mask            | 1                                                           | 1   | 1  | 1   | 1     | 1    | 1    | 1     |

Total subnet mask=255

---
**Third subnet mask:**

 | Group Size | 128                                                           | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----------------------|-----------------------------------------------------------------|-------|-------|-------|-------|-------|-------|-------|
| Third Subnet Mask            | 1                                                           | 1   | 1  | 1   | 1     | 1    | 1    | 1     |

Total subnet mask=255

---
**Fourth subnet mask**

 | Group Size | 128                                                           | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----------------------|-----------------------------------------------------------------|-------|-------|-------|-------|-------|-------|-------|
| Fourth Subnet Mask            | 1                                                           | 1   | 1  | 1   | 1     | 0    | 0   | 0    |

Total subnet mask=248

---
Sum of all subnet mask in decimal=255.255.255.248

Subnet Mask in binary format=11111111.11111111.11111111.11111000

**Lets find the Network ID:**

> Note: we will use `and` operation between the given IP converted to binary and the subnet mask

Since the first three octect of our given IP is constant, we will only calculate with the fourth octect to determine our network ID 
where;
Subnet Mask=11111111.11111111.11111111.11111000
Given IP in Binary=11000001.00010000.000101000.00100011

**Fourth octect:**


 | Subnet Mask | 1                                                           | 1 | 1 | 1 | 1 | 0 | 0 | 0 |
|-----------------------|-----------------------------------------------------------------|-------|-------|-------|-------|-------|-------|-------|
| Given IP            | 0                                                           | 0   | 1  | 0   | 0     | 0    | 1   | 1   |
| Result            | 0                                                           | 0   | 1  | 0   | 0     | 0    | 0   | 0    |

Output of the above operation in decimal=32
Therefore network IP=193.16.20.32


