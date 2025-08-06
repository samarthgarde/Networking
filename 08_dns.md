# 08 – DNS & Name Resolution

**DNS (Domain Name System)** translates human-readable domain names (like `google.com`) into IP addresses (like `142.250.192.78`), enabling browsers, servers, and tools to locate each other over the internet.

---

## 🔹 1. Why DNS Matters for DevOps

- Resolves domain names to IPs for servers, APIs, endpoints
- Critical in Kubernetes (Service Discovery)
- Used in CI/CD pipelines to access cloud or SaaS endpoints
- Important for monitoring, debugging, and DNS-based routing (CDNs, Load Balancers)

---

## 🔹 2. How DNS Works

### Example: Visiting `example.com`

1. Client checks **local DNS cache**
2. If not found → asks **configured DNS resolver** (ISP or public like 8.8.8.8)
3. Resolver queries:
   - **Root DNS servers** → direct to
   - **TLD servers (.com)** → direct to
   - **Authoritative DNS server** of `example.com`
4. IP is returned → browser connects to it

---

## 🔹 3. DNS Record Types

| Record Type | Purpose                           | Example                    |
|-------------|-----------------------------------|----------------------------|
| A           | Maps domain → IPv4 address        | `example.com → 192.0.2.1`  |
| AAAA        | Maps domain → IPv6 address        |                            |
| CNAME       | Alias for another domain          | `www → example.com`        |
| MX          | Mail server for the domain        |                            |
| TXT         | Text data (SPF, DKIM, verifications) |                        |
| NS          | Nameserver for the domain         |                            |
| SRV         | Service record (used in SIP, etc) |                            |

---

## 🔹 4. Common DNS Tools

```bash
# Linux/Mac
nslookup example.com

dig example.com

host example.com

# Windows
nslookup example.com

# Get authoritative answer
dig @8.8.8.8 example.com +trace

# Show DNS records (A, MX, TXT)
dig example.com ANY

