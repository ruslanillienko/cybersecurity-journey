# Understand the OSI Model

The **OSI (Open Systems Interconnection) Model** is a **conceptual framework** used to standardize the functions of a telecommunication or computing system into **seven distinct layers**. Each layer serves a specific purpose and communicates with the layers directly above and below it.

This model helps in **troubleshooting network issues**, **designing protocols**, and **understanding how data flows** through a network.

---

## OSI Model Layers

| Layer | Name         | Function                                                                          | Examples                                      |
|-------|--------------|-----------------------------------------------------------------------------------|-----------------------------------------------|
| 7     | Application   | Interface for end-user processes and applications                                | HTTP, FTP, SMTP, DNS                          |
| 6     | Presentation  | Data translation, encryption, compression                                         | SSL/TLS, JPEG, ASCII, EBCDIC                  |
| 5     | Session       | Manages sessions, connections, and dialogues                                     | NetBIOS, RPC, PPTP                            |
| 4     | Transport     | Ensures reliable data transfer with error checking and flow control              | TCP, UDP                                      |
| 3     | Network       | Logical addressing and path determination (routing)                              | IP, ICMP, IPSec, IGMP                         |
| 2     | Data Link     | Error detection/correction between nodes on the same network segment             | MAC, Ethernet, PPP, ARP                       |
| 1     | Physical      | Transmits raw bitstream over physical medium                                     | Cables, Hubs, Modems, RJ45, Fiber Optics     |

---

## How It Works

When data is sent from one device to another:

- It **moves down** the OSI layers at the sender's side, being **encapsulated** with headers/footers at each layer.
- At the receiver's side, data moves **up the layers**, where each layer **decapsulates** the corresponding information.

This layered approach helps isolate specific problems and simplifies protocol development.

---

## Usage in Cybersecurity

Understanding the OSI model is **critical for security professionals** because:

- **Threats can target specific layers** (e.g., DDoS at Layer 3/4, malware via Layer 7).
- **Security tools and defenses** are often built with specific OSI layers in mind (e.g., firewalls, intrusion detection systems).
- It helps in **analyzing logs**, **packet captures**, and **attack surfaces** more effectively.

---

> See also: [OSI vs TCP/IP Model](../../../deep-dive/OSI-vs-TCP-IP-Model.md)

