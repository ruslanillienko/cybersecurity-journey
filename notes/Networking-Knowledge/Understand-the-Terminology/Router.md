# Router

A **router** is a networking device that directs data packets between different networks, ensuring they reach their intended destination. It operates at the **Network Layer (Layer 3)** of the OSI model and makes forwarding decisions based on the **IP addresses** of the source and destination devices.

Routers are critical for:

- **Connecting devices to the Internet** or linking multiple networks together.
- **Maintaining routing tables** to determine the most efficient path for data transmission.
- **Updating routes dynamically** using routing protocols such as:
  - **RIP** (Routing Information Protocol) – distance-vector based
  - **OSPF** (Open Shortest Path First) – link-state based
  - **BGP** (Border Gateway Protocol) – used for large-scale internet routing between autonomous systems.

## Core Functions

1. **Packet Forwarding**  
   Uses routing tables and algorithms to determine the best next hop for a data packet.

2. **Network Address Translation (NAT)**  
   Allows multiple devices on a private network to share a single public IP address, improving IP address efficiency and adding a layer of security by hiding internal IP addresses.

3. **DHCP Relay**  
   Forwards DHCP requests and responses between clients and a central DHCP server across networks.

4. **Firewall Integration**  
   Many routers have built-in firewall features, filtering unwanted traffic to protect against external threats.

5. **Wi-Fi Access Point Functionality**  
   Modern routers often provide wireless connectivity alongside wired Ethernet ports.

## Cybersecurity Considerations

Routers play a **frontline role in network defense**:

- **Default Credentials**: Many router breaches occur due to unchanged factory usernames/passwords.
- **Firmware Updates**: Outdated firmware can expose vulnerabilities.
- **Remote Management**: Should be disabled unless necessary, as it can be exploited by attackers.
- **Firewall Rules**: Misconfigured or overly permissive rules can allow malicious traffic.
- **Encryption for Wi-Fi**: WPA3 (or at least WPA2) should be enabled to secure wireless communications.
- **Logging and Monitoring**: Routers can log suspicious activity for forensic analysis.

## Router Attacks and Threats

- **Man-in-the-Middle (MITM)** via compromised routers
- **DNS Hijacking** – altering DNS settings to redirect traffic
- **Router Malware** – malicious firmware implants
- **Distributed Denial-of-Service (DDoS)** amplification attacks

## Best Practices for Secure Router Configuration

- Change default admin credentials immediately.
- Disable unnecessary services (e.g., UPnP, WPS, remote admin).
- Apply firmware updates regularly.
- Use strong Wi-Fi encryption (WPA3).
- Restrict administrative access to specific IP ranges.
- Enable firewall and intrusion prevention features.

---

**References:**
- RFC 1812 – Requirements for IP Version 4 Routers
- NIST SP 800-41 – Guidelines on Firewalls and Router Security
- OWASP Secure Network Architecture Guidelines
