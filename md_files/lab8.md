# Lab Practical #08: Network Infrastructure Survey

**Student Name:** Dhairya Adroja  
**Enrollment No:** 24010101602  
**Course:** B.Tech. CSE

---

## Aim

Study and survey institute network infrastructure, identify network types, and document devices and cables used.

## Network Type Identification

**Primary Network:** Hierarchical Star Topology with Wireless Integration

### Classification:

- **LAN:** Building/floor networks
- **WLAN:** Campus-wide Wi-Fi
- **MAN:** Inter-building connectivity
- **WAN:** Internet connection

## CS Department Network Design

### Topology Diagram

```
           [Internet]
               |
        [Core Router]
               |
    [Distribution Switch]
               |
    +----------+----------+
    |          |          |
[Lab Switch] [WiFi AP] [Server Rack]
    |          |          |
[30 PCs]   [WiFi Users] [2 Servers]
```

## Device Inventory

### Network Equipment

| Device Type   | Model               | Quantity | Location          |
| ------------- | ------------------- | -------- | ----------------- |
| Core Router   | Cisco ASR 1001-X    | 1        | Server Room       |
| Core Switch   | Cisco Catalyst 3850 | 3        | Each Building     |
| Access Switch | Cisco SG350-28P     | 24       | Computer Labs     |
| Wireless AP   | Cisco AIR-AP2802I   | 45       | Throughout Campus |
| Desktop PCs   | Various             | 480      | Labs              |

### Cable Infrastructure

| Cable Type  | Usage               | Distance | Standard         |
| ----------- | ------------------- | -------- | ---------------- |
| Fiber Optic | Backbone            | 100m-2km | 1000BASE-LX      |
| Cat 6A UTP  | Desktop connections | 100m max | Gigabit Ethernet |
| Cat 6 UTP   | Access layer        | 100m max | Gigabit Ethernet |

## VLAN Configuration

| VLAN | Subnet          | Purpose  |
| ---- | --------------- | -------- |
| 10   | 192.168.10.0/24 | Faculty  |
| 20   | 192.168.20.0/24 | Students |
| 30   | 192.168.30.0/24 | Servers  |
| 40   | 192.168.40.0/24 | WiFi     |

## Network Services

- **DHCP:** Automatic IP assignment
- **DNS:** Internal domain resolution
- **RADIUS:** Wireless authentication
- **VLAN Segmentation:** Security isolation

## Performance Specifications

- **Internet:** 1 Gbps fiber connection
- **Core Network:** 10 Gbps backbone
- **Access Layer:** 100 Mbps per port
- **Coverage:** 3 buildings, 2000+ users

## Conclusion

Institute uses hierarchical star topology with wireless integration. Network serves 2000+ users across 3 buildings with 150+ devices, fiber backbone, and comprehensive VLAN segmentation for security and performance.

### Summary:

- **Network Type:** Hierarchical Star + Wireless
- **Total Devices:** 150+ (switches, routers, APs)
- **Cable Types:** Fiber backbone + Cat6A access
- **User Capacity:** 2000+ concurrent users

---

**Date:** August 23, 2025

1. **Network Type:** Hierarchical Star with Wireless Integration
2. **Total Network Devices:** 150+ active devices
3. **Cable Types:** Fiber optic backbone, Cat6A/Cat6 copper access
4. **Coverage Area:** 3 buildings, 12 floors, 50+ rooms
5. **User Capacity:** 2000+ concurrent users
6. **Internet Bandwidth:** 1 Gbps dedicated connection

---

**Date:** August 23, 2025  
