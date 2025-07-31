# Public vs Private IP Addresses

Understanding the difference between **public** and **private IP addresses** is essential in networking and cybersecurity. These two types of addresses play distinct roles in how devices communicate within local networks and across the internet.

---

## Public IP Addresses

**Public IP addresses** are globally unique and assigned by your Internet Service Provider (ISP). They are routable over the **public internet**, allowing external devices and services to reach your system directly.

### Characteristics:
- Assigned by **IANA** or **RIRs** (e.g., ARIN, RIPE)
- **Globally unique**
- Routable over the internet
- Required for **web servers**, **email servers**, **VPN gateways**, etc.

### Example:
- `8.8.8.8` (Google DNS)
- `104.26.10.78` (example.com web server)

### Risks:
- Exposes devices to the internet
- Must be secured with firewalls, encryption, and monitoring

---

## Private IP Addresses

**Private IP addresses** are reserved for use within **local area networks (LANs)**. They are **not routable** over the internet and are used to facilitate communication among devices within a private environment (home, office, data center, etc.).

### Private IP Ranges (RFC 1918):
| Class | Range | CIDR Notation |
|-------|-------|----------------|
| A     | 10.0.0.0 – 10.255.255.255 | `10.0.0.0/8`  |
| B     | 172.16.0.0 – 172.31.255.255 | `172.16.0.0/12` |
| C     | 192.168.0.0 – 192.168.255.255 | `192.168.0.0/16` |

### Example:
- `192.168.1.1` (home router)
- `10.0.0.5` (internal server)

### Used For:
- Internal network segmentation
- IP address conservation
- Enhanced privacy through **NAT**

---

## NAT (Network Address Translation)

Because private addresses are not valid on the public internet, **NAT** is used to translate private IPs into a public IP when accessing external services.

### Benefits of NAT:
- Allows many devices to share a single public IP
- Adds a layer of obscurity from external scans
- Reduces IPv4 address exhaustion

---

## Quick Comparison

| Feature                | Public IP                     | Private IP                     |
|------------------------|-------------------------------|-------------------------------|
| Visibility             | Globally visible              | Only within local network      |
| Uniqueness             | Must be unique worldwide      | Can be reused in different LANs|
| Assigned By            | ISP or RIR                    | Network administrator or DHCP  |
| Internet Access        | Direct                        | Requires NAT                   |
| Security               | Needs strong protection       | More isolated by design        |

---
