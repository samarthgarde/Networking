# 06 – Routing & Switching

Routing and Switching are core components of network communication. DevOps professionals often work with both — especially in cloud networking, virtual private clouds (VPCs), Kubernetes clusters, and VPN setups.

---

## 🔹 1. What is Switching?

**Switching** occurs at **Layer 2 (Data Link Layer)** of the OSI model.  
It connects devices **within the same network (LAN)**.

### ✅ Features:
- Uses **MAC addresses** to forward frames.
- Switches learn the MAC addresses of connected devices.
- Reduces unnecessary data flooding (unlike hubs).

### 🛠️ Real Example:
- In a local network, a switch connects computers, printers, and routers.
- Each device gets a dedicated path to communicate.

---

## 🔹 2. What is Routing?

**Routing** occurs at **Layer 3 (Network Layer)** of the OSI model.  
It connects **multiple networks together** and routes data between them.

### ✅ Features:
- Uses **IP addresses** to route packets.
- Routers maintain **routing tables**.
- Can be **static** or **dynamic** (using routing protocols like OSPF, BGP).

### 🛠️ Real Example:
- A router connects your home network to the internet.
- In cloud (AWS/GCP), **route tables** define how traffic flows inside VPCs.

---

## 🔹 3. Key Differences

| Feature       | Switching                          | Routing                               |
|---------------|------------------------------------|----------------------------------------|
| OSI Layer     | Layer 2 (Data Link)                | Layer 3 (Network)                      |
| Address Used  | MAC Address                        | IP Address                             |
| Purpose       | Connect devices in same network    | Connect different networks             |
| Device Used   | Switch                             | Router                                 |
| Protocol      | Ethernet                           | IP (Routing Protocols: BGP, OSPF)      |

---

## 🔹 4. Linux Routing Basics

### 🧪 View Routing Table
```bash
ip route show

