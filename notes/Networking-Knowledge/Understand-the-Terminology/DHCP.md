# DHCP (Dynamic Host Configuration Protocol)

**Dynamic Host Configuration Protocol (DHCP)** is a network protocol used to automatically assign **IP addresses** and other network configuration parameters to devices on a network.

## Purpose

DHCP simplifies network management by dynamically assigning:
- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

It eliminates the need for manual IP configuration and prevents IP address conflicts.

## How DHCP Works

1. **DHCP Discover**: Client broadcasts a request to find available DHCP servers.
2. **DHCP Offer**: Server responds with an available IP and configuration options.
3. **DHCP Request**: Client requests to use the offered IP.
4. **DHCP Acknowledgment (ACK)**: Server confirms the lease and assigns the IP.

```
Client → [DHCPDISCOVER] → Broadcast
Server → [DHCPOFFER] → Client
Client → [DHCPREQUEST] → Server
Server → [DHCPACK] → Client
```

## Lease Concept

- IP addresses are leased for a specific **duration**.
- Clients must renew the lease periodically to keep using the IP.

## DHCP Components

| Component     | Description                                 |
|---------------|---------------------------------------------|
| DHCP Server   | Assigns IPs and configuration settings      |
| DHCP Client   | Requests and receives network configuration |
| DHCP Relay    | Forwards requests across subnets            |

## Advantages

- **Automation**: No manual configuration needed
- **Conflict Avoidance**: Centralized IP address management
- **Scalability**: Ideal for large dynamic networks
- **Flexibility**: Easily change network settings without reconfiguring each device

## Security Considerations

- Unauthorized DHCP servers (Rogue DHCP) can mislead clients
- Mitigations:
  - DHCP snooping on switches
  - IP source guard

## Real-World Applications

- Home and enterprise networks
- Wi-Fi hotspots
- Cloud virtual networks

---

