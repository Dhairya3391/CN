# Lab Practical #04: Installation of Network Simulator (Packet Tracer) and Implement different LAN topologies

**Student Name:** Dhairya Adroja  
**Enrollment No:** 24010101602  
**Course:** B.Tech. CSE

---

## Aim/Objective

To install Network Simulator (Packet Tracer) and implement different LAN topologies. Check connectivity between devices using ping command or PDU utility.

## Theory

Network topology refers to the arrangement of devices in a computer network. Each topology has specific characteristics and use cases in network design.

## Procedure

### 1. Simple Network with Switch and PCs

![Basic Network Setup](images/first.png)

**Configuration:**

- PC1: 192.168.1.10/24
- PC2: 192.168.1.11/24
- PC3: 192.168.1.12/24
- Switch: Catalyst 2960

**Testing:** Ping successful between all PCs.

---

### 2. Bus Topology

![Bus Topology](images/bus.png)

**Configuration:**

- PC1: 192.168.2.10/24
- PC2: 192.168.2.11/24
- PC3: 192.168.2.12/24
- PC4: 192.168.2.13/24

**Characteristics:**

- Single backbone cable
- Cost-effective for small networks
- Single point of failure

**Testing:** PDU simulation successful along backbone.

---

### 3. Ring Topology

![Ring Topology](images/ring.png)

**Configuration:**

- PC1: 192.168.3.10/24
- PC2: 192.168.3.11/24
- PC3: 192.168.3.12/24
- PC4: 192.168.3.13/24

**Characteristics:**

- Circular connection pattern
- Token passing mechanism
- Deterministic access

**Testing:** Token circulation verified.

---

### 4. Star Topology

![Star Topology](images/star.png)

**Configuration:**

- PC1: 192.168.4.10/24
- PC2: 192.168.4.11/24
- PC3: 192.168.4.12/24
- PC4: 192.168.4.13/24

**Characteristics:**

- Central hub/switch
- Most common in LANs
- Easy troubleshooting

**Testing:** All pings successful.

---

### 5. Mesh Topology

![Mesh Topology](images/mesh.png)

**Configuration:**

- PC1: 192.168.5.10/24
- PC2: 192.168.5.11/24
- PC3: 192.168.5.12/24
- PC4: 192.168.5.13/24

**Characteristics:**

- Every device connected to others
- Maximum redundancy
- High cost

**Testing:** Multiple paths verified.

---

### 6. Tree Topology

![Tree Topology](images/tree.png)

**Configuration:**

- PC1-PC2: 192.168.6.10-11/24
- PC3-PC4: 192.168.6.12-13/24

**Characteristics:**

- Hierarchical structure
- Scalable design
- Combined star-bus features

**Testing:** Inter-branch communication successful.

---

## Steps to Create Networks in Packet Tracer

1. **Launch Packet Tracer**
2. **Add Devices:** Drag PCs, switches from device panel
3. **Connect:** Use appropriate cables between devices
4. **Configure IPs:** PC → Desktop → IP Configuration
5. **Test:** Use ping command or PDU utility

## Conclusion

Successfully implemented all LAN topologies in Packet Tracer. Each topology serves different network requirements based on cost, scalability, and fault tolerance needs.
