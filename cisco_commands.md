# Lab Reference: Cisco Packet Tracer Commands and VLAN Configuration

**Student Name:** Dhairya Adroja  
**Enrollment No:** 24010101602  
**Course:** B.Tech. CSE

---

## Objective

This reference guide covers essential Cisco Packet Tracer commands for configuring switches and VLANs, providing a comprehensive command reference for network configuration tasks.

---

## Common Commands

| Command                       | Description                                                  |
| ----------------------------- | ------------------------------------------------------------ |
| `enable`                      | Enters privileged EXEC mode ("enable mode")                  |
| `conf t`                      | Enters global configuration mode                             |
| `vlan <id>`                   | Creates a VLAN with the specified ID                         |
| `name <name>`                 | Assigns a name to the current VLAN                           |
| `interface <type> <id>`       | Enters interface configuration mode (e.g., FastEthernet 0/1) |
| `switchport mode access`      | Sets the port as an access port (for end devices)            |
| `switchport mode trunk`       | Sets the port as a trunk port (for inter-switch links)       |
| `switchport access vlan <id>` | Assigns the port to a specific VLAN                          |

---

## Example Topology

**Scenario:**

- 2 Switches (SW1, SW2)
- 2 PCs (PC1, PC2)
- PC1 on VLAN 10, PC2 on VLAN 20
- SW1 and SW2 connected via trunk

```
PC1 ---- SW1 ==== SW2 ---- PC2
         |         |
      VLAN 10   VLAN 20
```

---

## Sample Configuration

### On SW1

```
enable
conf t
vlan 10
 name Sales
vlan 20
 name HR
interface FastEthernet 0/1
 switchport mode access
 switchport access vlan 10
interface FastEthernet 0/2
 switchport mode trunk
```

### On SW2

```
enable
conf t
vlan 10
 name Sales
vlan 20
 name HR
interface FastEthernet 0/1
 switchport mode trunk
interface FastEthernet 0/2
 switchport mode access
 switchport access vlan 20
```

---

## Notes and Best Practices

- Replace interface numbers as per your topology
- Use `show vlan brief` to verify VLAN configuration
- Use `show running-config` to see the current configuration
- Always save configuration using `copy running-config startup-config`
- Use `no shutdown` to enable interfaces if they are administratively down

---

**Student Name:** Dhairya Adroja  
**Enrollment No:** 24010101602  
**Course:** B.Tech. CSE  
**Date:** 02 July 2025
