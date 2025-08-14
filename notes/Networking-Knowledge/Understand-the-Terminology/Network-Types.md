# Network Types (MAN, LAN, WAN, WLAN)

## 1. LAN (Local Area Network)
A **Local Area Network (LAN)** is a network that covers a small geographic area, such as a home, office, or small group of buildings.  
- **Range**: Typically up to a few hundred meters.  
- **Ownership**: Usually owned, managed, and maintained by a single organization or individual.  
- **Speed**: High data transfer rates (often 100 Mbps to 10 Gbps or more).  
- **Technologies**: Ethernet, Wi-Fi.  
- **Security Considerations**:  
  - Physical access control is important since devices are in close proximity.  
  - Use of VLANs to segment sensitive systems.  
  - Strong authentication for wireless access (WPA3).  

---

## 2. MAN (Metropolitan Area Network)
A **Metropolitan Area Network (MAN)** spans a city or a large campus, connecting multiple LANs within the same geographic area.  
- **Range**: Several kilometers to tens of kilometers.  
- **Ownership**: Can be owned by a single organization or leased from a telecommunications provider.  
- **Speed**: High-speed connections (often fiber-based).  
- **Technologies**: Metro Ethernet, MPLS, fiber optics.  
- **Security Considerations**:  
  - Data encryption in transit to prevent interception.  
  - Provider trust and SLA (Service Level Agreement) verification.  
  - Redundancy to protect against outages.  

---

## 3. WAN (Wide Area Network)
A **Wide Area Network (WAN)** connects networks over large geographic distances, often across countries or continents.  
- **Range**: Potentially global.  
- **Ownership**: Infrastructure often owned by multiple service providers.  
- **Speed**: Varies from Mbps to Gbps depending on links and technology.  
- **Technologies**: MPLS, SD-WAN, leased lines, satellite links.  
- **Security Considerations**:  
  - End-to-end encryption (IPsec, TLS).  
  - Secure tunneling (VPN) to protect data over public infrastructure.  
  - Strong access control to WAN edge devices (firewalls, routers).  

---

## 4. WLAN (Wireless Local Area Network)
A **Wireless Local Area Network (WLAN)** is a type of LAN that uses wireless technology (usually Wi-Fi) instead of cables.  
- **Range**: Typically 30–100 meters indoors, more outdoors with line of sight.  
- **Ownership**: Usually owned and controlled by the organization or individual.  
- **Speed**: Depends on Wi-Fi standards (e.g., Wi-Fi 5: up to ~3.5 Gbps, Wi-Fi 6: up to ~9.6 Gbps).  
- **Technologies**: IEEE 802.11 standards.  
- **Security Considerations**:  
  - WPA3 encryption to secure communications.  
  - Disable WPS to avoid brute-force attacks.  
  - MAC address filtering for device-level control.  
  - Rogue access point detection.  

---

## Summary Table

| Network Type | Range            | Technology Examples   | Common Security Practices |
|--------------|------------------|-----------------------|---------------------------|
| **LAN**      | Small building   | Ethernet, Wi-Fi       | VLANs, WPA3, access control |
| **MAN**      | City-wide        | Metro Ethernet, MPLS  | Encryption, redundancy     |
| **WAN**      | Global           | SD-WAN, IPsec         | VPNs, TLS, firewalls       |
| **WLAN**     | 30–100 m         | IEEE 802.11 Wi-Fi     | WPA3, disable WPS, MAC filtering |

---

