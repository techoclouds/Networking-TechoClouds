
# Chapter 6: Subnetting Basics

## 6.1 Why Subnet?
- **Network Efficiency**: Subnetting reduces broadcast traffic and segments networks into manageable, logical pieces, enhancing overall network performance.
- **Enhanced Security**: Limits the broadcast domain, increasing security by isolating broadcast traffic within specific subnets.
- **Resource Optimization**: Enables efficient use of an IP address space within large networks, preventing address exhaustion.

## 6.2 Subnet Masks
- **Definition**: A subnet mask is a 32-bit number that masks an IP address, dividing the IP address into network and host parts.
- **Function**: Subnet masks determine the network and host portions of an IP address, allowing the creation of multiple subnetworks from a single network.



Default Subnet Mask (Class C): 255.255.255.0
```
Binary Form:                     11111111.11111111.11111111.00000000
                                 [NNNNNNNN.NNNNNNNN.NNNNNNNN.HHHHHHHH]
                                 (N=Network bits, H=Host bits)
```

## 6.3 Calculating Subnets
### Example 1: Basic Subnetting of a Class C Network
- **Objective**: Divide a Class C network (`192.168.1.0/24`) into 4 subnets.

### Calculation:
- **Mathematical Breakdown**:
  - **Step 1**: Determine how many bits to borrow using the formula `2^n ≥ number of subnets`. For 4 subnets, `n` must be at least 2 because `2^2 = 4`.
  - **Step 2**: Apply the new subnet mask by borrowing 2 bits. This changes the subnet mask from `/24` (255.255.255.0) to `/26` (255.255.255.192), providing 64 addresses per subnet.
  - **Step 3**: Calculate the IP address range for each subnet, noting that the first and last addresses (network and broadcast respectively) are not usable for hosts.
  - **Step 4**: Calculate usable hosts: \(2^{number\ of\ host\ bits} - 2\). For `/26`, it's \(2^6 - 2 = 62\) usable hosts per subnet.


```
Network ID: 192.168.1.0/26
Usable Range: 192.168.1.1 to 192.168.1.62
Broadcast: 192.168.1.63
---
Network ID: 192.168.1.64/26
Usable Range: 192.168.1.65 to 192.168.1.126
Broadcast: 192.168.1.127
---
Network ID: 192.168.1.128/26
Usable Range: 192.168.1.129 to 192.168.1.190
Broadcast: 192.168.1.191
---
Network ID: 192.168.1.192/26
Usable Range: 192.168.1.193 to 192.168.1.254
Broadcast: 192.168.1.255
```
### Example 2: Advanced Subnetting of a Class B Network
- **Objective**: Subnet a Class B network (`172.16.0.0/16`) into 32 subnets.

### Calculation:
- **Mathematical Breakdown**:
  - **Step 1**: Calculate the new subnet mask by determining how many bits to borrow. For 32 subnets, `n` must be 5 because `2^5 = 32`.
  - **Step 2**: Apply the new subnet mask by borrowing 5 bits, resulting in a subnet mask of `/21` (255.255.248.0), which gives 2048 addresses per subnet.
  - **Step 3**: Detail the range for each subnet.
  - **Step 4**: Calculate usable hosts: \(2^{number\ of\ host\ bits} - 2\). For `/21`, it's \(2^{11} - 2 = 2046\) usable hosts per subnet.
## 6.4 Classful vs. Classless Subnetting


 Classful Subnetting: Fixed blocks (Class A, B, C)
 Classless Subnetting (CIDR): Flexible block sizes (e.g., /26, /21)




## 6.5 CIDR Notation
- **Explanation**: CIDR notation expresses an IP address and its associated network mask.
- **Example**: `192.168.1.0/26` indicates a subnet mask of `255.255.255.192`, specifying the network portion of the address.

```
CIDR: 192.168.1.0/26
Binary: 11000000.10101000.00000001.00000000/26
Mask:   255.255.255.192
```
