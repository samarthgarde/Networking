# 07 – Subnetting & CIDR

**Subnetting** is the process of dividing a large network into smaller, more manageable sub-networks.  
**CIDR (Classless Inter-Domain Routing)** is a flexible way of assigning IP addresses and subnet masks.

These concepts are essential in:
- Cloud networking (VPCs, subnets)
- Kubernetes cluster planning
- Designing scalable, secure infrastructure

---

## 🔹 1. Why Subnetting?

- Organize network by teams/departments
- Improve security (isolated networks)
- Efficient IP allocation
- Better traffic management

---

## 🔹 2. IP Address Format

IPv4 Address = `192.168.10.1` (32 bits)

| Part         | Description        |
|--------------|--------------------|
| Network part | Identifies the network |
| Host part    | Identifies a device |

---

## 🔹 3. What is CIDR?

CIDR notation represents an IP address and subnet mask like:

