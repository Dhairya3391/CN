# Lab Practical #05: Study the concept of VLAN using packet tracer

**Student Name:** Dhairya Adroja  
**Enrollment No:** 24010101602  
**Course:** B.Tech. CSE

---

## Aim/Objective

To implement different network structures in VLAN and VLAN trunking. Check connectivity between VLANs using ping command or PDU utility.

## Theory

VLAN (Virtual LAN) logically segments a physical network into multiple broadcast domains. Devices in the same VLAN can communicate directly, while inter-VLAN communication requires routing.

## Procedure

### 1. Basic VLAN Configuration

<div style="text-align: center;">
<img src="images/second.png" alt="VLAN Setup" width="580" style="max-width: 100%; height: auto;">
</div>

**VLAN Configuration:**

- VLAN 10 (Sales): PC1 (192.168.10.10/24), PC2 (192.168.10.11/24)
- VLAN 20 (IT): PC3 (192.168.20.10/24), PC4 (192.168.20.11/24)
- Switch: Catalyst 2960

**Switch Commands:**

```
enable
configure terminal
vlan 10
name Sales
vlan 20
name IT
interface fa0/1
switchport mode access
switchport access vlan 10
interface fa0/2
switchport mode access
switchport access vlan 10
interface fa0/3
switchport mode access
switchport access vlan 20
interface fa0/4
switchport mode access
switchport access vlan 20
```

**Testing:**

- Ping within VLAN 10: Successful
- Ping within VLAN 20: Successful
- Ping between VLANs: Failed (as expected)

---

### 2. VLAN Trunking Configuration

<div style="page-break-before: auto; text-align: center;">
<img src="images/hybrid.png" alt="VLAN Trunking" width="580" style="max-width: 100%; height: auto;">
</div>

**Configuration:**

- Switch1: VLAN 10 ports
- Switch2: VLAN 20 ports
- Trunk link between switches

**Trunk Commands:**

```
interface fa0/24
switchport mode trunk
switchport trunk allowed vlan 10,20
```

**Testing:** Inter-switch VLAN communication verified.

---

### 3. Inter-VLAN Routing

**Router Configuration:**

```
interface fa0/0.10
encapsulation dot1q 10
ip address 192.168.10.1 255.255.255.0
interface fa0/0.20
encapsulation dot1q 20
ip address 192.168.20.1 255.255.255.0
```

**Testing:** Cross-VLAN ping successful through router.

---

## Steps to Create VLANs in Packet Tracer

1. **Add Devices:** Place switches, PCs, router
2. **Configure VLANs:**
   - Switch CLI: `vlan [number]`, `name [name]`
3. **Assign Ports:**
   - `interface fa0/x`
   - `switchport access vlan [number]`
4. **Configure Trunk:**
   - `switchport mode trunk`
5. **Set IP Addresses:** Configure PCs with appropriate IPs
6. **Test:** Use ping or PDU utility

## Conclusion

Successfully implemented VLANs with trunking and inter-VLAN routing. VLANs provide network segmentation, improved security, and better traffic management in enterprise networks.
