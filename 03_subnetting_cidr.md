# 03 – Subnetting & CIDR

Subnetting and CIDR are essential for organizing and managing IP addresses within networks — especially in cloud infrastructure and container orchestration.

---

## 🔹 1. What is Subnetting?

**Subnetting** is the process of dividing a large IP network into smaller, more manageable subnetworks (subnets). It helps:
- Improve network performance
- Enhance security and isolation
- Optimize IP address usage

---

## �� 2. IP Address Structure

### IPv4 Format:
- 32-bit address written as 4 octets (e.g., `192.168.10.15`)
- Divided into **Network** and **Host** portions

---

## 🔹 3. What is CIDR?

**CIDR** = Classless Inter-Domain Routing  
- Notation: `IP_address/prefix_length`
- Example: `192.168.1.0/24`

### Prefix Length:
- `/24` → First 24 bits are the network part  
- Remaining 8 bits are for hosts

---

## 🔹 4. Subnet Mask Table (Common Prefixes)

| CIDR     | Subnet Mask        | Hosts per Subnet |
|----------|--------------------|------------------|
| /30      | 255.255.255.252    | 2 usable         |
| /29      | 255.255.255.248    | 6 usable         |
| /28      | 255.255.255.240    | 14 usable        |
| /27      | 255.255.255.224    | 30 usable        |
| /26      | 255.255.255.192    | 62 usable        |
| /24      | 255.255.255.0      | 254 usable       |
| /16      | 255.255.0.0        | 65,534 usable    |

---

## 🔹 5. Example: Subnetting a `/24` Network

- Given: `192.168.1.0/24`
- Want: 4 subnets  
- Solution: Use `/26` (2 extra bits)

### Resulting Subnets:
- `192.168.1.0/26` → Hosts: `.1` to `.62`
- `192.168.1.64/26` → Hosts: `.65` to `.126`
- `192.168.1.128/26` → Hosts: `.129` to `.190`
- `192.168.1.192/26` → Hosts: `.193` to `.254`

---

## 🔹 6. How to Calculate Subnets (Manual Steps)

1. Convert subnet mask to binary  
2. Count number of host bits  
3. 2ⁿ - 2 = usable hosts  
4. Increment subnet base by block size  
   - Block size = `256 - subnet mask last octet`

---

## 🔹 7. Use Cases in DevOps

| Platform | Use Case                               |
|----------|----------------------------------------|
| AWS      | Dividing VPC into public/private subnets |
| Kubernetes | Allocating Pod and Service CIDRs       |
| Docker   | Custom bridge networks for containers  |

---

## 🔹 8. Helpful Tools

- [Subnet Calculator – ipcalc](https://jodies.de/ipcalc)
- `ipcalc` (CLI):
```bash
sudo apt install ipcalc
ipcalc 192.168.1.0/25

