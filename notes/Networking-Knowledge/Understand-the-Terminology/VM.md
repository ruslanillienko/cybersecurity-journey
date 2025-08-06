# VM (Virtual Machine)

A **Virtual Machine (VM)** is a software-based emulation of a physical computer. It runs its own operating system and applications in an isolated environment, separate from the underlying physical hardware.

## Key Characteristics

- **Emulated Hardware**: Virtual CPU, memory, disk, and network interface
- **Guest OS**: Each VM runs a full operating system independently
- **Isolation**: One VM cannot directly affect another or the host
- **Portability**: VMs can be moved, copied, or restored easily

## How It Works

A **hypervisor** (also known as a Virtual Machine Monitor or VMM) manages multiple VMs on a single physical machine (host).

### Types of Hypervisors

| Type        | Description                                 | Examples                      |
|-------------|---------------------------------------------|-------------------------------|
| Type 1      | Runs directly on hardware (bare-metal)      | VMware ESXi, Microsoft Hyper-V|
| Type 2      | Runs on top of an OS (hosted)               | VirtualBox, VMware Workstation|

## Example Use Case

A developer can run:
- Windows 11 on the host machine
- Ubuntu Linux as a VM for testing
- Legacy Windows XP VM for compatibility testing

## Benefits

- **Efficient Resource Usage**: Multiple VMs on one machine
- **Snapshots & Rollbacks**: Easy state recovery
- **Security**: Isolation prevents malware from escaping the VM
- **Cloud Enablement**: Basis for IaaS in cloud computing

## Real-World Applications

- Cloud platforms (e.g., AWS EC2, Azure VMs)
- Software development and testing
- Training labs and cybersecurity exercises
- Legacy application hosting

