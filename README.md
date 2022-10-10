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

Haven gotten the subnet mask in binary, lets convert it to decimal format

 | Group Size Derivation | $2^7$                                                           | $2^6$ | $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ |
|-----------------------|-----------------------------------------------------------------|-------|-------|-------|-------|-------|-------|-------|
| Group Size            | 128                                                             | 64    | 32    | 16    | 8     | 4     | 2     | 1     |






