# CIDR (Classless Inter-Domain Routing)

CIDR is a method for allocating IP addresses and routing packets more efficiently than the older classful addressing system. Introduced in 1993, CIDR helps conserve IPv4 addresses and reduce routing table sizes by allowing variable-length subnet masks (VLSM).

## Background: The Problem with Classful Addressing

Previously, IP addresses were divided into fixed classes:

- **Class A** — 8 bits for network (≈16 million hosts)
- **Class B** — 16 bits for network (≈65,000 hosts)
- **Class C** — 24 bits for network (254 hosts)

This led to address waste. Many organizations didn’t need such large blocks but were still assigned them.

## What CIDR Does

CIDR replaces classful boundaries with **VLSM**, which allows custom subnet masks.

CIDR notation looks like this:
- `192.168.1.0/24`

- `192.168.1.0` is the network address
- `/24` is the **prefix length** — the number of bits reserved for the network portion

This means:
- Subnet mask: `255.255.255.0`
- Address range: `192.168.1.0 – 192.168.1.255`
- Usable hosts: `2⁸ – 2 = 254`

> CIDR enables efficient subnetting based on actual needs.

## Benefits of CIDR

- Better utilization of IP address space
- Smaller and more efficient routing tables
- Flexible network design and scaling

## CIDR vs Classful Addressing

| Address       | Classful Mask        | CIDR Mask | Hosts     |
|---------------|----------------------|-----------|-----------|
| 10.0.0.0      | Class A (255.0.0.0)   | /8        | ≈16M      |
| 192.168.1.0   | Class C (255.255.255.0) | /24     | 254       |
| 192.168.1.0   | –                    | **/26**   | **62**     |

## Common CIDR Blocks

| CIDR      | Subnet Mask         | # of IPs   |
|-----------|----------------------|------------|
| /8        | 255.0.0.0            | 16,777,216 |
| /16       | 255.255.0.0          | 65,536     |
| /24       | 255.255.255.0        | 256        |
| /30       | 255.255.255.252      | 4          |

## Extra Notes

- CIDR is used in both **IPv4** and **IPv6**
- It enables **route summarization** (aggregation of routes)
- It's fundamental in modern network planning and security

---
