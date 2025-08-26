# Lab Practical #10: Study of IP Addressing and Sub-netting

**Student Name:** Dhairya Adroja  
**Enrollment No:** 24010101602  
**Course:** B.Tech. CSE

---

## Aim/Objective

To study IP addressing and sub-netting concepts, including finding default subnet masks, network bits, host bits, hosts per subnet, number of subnets, subnet number, valid IP addresses, and broadcast addresses.

## Theory

IP addressing is a fundamental concept in networking that involves assigning unique identifiers to devices on a network. Subnetting is the process of dividing a larger network into smaller sub-networks to improve network performance, security, and management.

### Key Concepts:

1. **IP Address Classes:**

   - Class A: 1.0.0.0 to 126.0.0.0 (Default mask: /8 or 255.0.0.0)
   - Class B: 128.0.0.0 to 191.255.0.0 (Default mask: /16 or 255.255.0.0)
   - Class C: 192.0.0.0 to 223.255.255.0 (Default mask: /24 or 255.255.255.0)

2. **CIDR Notation:** Uses /n format where n represents the number of network bits

3. **Subnet Calculations:**
   - Network bits: Determine the network portion
   - Host bits: Determine the host portion
   - Hosts per subnet: 2^(host bits) - 2
   - Number of subnets: 2^(borrowed bits)

## Procedure

### Problem 1: Find subnet details for given IP addresses

#### i. 8.1.4.5/16

**Solution:**

- **IP Address:** 8.1.4.5
- **CIDR:** /16
- **Class:** A (since first octet is 8)
- **Default Subnet Mask:** 255.0.0.0 (/8)
- **Given Subnet Mask:** 255.255.0.0 (/16)
- **Network Bits:** 16
- **Host Bits:** 32 - 16 = 16
- **Hosts per Subnet:** 2^16 - 2 = 65,534
- **Number of Subnets:** 2^(16-8) = 256
- **Network Address:** 8.1.0.0
- **First Valid IP:** 8.1.0.1
- **Last Valid IP:** 8.1.255.254
- **Broadcast Address:** 8.1.255.255

#### ii. 130.4.102.1/24

**Solution:**

- **IP Address:** 130.4.102.1
- **CIDR:** /24
- **Class:** B (since first octet is 130)
- **Default Subnet Mask:** 255.255.0.0 (/16)
- **Given Subnet Mask:** 255.255.255.0 (/24)
- **Network Bits:** 24
- **Host Bits:** 32 - 24 = 8
- **Hosts per Subnet:** 2^8 - 2 = 254
- **Number of Subnets:** 2^(24-16) = 256
- **Network Address:** 130.4.102.0
- **First Valid IP:** 130.4.102.1
- **Last Valid IP:** 130.4.102.254
- **Broadcast Address:** 130.4.102.255

#### iii. 130.4.102.1/22

**Solution:**

- **IP Address:** 130.4.102.1
- **CIDR:** /22
- **Class:** B (since first octet is 130)
- **Default Subnet Mask:** 255.255.0.0 (/16)
- **Given Subnet Mask:** 255.255.252.0 (/22)
- **Network Bits:** 22
- **Host Bits:** 32 - 22 = 10
- **Hosts per Subnet:** 2^10 - 2 = 1,022
- **Number of Subnets:** 2^(22-16) = 64
- **Network Address:** 130.4.100.0 (102 & 252 = 100)
- **First Valid IP:** 130.4.100.1
- **Last Valid IP:** 130.4.103.254
- **Broadcast Address:** 130.4.103.255

#### iv. 199.1.1.100/27

**Solution:**

- **IP Address:** 199.1.1.100
- **CIDR:** /27
- **Class:** C (since first octet is 199)
- **Default Subnet Mask:** 255.255.255.0 (/24)
- **Given Subnet Mask:** 255.255.255.224 (/27)
- **Network Bits:** 27
- **Host Bits:** 32 - 27 = 5
- **Hosts per Subnet:** 2^5 - 2 = 30
- **Number of Subnets:** 2^(27-24) = 8
- **Network Address:** 199.1.1.96 (100 & 224 = 96)
- **First Valid IP:** 199.1.1.97
- **Last Valid IP:** 199.1.1.126
- **Broadcast Address:** 199.1.1.127

### Problem 2: Class C network analysis (192.168.17.9)

**Given:** IP address 192.168.17.9 (Class C network)

**Solution:**

- **Class:** C
- **Default Subnet Mask:** 255.255.255.0 (/24)
- **Network Address:** 192.168.17.0
- **Number of addresses in block:** 256 (2^8)
- **First Address:** 192.168.17.0
- **Last Address:** 192.168.17.255

### Problem 3: Block analysis for 185.28.17.9

**Given:** IP address 185.28.17.9

