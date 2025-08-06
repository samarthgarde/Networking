# 06 – TCP vs UDP

TCP and UDP are two core **transport layer protocols (Layer 4)** in the OSI model.  
Understanding how they differ helps DevOps engineers configure reliable vs fast communication in networks, services, containers, and cloud environments.

---

## 🔹 1. What is TCP?

**TCP (Transmission Control Protocol)** is a **connection-oriented**, reliable protocol.

### ✅ Key Features:
- **3-way handshake**: Ensures a connection is established
- **Reliable**: Retransmits lost packets
- **Ordered delivery**: Packets arrive in sequence
- **Flow & Congestion control**

### 📦 Used For:
| Application | Reason                        |
|-------------|-------------------------------|
| HTTP/HTTPS  | Reliable web browsing         |
| SSH         | Secure login sessions         |
| FTP         | File transfer with checks     |
| SMTP        | Email transfer with confirmation |

---

## 🔹 2. What is UDP?

**UDP (User Datagram Protocol)** is a **connectionless**, fast protocol.

### ✅ Key Features:
- No connection setup (no handshake)
- No guarantee of delivery
- Packets may arrive out of order
- Lightweight and faster

### 📦 Used For:
| Application      | Reason                             |
|------------------|------------------------------------|
| DNS              | Fast resolution, small data        |
| Video streaming  | Tolerates loss, prioritizes speed  |
| VoIP             | Real-time voice calls              |
| Gaming           | Fast real-time data updates        |

---

## 🔹 3. Key Differences

| Feature             | TCP                                  | UDP                                |
|---------------------|---------------------------------------|------------------------------------|
| Connection          | Connection-oriented (handshake)      | Connectionless                     |
| Reliability         | Reliable (acknowledgements, retransmit) | Unreliable                         |
| Order of Delivery   | Guaranteed                           | Not guaranteed                     |
| Speed               | Slower (due to overhead)             | Faster (less overhead)             |
| Header Size         | 20 bytes                             | 8 bytes                            |
| Use Cases           | Web, SSH, Email                      | Streaming, DNS, VoIP, Games        |

---

## 🔹 4. TCP/UDP in Linux

### 🧪 List Listening Ports
```bash
sudo netstat -tuln
# or
sudo ss -tuln

