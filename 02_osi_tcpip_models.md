# 02 – OSI & TCP/IP Models

| **Layer** | **Layer Name**   | **Function**                                                   | **Example Protocols**                      | **Devices Used**        | **Real-life Example**                               |
| --------- | ---------------- | -------------------------------------------------------------- | ------------------------------------------ | ----------------------- | --------------------------------------------------- |
| 7         | **Application**  | Interfaces with user applications                              | HTTP, HTTPS, FTP, DNS, SMTP, Telnet, DHCP  | Computer, Browser       | Typing a URL in Chrome                              |
| 6         | **Presentation** | Data translation, encryption, compression                      | SSL/TLS, JPEG, MP3, MPEG, ASCII            | Encryption Software     | Securing data via HTTPS                             |
| 5         | **Session**      | Establishes, manages, and terminates sessions                  | NetBIOS, PPTP, RPC, SIP                    | API, OS session manager | Keeping a video call connected                      |
| 4         | **Transport**    | Reliable delivery, error checking, flow control                | TCP, UDP, SCTP                             | Firewall, OS kernel     | Streaming a YouTube video                           |
| 3         | **Network**      | Logical addressing and routing                                 | IP, ICMP, IGMP, IPSec, ARP                 | Router                  | Data travels across internet hops                   |
| 2         | **Data Link**    | MAC addressing, framing, error detection                       | Ethernet, PPP, ARP, Frame Relay, HDLC      | Switch, NIC             | LAN connection via Ethernet                         |
| 1         | **Physical**     | Transmits raw bits via physical medium (cables, signals, etc.) | Ethernet Cables, Wi-Fi (802.11), Bluetooth | Hub, Cable, Fiber       | Sending bits through copper wire or wireless signal |

---

## 🔹 2. TCP/IP Model – 4 Layers

| Layer | Name              | Corresponds to OSI Layers          | Protocols                     |
|-------|-------------------|------------------------------------|-------------------------------|
| 4     | Application       | OSI Layers 5–7                     | HTTP, DNS, SMTP, SSH          |
| 3     | Transport         | OSI Layer 4                        | TCP, UDP                      |
| 2     | Internet          | OSI Layer 3                        | IP, ICMP, ARP                 |
| 1     | Network Access    | OSI Layers 1–2                     | Ethernet, Wi-Fi               |

---

## 🔹 3. OSI vs TCP/IP Comparison

| OSI Model (7 Layers) | TCP/IP Model (4 Layers) |
|----------------------|-------------------------|
| Application          | Application             |
| Presentation         | Application             |
| Session              | Application             |
| Transport            | Transport               |
| Network              | Internet                |
| Data Link            | Network Access          |
| Physical             | Network Access          |

---

## 🔹 4. DevOps Use Cases

| Tool       | OSI Layer | Purpose                              |
|------------|-----------|--------------------------------------|
| `ping`     | Layer 3   | Check host reachability              |
| `traceroute` | Layer 3 | Show packet route across networks    |
| `curl`     | Layer 7   | Fetch data from HTTP APIs            |
| `telnet`   | Layer 4   | Test TCP ports                       |
| `wireshark`| All       | Packet-level analysis                |
| `netstat`  | Layer 4   | Show open ports and connections      |

---
