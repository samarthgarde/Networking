# 04 – DNS (Domain Name System)

DNS (Domain Name System) is a critical component of networking. It translates human-readable domain names (like `google.com`) into IP addresses (like `142.250.182.206`) that computers use to identify each other.

---

## 🔹 1. What is DNS?

DNS works like the **"phonebook of the internet"**.  
Instead of remembering IP addresses, users type domain names.

---

## 🔹 2. How DNS Works

When you type a website like `example.com`, the process looks like this:

1. **Browser Cache**: Checks local DNS cache
2. **OS Resolver**: OS checks `/etc/hosts` (Linux/Mac) or local DNS cache
3. **DNS Server**: Queries recursive DNS resolver (usually provided by ISP or Google)
4. **Root Server**: Points to TLD servers (.com, .org, etc.)
5. **TLD Server**: Points to authoritative DNS server for domain
6. **Authoritative Server**: Returns final IP for domain

---

## 🔹 3. DNS Record Types

| Record Type | Purpose                                | Example                        |
|-------------|-----------------------------------------|--------------------------------|
| A           | Maps domain to IPv4 address             | `example.com → 93.184.216.34`  |
| AAAA        | Maps domain to IPv6 address             | `example.com → ::1`            |
| CNAME       | Alias one domain to another             | `www.example.com → example.com`|
| MX          | Mail server for domain                  | Mail goes to `mail.example.com`|
| TXT         | Text data, often for verification (SPF, DKIM) | Google site verification |
| NS          | Name servers for the domain             | `ns1.example.com`              |

---

## 🔹 4. DevOps Use Cases for DNS

| Use Case                        | Description                                     |
|----------------------------------|-------------------------------------------------|
| Load Balancing (Round-robin DNS)| Distribute traffic across multiple IPs          |
| Custom Domains for Apps         | Assign `myapp.company.com` to app service       |
| Service Discovery               | Internal DNS resolves service names             |
| SSL Certificates                | TXT records used for domain verification        |

---

## 🔹 5. DNS Tools (Linux CLI)

### 🧪 `dig` – DNS Query Tool
```bash
dig example.com
dig +short google.com
