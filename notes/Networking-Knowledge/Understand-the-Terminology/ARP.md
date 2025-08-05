# ARP (Address Resolution Protocol)

**Address Resolution Protocol (ARP)** is a network protocol used to map an IP address to a corresponding **MAC address** (hardware address) within a Local Area Network (LAN). It enables devices to communicate by resolving logical IP addresses into physical addresses required for data transmission.

## Why ARP Is Needed

Devices use IP addresses to identify each other on a network, but actual data transfer at the data link layer (Layer 2) requires MAC addresses. ARP bridges this gap.

## How ARP Works

1. A device wants to send data to another IP address on the LAN.
2. It checks its **ARP cache** to see if it already knows the corresponding MAC address.
3. If not, it sends out an **ARP Request** (broadcast) asking:  
   > "Who has IP address X.X.X.X? Tell me your MAC."
4. The device with that IP responds with an **ARP Reply** containing its MAC address.
5. The original device updates its ARP cache and sends the data to the resolved MAC.

## ARP Packet Types

- **ARP Request**: Broadcasted to all devices on the LAN
- **ARP Reply**: Sent directly back to the requester

## ARP Cache

The ARP cache stores recent mappings of IP addresses to MAC addresses to reduce overhead. These entries time out after a set period or can be cleared manually.

## Example

```
IP: 192.168.1.10 → needs MAC for 192.168.1.20
→ ARP Request: "Who has 192.168.1.20?"
→ 192.168.1.20 replies: "My MAC is 00:1A:2B:3C:4D:5E"
→ Cache updated, data sent to 00:1A:2B:3C:4D:5E
```

## Security Considerations

- **ARP Spoofing/Poisoning**: An attacker sends fake ARP replies to redirect traffic to themselves (Man-in-the-Middle).
- Mitigations:
  - Dynamic ARP Inspection (DAI)
  - Static ARP entries
  - Packet filtering rules

## Real-World Use Cases

- Internal network communication
- MAC address resolution in IPv4 networks
- Network troubleshooting with tools like `arp -a`, `arping`, `wireshark`

---
# ARP (Address Resolution Protocol)

**Address Resolution Protocol (ARP)** is a network protocol used to map an IP address to a corresponding **MAC address** (hardware address) within a Local Area Network (LAN). It enables devices to communicate by resolving logical IP addresses into physical addresses required for data transmission.

## Why ARP Is Needed

Devices use IP addresses to identify each other on a network, but actual data transfer at the data link layer (Layer 2) requires MAC addresses. ARP bridges this gap.

## How ARP Works

1. A device wants to send data to another IP address on the LAN.
2. It checks its **ARP cache** to see if it already knows the corresponding MAC address.
3. If not, it sends out an **ARP Request** (broadcast) asking:  
   > "Who has IP address X.X.X.X? Tell me your MAC."
4. The device with that IP responds with an **ARP Reply** containing its MAC address.
5. The original device updates its ARP cache and sends the data to the resolved MAC.

## ARP Packet Types

- **ARP Request**: Broadcasted to all devices on the LAN
- **ARP Reply**: Sent directly back to the requester

## ARP Cache

The ARP cache stores recent mappings of IP addresses to MAC addresses to reduce overhead. These entries time out after a set period or can be cleared manually.

## Example

```
IP: 192.168.1.10 → needs MAC for 192.168.1.20
→ ARP Request: "Who has 192.168.1.20?"
→ 192.168.1.20 replies: "My MAC is 00:1A:2B:3C:4D:5E"
→ Cache updated, data sent to 00:1A:2B:3C:4D:5E
```

## Security Considerations

- **ARP Spoofing/Poisoning**: An attacker sends fake ARP replies to redirect traffic to themselves (Man-in-the-Middle).
- Mitigations:
  - Dynamic ARP Inspection (DAI)
  - Static ARP entries
  - Packet filtering rules

## Real-World Use Cases

- Internal network communication
- MAC address resolution in IPv4 networks
- Network troubleshooting with tools like `arp -a`, `arping`, `wireshark`

---

