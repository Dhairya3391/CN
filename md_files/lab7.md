# Lab Practical #07: Application Layer Protocols - DNS, DHCP, FTP

**Student Name:** Dhairya Adroja  
**Enrollment No:** 24010101602  
**Course:** B.Tech. CSE

---

## Aim

Implement DNS, DHCP, and FTP protocols using Cisco Packet Tracer and verify connectivity.

## Theory

- **DNS:** Translates domain names to IP addresses (Port 53)
- **DHCP:** Automatically assigns IP addresses (Ports 67/68)
- **FTP:** File transfer protocol (Ports 20/21)

## Network Setup

### Topology

```
    [Switch]
        |
+-------+-------+
|       |       |
PC1    PC2   [Servers]
              /   |   \
         DNS  DHCP  FTP
```

### IP Configuration

| Device      | IP Address           | Role              |
| ----------- | -------------------- | ----------------- |
| DNS Server  | 192.168.1.10         | Domain resolution |
| DHCP Server | 192.168.1.11         | IP assignment     |
| FTP Server  | 192.168.1.12         | File transfer     |
| PC1         | 192.168.1.100 (DHCP) | Client            |
| PC2         | 192.168.1.101 (DHCP) | Client            |

#### DNS Configuration Steps:

1. Configure server with static IP address
2. Enable DNS service
3. Add DNS records:
   - www.example.com → 192.168.1.20
   - mail.example.com → 192.168.1.30
   - ftp.example.com → 192.168.1.40

### 2. DHCP Server Configuration

**Server IP:** 192.168.1.11  
**Subnet Mask:** 255.255.255.0  
**Default Gateway:** 192.168.1.1

## Configuration Steps

### 1. DNS Server (192.168.1.10)

- Enable DNS service
- Add records: www.example.com → 192.168.1.20

### 2. DHCP Server (192.168.1.11)

- Enable DHCP service
- Pool: 192.168.1.100-150, Gateway: 192.168.1.1

### 3. FTP Server (192.168.1.12)

- Enable FTP service
- Users: admin/admin123, user1/user123

## Testing Results

### Connectivity Tests

```bash
# PC1 to DNS Server
C:\> ping 192.168.1.10
Reply from 192.168.1.10: bytes=32 time<1ms TTL=128

# DNS Resolution
C:\> nslookup www.example.com
Server: 192.168.1.10
Address: 192.168.1.20

# FTP Access
C:\> ftp 192.168.1.12
Connected to 192.168.1.12
User: admin
230 User logged in
```

### DHCP Verification

- PC1 auto-assigned: 192.168.1.100
- PC2 auto-assigned: 192.168.1.101

## Conclusion

Successfully implemented and tested DNS, DHCP, and FTP protocols. All services working properly with confirmed connectivity.

---

**Date:** August 23, 2025
