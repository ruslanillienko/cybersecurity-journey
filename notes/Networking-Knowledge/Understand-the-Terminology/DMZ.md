# DMZ (Demilitarized Zone)

A **DMZ (Demilitarized Zone)** is a physical or logical subnetwork that separates an organization's internal, trusted network from untrusted external networks, such as the internet.

## Purpose

The main goal of a DMZ is to **add an additional layer of security** by isolating publicly accessible services from the internal network. It acts as a buffer zone, limiting access to internal resources even if the DMZ is compromised.

## Key Concepts

- **Isolation**: Internal network remains protected even if the DMZ is breached
- **Controlled Access**: Only specific services (e.g., web, mail, DNS) are exposed to the public
- **Traffic Filtering**: Firewalls control incoming and outgoing traffic between each zone

## Typical Architecture

```
[ Internet ]
     |
 [External Firewall]
     |
   [ DMZ ]
     |
 [Internal Firewall]
     |
[ Internal Network ]
```

- **DMZ** hosts systems like:
  - Web servers
  - Mail servers
  - FTP servers
  - DNS servers

## Security Design

- **Two-firewall model**: Separate firewalls for external and internal access
- **One-firewall model**: Single firewall with three interfaces (WAN, DMZ, LAN)
- **Strict rules**: Internal systems never initiate traffic to DMZ or internet directly

## Real-World Use Cases

- Hosting public-facing web applications
- Providing secure access to corporate services for remote users
- Isolating third-party services that require internet connectivity

---

