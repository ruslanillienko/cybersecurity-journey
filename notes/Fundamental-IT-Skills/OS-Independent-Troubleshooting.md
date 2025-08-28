# OS-Independent Troubleshooting

## Common Symptoms
- Hardware issues: overheating, physical damage
- Software issues: slow performance, unresponsive UI
- Networking: connectivity drops, DNS errors, etc.

## Basic Troubleshooting Steps
1. **Identify the problem** — collect symptoms, reproduce, observe error messages.
2. **Research** — check forums, docs, vendor knowledge bases.
3. **Develop a plan** — start with non-invasive methods.
4. **Test** — implement and verify solution.
5. **Document** — record what worked or didn’t.

## Isolation Techniques
- Disconnect peripherals one by one
- Monitor CPU/RAM/Disk usage
- Review app/system configurations

## Networking Troubleshooting
- Check physical connections
- Validate IP config (e.g., `ip a`, `ipconfig`)
- Use tools: `ping`, `traceroute`, `nslookup`, `netstat`, etc.

## Log Analysis
- Identify relevant log files (e.g., `/var/log`, Event Viewer)
- Search for error codes or timestamps
- Use tools like `grep`, `less`, or GUI log viewers
