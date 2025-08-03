# Default Gateway

A **default gateway** is a network node—usually a **router** or **firewall**—that acts as the access point between a local network and external networks, such as the internet.

## Purpose

When a device on a local subnet wants to communicate with a device outside its own subnet (e.g., visiting a website or sending an email), it forwards the traffic to the default gateway. The gateway then determines the best path to the destination.

## How It Works

- Devices on the local network are configured with the IP address of the default gateway.
- If the destination IP is not part of the local subnet, the data is sent to the gateway.
- The gateway forwards the data to the next hop, such as an ISP or external router.

Example:

```
Device IP:          192.168.1.10
Subnet Mask:        255.255.255.0
Default Gateway:    192.168.1.1
```

If `192.168.1.10` wants to access `8.8.8.8`, it sends the packet to `192.168.1.1`.

## Key Functions

- Acts as a **traffic director** between internal and external networks
- Provides **routing** for devices that are not aware of how to reach other networks
- Serves as a point for **security policies** and **NAT (Network Address Translation)**

## Importance

- Enables internet access from local networks
- Central to configuring routers, firewalls, and DHCP servers
- Essential for proper **routing** and **network segmentation**

## Real-World Use Cases

- Home routers serving as gateways to ISPs
- Corporate firewalls acting as secure gateways to the internet
- Multi-router setups where one node acts as the default path to the outside
