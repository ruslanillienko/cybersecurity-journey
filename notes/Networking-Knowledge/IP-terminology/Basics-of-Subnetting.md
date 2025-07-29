# Basics of Subnetting

**Subnetting** is a fundamental networking technique used to divide a large IP network into smaller, more efficient and manageable segments called **subnets**. It plays a critical role in network design, performance optimization, and security management.

---

## What is Subnetting?

Subnetting involves partitioning a network's IP address space into multiple **smaller subnetworks**, each with its own **range of IP addresses**. This allows network administrators to:

- Reduce network congestion
- Improve routing efficiency
- Enhance network security
- Allocate IP addresses more effectively

---

## Key Concepts

### ➤ Network and Host Portions

An **IP address** is made up of two components:
- **Network portion** – identifies the specific network
- **Host portion** – identifies the specific device (host) within that network

### ➤ Subnet Mask

A **subnet mask** defines where the network portion ends and the host portion begins. For example:

- `255.255.255.0` → `/24` in CIDR notation  
- Network portion: first 24 bits  
- Host portion: remaining 8 bits

Changing the subnet mask allows administrators to create multiple subnets, each with a different number of available hosts.

---

## Why Subnetting Matters

### Benefits:
- **Scalability**: Easily scale your network by adding subnets
- **Security**: Segment sensitive departments (e.g., HR, Finance)
- **Reduced Broadcast Domains**: Limits broadcast traffic to within subnets
- **Efficient IP Usage**: Prevents IP address waste

### Without Subnetting:
- All devices would share one broadcast domain
- Increased traffic and security risks
- Poor performance in large networks

---

## Example: Subnetting a /24 Network

Given IP block: `192.168.1.0/24`  
Total addresses: 256 (including network and broadcast)

Split into **4 subnets** using a `/26` mask:

| Subnet | Range              | Host Range         | Broadcast Address |
|--------|--------------------|--------------------|-------------------|
| 1      | 192.168.1.0/26     | .1 – .62            | 192.168.1.63       |
| 2      | 192.168.1.64/26    | .65 – .126          | 192.168.1.127      |
| 3      | 192.168.1.128/26   | .129 – .190         | 192.168.1.191      |
| 4      | 192.168.1.192/26   | .193 – .254         | 192.168.1.255      |

Each subnet supports up to **62 usable hosts**.

---

## Use Cases

- **Enterprise networks**: Isolate departments or teams
- **Network security**: Limit access between subnets via firewalls
- **Data centers**: Allocate different VLANs to virtual machines
- **Home labs**: Practice IP planning and segmentation

---
