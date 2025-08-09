# Switch

A **switch** is a network device that operates primarily at the **Data Link Layer (Layer 2)** of the OSI model, although some advanced switches (Layer 3 switches) also perform routing functions. Its main role is to connect multiple devices within a **Local Area Network (LAN)** and efficiently forward data frames between them.

## How It Works
Switches use **MAC addresses** to identify devices on the network. When a data frame arrives at a switch port, the switch:
1. Reads the **source MAC address** and stores it in its MAC address table along with the port number.
2. Looks up the **destination MAC address** in the table.
3. Forwards the frame only to the specific port where the destination device is connected, rather than broadcasting to all ports.

This targeted forwarding:
- **Reduces unnecessary traffic**.
- **Prevents collisions** by creating separate **collision domains** for each port.
- Supports **full-duplex communication**, allowing simultaneous sending and receiving of data.

## Key Features
- **VLAN Support** – Allows logical segmentation of networks for better security and traffic management.
- **Port Mirroring** – Copies network traffic from one port to another for monitoring and analysis.
- **Quality of Service (QoS)** – Prioritizes certain types of traffic (e.g., VoIP or video streaming).
- **Link Aggregation** – Combines multiple network links to increase bandwidth and provide redundancy.

## Security Considerations
Switches are critical in network security because they control how devices communicate within a LAN. Common security measures include:
- **Port Security** – Limits the number of devices that can connect to a port by MAC address.
- **802.1X Authentication** – Requires user/device authentication before granting network access.
- **DHCP Snooping** – Prevents rogue DHCP servers from assigning malicious IP addresses.
- **Dynamic ARP Inspection (DAI)** – Protects against ARP spoofing attacks.
- **Private VLANs (PVLAN)** – Restrict communication between devices in the same VLAN.

## Role in Cybersecurity
While switches help segment and secure networks, they are also targets for attacks such as:
- **MAC Flooding** – Overloading the MAC address table to force the switch into broadcasting mode.
- **VLAN Hopping** – Exploiting misconfigured VLANs to gain unauthorized access to other network segments.
- **ARP Spoofing** – Manipulating ARP tables to intercept traffic.

**Best Practices:**
- Keep firmware up-to-date.
- Disable unused ports.
- Use strong VLAN configurations.
- Enable monitoring and logging for suspicious activity.

## Summary
Switches are fundamental to building efficient, scalable, and secure network infrastructures. With proper configuration and security controls, they not only improve performance but also strengthen the network’s defense against internal threats.

---

