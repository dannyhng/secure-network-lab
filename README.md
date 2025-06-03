# 🔐 Secure Network Infrastructure Lab

A simulated secure network environment designed in Cisco Packet Tracer to demonstrate core principles of network segmentation, access control, NAT, VPN, and basic threat detection.

## 🧱 Network Topology

- 3 VLANs: Admin, Staff, Guest
- Layer 3 Router-on-a-Stick for inter-VLAN routing
- ACLs to control access between segments
- NAT for outbound Internet simulation
- Simulated site-to-site VPN between two routers
- Monitoring of unauthorized access attempts

---

## 🛠 Tools Used

- Cisco Packet Tracer
- (Optional) Wireshark (for offline packet analysis)
- Static Routing, ACLs, VLANs, NAT, VPN Simulation

---

## ⚙️ Configuration Highlights

### 🔹 VLAN Setup (Switch)
```bash
vlan 10
name Admin
vlan 20
name Staff
vlan 30
name Guest
interface range fa0/1 - 2
switchport mode access
switchport access vlan 10
```
### 🔹 Router-on-a-Stick (Router)
```bash
interface fa0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
```

### 🔹 ACL Example
```bash
access-list 100 deny ip 192.168.30.0 0.0.0.255 192.168.10.0 0.0.0.255
access-list 100 permit ip any any
interface fa0/0
ip access-group 100 in
```

### 🎯 Learning Objectives
- Practice configuring VLANs, ACLs, NAT, and VPN in a simulated environment
- Understand secure network segmentation
- Analyze basic unauthorized access attempts
- Prepare for CCNA or cybersecurity certification labs
