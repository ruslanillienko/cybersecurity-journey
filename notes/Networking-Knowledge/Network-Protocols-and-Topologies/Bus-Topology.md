# Bus Topology

A **bus topology** is a network configuration where all devices (nodes) share a single communication line (the "bus"). In computing, the concept of a **bus** also extends to internal system communication between components (e.g., CPU, memory, peripherals).  

From a **cybersecurity perspective**, bus systems represent both **legacy network structures** and **critical data channels** inside computers that require strong protection.

---

## Key Characteristics
- **Single communication line** – all nodes connect to the same backbone cable.  
- **Shared medium** – only one device can transmit at a time.  
- **Termination required** – both ends of the bus must be terminated to prevent signal reflection.  
- **Simple and cost-effective** – requires less cabling compared to star or mesh.  

---

## Advantages
- **Cost-efficient** – minimal cabling required.  
- **Easy to set up** – especially in small networks.  
- **Scalability (to a point)** – new devices can be added without major changes.  

---

## Disadvantages
- **Single point of failure** – if the backbone fails, the entire network stops.  
- **Difficult troubleshooting** – identifying faults can be challenging.  
- **Limited performance** – collisions and bandwidth sharing reduce efficiency.  
- **Obsolete in modern networks** – rarely used today outside specific scenarios.  

---

## Cybersecurity Perspective

### Risks in Network Bus Topologies
- **Eavesdropping** – all data passes through the shared bus, making sniffing easier.  
- **Denial of Service (DoS)** – a compromised device can flood the bus, disrupting communication.  
- **Injection attacks** – attackers can insert malicious packets into the shared medium.  
- **Physical tampering** – access to the backbone cable allows interception or manipulation.  

### Risks in Computer Architecture Buses
- **DMA (Direct Memory Access) attacks** – malicious devices on expansion buses can read/write memory directly.  
- **Side-channel attacks** – monitoring bus signals (timing, power) may leak sensitive information.  
- **Firmware-level exploits** – vulnerable peripheral buses (e.g., PCI, USB, Thunderbolt) can be abused.  

---

## Best Practices for Security
- **Encryption** – protect data transmitted over buses, especially external ones (USB, PCIe).  
- **Access control** – restrict which devices can connect to system buses.  
- **Bus isolation** – separate critical systems from non-trusted peripherals.  
- **Monitoring** – use intrusion detection to identify unusual bus activity.  
- **Physical security** – prevent unauthorized physical access to backbone cables or system internals.  

---

## Common Use Cases
- **Legacy LANs** – early Ethernet implementations used bus topology.  
- **System architecture** – CPU ↔ memory ↔ peripherals still rely on bus concepts.  
- **Peripheral expansion** – USB, PCIe, and Thunderbolt are modern examples of bus systems.  

---

**Summary:**  
Bus topology is largely outdated in networking but remains fundamental in **computer system design**. From a cybersecurity perspective, buses are **high-value attack surfaces** — whether as a shared backbone in networks or as internal communication channels (PCI, USB, DMA). Protecting buses with **encryption, access controls, and monitoring** is critical to maintaining the **integrity and confidentiality** of modern systems.