**Solution:**

- **Class:** B (assuming default /16)
- **Default Subnet Mask:** 255.255.0.0 (/16)
- **Network Address:** 185.28.0.0
- **Number of addresses in block:** 65,536 (2^16)
- **First Address:** 185.28.0.0
- **Last Address:** 185.28.255.255

### Problem 4: Block analysis for 205.16.37.39/28

**Given:** IP address 205.16.37.39/28

**Solution:**

- **IP Address:** 205.16.37.39
- **CIDR:** /28
- **Subnet Mask:** 255.255.255.240
- **Host Bits:** 32 - 28 = 4
- **Number of addresses in block:** 2^4 = 16
- **Network Address:** 205.16.37.32 (39 & 240 = 32)
- **First Address:** 205.16.37.32
- **Last Address:** 205.16.37.47

### Problem 5: Subnet 216.21.5.0 for 30 hosts per subnet

**Given:** IP address 216.21.5.0, need 30 hosts per subnet

**Solution:**

- **Class:** C
- **Default Mask:** 255.255.255.0 (/24)
- **Required host bits:** log₂(30+2) = 5 bits (2^5 = 32, accommodates 30 hosts)
- **Bits Borrowed:** 8 - 5 = 3 bits
- **New Subnet Mask:** 255.255.255.224 (/27)
- **Number of Subnets:** 2^3 = 8
- **Number of Hosts per Subnet:** 2^5 - 2 = 30

**Network Ranges (Subnets):**

1. 216.21.5.0/27 (216.21.5.0 - 216.21.5.31)
2. 216.21.5.32/27 (216.21.5.32 - 216.21.5.63)
3. 216.21.5.64/27 (216.21.5.64 - 216.21.5.95)
4. 216.21.5.96/27 (216.21.5.96 - 216.21.5.127)
5. 216.21.5.128/27 (216.21.5.128 - 216.21.5.159)
6. 216.21.5.160/27 (216.21.5.160 - 216.21.5.191)
7. 216.21.5.192/27 (216.21.5.192 - 216.21.5.223)
8. 216.21.5.224/27 (216.21.5.224 - 216.21.5.255)

### Problem 6: Subnet 192.10.20.0 for 52 hosts per subnet

**Given:** IP address 192.10.20.0, need 52 hosts per subnet

**Solution:**

- **Class:** C
- **Default Mask:** 255.255.255.0 (/24)
- **Required host bits:** log₂(52+2) = 6 bits (2^6 = 64, accommodates 52 hosts)
- **Bits Borrowed:** 8 - 6 = 2 bits
- **New Subnet Mask:** 255.255.255.192 (/26)
- **Number of Subnets:** 2^2 = 4
- **Number of Hosts per Subnet:** 2^6 - 2 = 62

**Network Ranges (Subnets):**

1. 192.10.20.0/26 (192.10.20.0 - 192.10.20.63)
2. 192.10.20.64/26 (192.10.20.64 - 192.10.20.127)
3. 192.10.20.128/26 (192.10.20.128 - 192.10.20.191)
4. 192.10.20.192/26 (192.10.20.192 - 192.10.20.255)

### Problem 7: Determining Subnet Mask for Devices A and B

#### Device A: 172.16.17.30/20

**Solution:**

- **IP Address:** 172.16.17.30
- **CIDR:** /20
- **Class:** B
- **Subnet Mask:** 255.255.240.0
- **Network Address:** 172.16.16.0 (17 & 240 = 16)
- **Network Range:** 172.16.16.0 - 172.16.31.255

#### Device B: 172.16.28.15/20

**Solution:**

- **IP Address:** 172.16.28.15
- **CIDR:** /20
- **Class:** B
- **Subnet Mask:** 255.255.240.0
- **Network Address:** 172.16.16.0 (28 & 240 = 16)
- **Network Range:** 172.16.16.0 - 172.16.31.255

**Analysis:** Both devices A and B are in the same subnet (172.16.16.0/20) since they have the same network address when the subnet mask is applied.

## Conclusion

This lab provided comprehensive understanding of IP addressing and subnetting concepts including:

1. **Subnet Calculations:** Successfully calculated network addresses, host ranges, and broadcast addresses for various CIDR notations.

2. **Class-based Addressing:** Identified IP address classes and their default subnet masks.

3. **Subnetting Techniques:** Applied subnetting to meet specific host requirements while optimizing network design.

4. **Practical Applications:** Analyzed real-world scenarios involving device placement and network planning.

5. **Binary Operations:** Used bitwise AND operations to determine network addresses and subnet boundaries.

The exercises demonstrated the importance of proper subnetting in network design for efficient IP address utilization and network segmentation.

---

**Date:** August 26, 2025  
**Submitted by:** Dhairya Adroja
