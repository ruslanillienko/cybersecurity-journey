# VLAN (Virtual Local Area Network)

A **Virtual Local Area Network (VLAN)** is a logical segmentation of a physical network. It allows multiple isolated broadcast domains to coexist on the same physical infrastructure by grouping devices based on function, department, or application—regardless of their physical location.

## Key Benefits

- **Security**: Isolates sensitive traffic from the rest of the network
- **Performance**: Reduces broadcast traffic and congestion
- **Flexibility**: Enables easier reconfiguration without changing physical cabling
- **Manageability**: Simplifies administration in large networks

## How It Works

VLANs are implemented at the **switch** level using the **IEEE 802.1Q** standard, which inserts a VLAN tag into Ethernet frames to indicate VLAN membership.

Example:

```
Frame with VLAN Tag:
[Ethernet Header | 802.1Q Tag | Payload | CRC]
```

A single switch can handle multiple VLANs and isolate their traffic logically.

## Use Case Examples

| VLAN ID | Department       | Purpose               |
|---------|------------------|-----------------------|
| 10      | Finance          | Isolate sensitive data|
| 20      | HR               | Limit access to payroll systems |
| 30      | Guest Wi-Fi      | Separate guest devices from internal resources |

## Trunk vs Access Ports

- **Access Port**: Belongs to one VLAN and connects to end devices (PCs, printers)
- **Trunk Port**: Carries multiple VLANs between switches using 802.1Q tagging

## VLAN and Routing

Devices in different VLANs **cannot communicate directly** without a **Layer 3 device** (like a router or L3 switch). This process is known as **Inter-VLAN Routing**.

## Real-World Use Cases

- Segmenting traffic in universities, hospitals, and offices
- Isolating IoT devices from core infrastructure
- Supporting multi-tenant environments in data centers

---

