# Subnet Mask

A **subnet mask** is a 32-bit number used in IP networking to divide an IP address into two parts: the **network portion** and the **host portion**. It plays a key role in defining how IP addresses are interpreted within a network.

## Purpose

Subnet masks allow the creation of **subnetworks (subnets)** within a larger network, enabling:

- Efficient IP address allocation
- Better network segmentation
- Reduced broadcast traffic
- Improved security and performance

## How It Works

A subnet mask works by masking the IP address to identify the network portion. Each `1` in the subnet mask represents a bit belonging to the network; each `0` represents a bit belonging to the host.

Example:

```
IP Address:     192.168.1.10
Subnet Mask:    255.255.255.0  (/24)

Binary:
IP:             11000000.10101000.00000001.00001010
Mask:           11111111.11111111.11111111.00000000
```

The first 24 bits define the network, the last 8 bits define the host.

## Common Subnet Masks

| CIDR | Subnet Mask       | # of Hosts | Notes               |
|------|--------------------|------------|---------------------|
| /8   | 255.0.0.0          | 16,777,214 | Very large networks |
| /16  | 255.255.0.0        | 65,534     | Medium-sized        |
| /24  | 255.255.255.0      | 254        | Common for LANs     |
| /30  | 255.255.255.252    | 2          | Point-to-point links|

> Remember: the number of usable hosts is always **2 less** than the total number of addresses in a subnet (network + broadcast are reserved).

## Why It Matters

- **Configuration**: Required when setting up IP interfaces
- **Troubleshooting**: Helps identify issues with routing and communication
- **Security**: Enables logical network segmentation
- **Scalability**: Supports organized IP management for growth

## Real-World Use Cases

- Dividing a corporate network into departments
- Isolating IoT devices or guests from internal infrastructure
- Allocating minimal addresses for router-to-router connections

---

