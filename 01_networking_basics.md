# Networking Basics

### ✅ IP Address

- A unique identifier for each device on a network.
- **IPv4**: e.g., `192.168.1.1`
- **IPv6**: e.g., `2001:0db8:85a3::8a2e:0370:7334`
- Can be **static** (fixed) or **dynamic** (changes via DHCP).

---

### ✅ MAC Address
- A hardware address burned into your network interface.
- Format: `00:1A:2B:3C:4D:5E`
- Used in Layer 2 (Data Link) for LAN communication.

---

### ✅ Port Numbers
- Logical endpoints for network services.
- Example:
  - `22` → SSH
  - `80` → HTTP
  - `443` → HTTPS
- Format: `IP:Port` (e.g., `192.168.0.1:22`)

---

### ✅ Protocol
- A set of rules for communication.
- Common protocols:
  - **TCP** – Reliable, connection-oriented.
  - **UDP** – Faster, connectionless.
  - **ICMP** – Used by `ping`.

---

### ✅ Public vs Private IP

| Type        | Range                                | Used For                  |
|-------------|---------------------------------------|---------------------------|
| Private IP  | `10.0.0.0 – 10.255.255.255`<br>`172.16.0.0 – 172.31.255.255`<br>`192.168.0.0 – 192.168.255.255` | Internal LAN/Subnets      |
| Public IP   | All other addresses                   | Internet-accessible hosts |


---

### ✅ Tools to Check Networking in Linux

```bash
ip a             # Show IP addresses
ip r             # Show routing table
ping 8.8.8.8     # Check connectivity
nslookup google.com  # DNS lookup
netstat -tulnp   # Show listening ports and services
