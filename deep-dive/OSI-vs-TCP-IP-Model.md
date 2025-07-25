# OSI vs TCP/IP Model

Understanding the difference between the **OSI Model** and the **TCP/IP Model** is essential for grasping how modern computer networks operate. Both are conceptual frameworks used to describe how data is transmitted across a network, but they have different structures and use cases.

---

## Comparison Table

| OSI Model (7 Layers)     | TCP/IP Model (4 Layers)         | Description |
|--------------------------|----------------------------------|-------------|
| 7. Application           | 4. Application                   | Interface for user applications |
| 6. Presentation          | —                                | Data formatting, encryption |
| 5. Session               | —                                | Session management |
| 4. Transport             | 3. Transport                     | End-to-end communication, flow control |
| 3. Network               | 2. Internet                      | Routing and logical addressing |
| 2. Data Link             | 1. Network Access                | Physical addressing, error detection |
| 1. Physical              | 1. Network Access                | Media, signals, cables |

---

## OSI Model (7 Layers)

1. **Application** – User interface and services (HTTP, FTP)
2. **Presentation** – Data encryption and translation (SSL, TLS)
3. **Session** – Managing communication sessions
4. **Transport** – Ensuring reliable delivery (TCP, UDP)
5. **Network** – Routing and addressing (IP)
6. **Data Link** – MAC addressing and error control (Ethernet)
7. **Physical** – Hardware transmission (cables, hubs)

---

## TCP/IP Model (4 Layers)

1. **Application** – Combines OSI's Application, Presentation, Session (HTTP, DNS)
2. **Transport** – Responsible for data delivery (TCP, UDP)
3. **Internet** – Routing packets (IP, ICMP)
4. **Network Access** – Physical and data link functions (Ethernet, Wi-Fi)

---

## Practical Use

- **TCP/IP** is the **standard protocol suite** used in real-world networks, including the Internet.
- **OSI** is mainly used for **conceptual learning** and troubleshooting.

---

## Summary

| Aspect            | OSI Model        | TCP/IP Model   |
|------------------|------------------|----------------|
| Developed By     | ISO               | DARPA (US DoD) |
| Layers           | 7                 | 4              |
| Use Case         | Teaching, design  | Practical networking |
| Protocol Focus   | Protocol-independent | TCP/IP protocols only |
| Layer Separation | Clear distinction | Less separation, practical grouping |
