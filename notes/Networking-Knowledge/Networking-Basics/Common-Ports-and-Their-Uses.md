# Common Ports and Their Uses

Understanding common ports is fundamental for cybersecurity professionals, as many attacks target specific services via known ports. Ports are endpoints used by network protocols to establish communication between devices. Being familiar with them allows for proper firewall configuration, effective intrusion detection, and accurate threat assessment.

---

## Web and Browsing

| Port | Protocol | Description |
|------|----------|-------------|
| 80   | HTTP     | Used for unencrypted web traffic. Often targeted by attackers for injection or redirection. |
| 443  | HTTPS    | Secure version of HTTP using TLS/SSL encryption to protect transmitted data. |

---

## Secure Access

| Port | Protocol | Description |
|------|----------|-------------|
| 22   | SSH      | Secure Shell enables encrypted command-line access to remote systems. Commonly used by administrators and frequently scanned by attackers. |
| 3389 | RDP      | Remote Desktop Protocol for graphical remote access to Windows systems. Must be tightly controlled and monitored. |

---

## Email Services

| Port | Protocol | Description |
|------|----------|-------------|
| 25   | SMTP     | Sends emails between mail servers. Often exploited for spam if unsecured. |
| 110  | POP3     | Retrieves emails from a server, downloading them to the client. |
| 143  | IMAP     | Manages and retrieves emails without downloading them. More modern and flexible than POP3. |
| 587  | SMTP     | Secure submission of email from a client to a server. |

---

## File Transfer

| Port | Protocol | Description |
|------|----------|-------------|
| 20   | FTP (Data) | Transfers data for active FTP sessions. |
| 21   | FTP (Control) | Manages FTP session commands. Not encrypted by default, so insecure without FTPS. |
| 22   | SFTP     | FTP over SSH for secure file transfers. |
| 69   | TFTP     | Trivial FTP, often used for network booting. Lacks authentication, so risky. |

---

## Name Resolution and Directory Services

| Port | Protocol | Description |
|------|----------|-------------|
| 53   | DNS      | Resolves domain names to IP addresses. A critical service often targeted in DNS poisoning attacks. |
| 389  | LDAP     | Lightweight Directory Access Protocol, used for directory queries (e.g., Active Directory). |
| 636  | LDAPS    | LDAP over SSL for secure directory queries. |

---

## File Sharing (Windows)

| Port     | Protocol | Description |
|----------|----------|-------------|
| 137–139  | NetBIOS  | Legacy Windows file/printer sharing. Frequently exploited by malware and lateral movement. |
| 445      | SMB      | Modern file sharing, printer access, and interprocess communication. Widely used in ransomware attacks. |

---

## Databases

| Port  | Protocol          | Description |
|-------|-------------------|-------------|
| 1433  | Microsoft SQL     | Default port for Microsoft SQL Server. Must be protected to avoid data leaks. |
| 3306  | MySQL             | Default for MySQL databases. Needs strong authentication. |
| 1521  | Oracle DB         | Default for Oracle Database listeners. |
| 5432  | PostgreSQL        | Default PostgreSQL database port. |

---

## Network and System Management

| Port  | Protocol | Description |
|-------|----------|-------------|
| 161   | SNMP     | Used for collecting and organizing information about managed devices. Versions 1 and 2 are not secure. |
| 162   | SNMP Trap | Used to receive SNMP alerts. |
| 514   | Syslog   | Logging protocol used for sending system logs to a central server. |
| 123   | NTP      | Network Time Protocol for clock synchronization. Important for logs and security mechanisms. |

---

## VPN and Tunneling

| Port  | Protocol     | Description |
|-------|--------------|-------------|
| 500   | IPsec/IKE    | Used in VPN tunnels for key exchange. |
| 1701  | L2TP         | Layer 2 Tunneling Protocol, often paired with IPsec. |
| 1194  | OpenVPN      | Popular open-source VPN solution using its own protocol over UDP. |
| 443   | SSL VPN      | VPNs that tunnel traffic through HTTPS, useful for bypassing firewalls. |

---

## Why It Matters in Cybersecurity

- **Firewall Configuration:** Blocking or restricting unused ports reduces attack surface.
- **Port Scanning Detection:** Tools like Nmap can detect open ports and exposed services.
- **Threat Analysis:** Certain malware targets known ports (e.g., WannaCry exploited SMB on port 445).
- **Compliance:** Proper port management may be required by security standards like CIS, PCI-DSS, and ISO/IEC 27001.
