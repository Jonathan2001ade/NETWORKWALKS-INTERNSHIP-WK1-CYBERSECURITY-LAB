# 🔐 Cybersecurity Lab Setup Using VirtualBox and Kali Linux
# Training Program: Networkwalks
# Project: Week 1 — Cybersecurity and Penetration Testing Lab Setup

# 1. Project Overview

This project documents the configuration of a virtual networking environment using Oracle VirtualBox as part of my cybersecurity learning journey.

The objective is to establish a controlled virtual laboratory for learning network configuration, Linux networking, cybersecurity fundamentals, and authorized penetration testing.

The project includes configuring VirtualBox network settings, examining the available virtual networks, and preparing the environment for practical cybersecurity exercises.

# 2. Project Objectives

The objectives of this project are to:

* Configure VirtualBox networking.
* Examine the Host-only Network configuration.
* Create and configure a NAT Network.
* Understand IPv4 addressing and subnet masks.
* Review DHCP configuration.
* Prepare the environment for Kali Linux network testing.
* Document the configuration with technical evidence.

# 3. Tools and Technologies

| Tool                       | Purpose                                      |
| -------------------------- | -------------------------------------------- |
| Oracle VirtualBox          | Virtualization platform                      |
| Kali Linux                 | Operating system for cybersecurity learning  |
| VirtualBox Network Manager | Management of virtual network configurations |
| GitHub                     | Project documentation and evidence storage   |

# 4. Virtual Network Configuration

The following settings were observed in the VirtualBox Network Manager recording.

# A. Host-only Network

The Host-only Networks section displays a VirtualBox Host-Only Ethernet Adapter.

| Setting           | Observed Configuration                |
| ----------------- | ------------------------------------- |
| Network adapter   | VirtualBox Host-Only Ethernet Adapter |
| IPv4 address      | `192.168.56.1`                        |
| IPv4 network mask | `255.255.255.0`                       |
| DHCP server       | Enabled                               |

A Host-only Network allows communication between the host computer and appropriately configured virtual machines. It can also support communication between virtual machines connected to the same Host-only Network.

# B. NAT Network

The NAT Networks section displays a network named `NatNetwork`.

| Setting      | Observed Configuration |
| ------------ | ---------------------- |
| Network name | `NatNetwork`           |
| IPv4 prefix  | `10.0.0.0/24`          |
| DHCP         | Enabled                |
| IPv6         | Disabled               |

The configured IPv4 prefix, `10.0.0.0/24`, represents a network with the subnet mask `255.255.255.0`.

The enabled DHCP option allows VirtualBox to assign IPv4 addresses automatically to appropriately configured virtual machines connected to this NAT Network.

A NAT Network can provide outbound connectivity through network address translation when the virtual machine and host network are functioning correctly.

# 5. Understanding the Network Modes

### Host-only Network

This mode provides a virtual network between the host and connected virtual machines without automatically providing external network access.

# NAT Network

This mode allows appropriately configured virtual machines to communicate over the configured virtual network and can provide outbound connectivity through the host's network connection.

# Key Difference

The Host-only Network is useful for isolated host-to-VM communication, while a NAT Network can provide outbound connectivity and communication between connected virtual machines.

The appropriate configuration depends on the purpose of the cybersecurity laboratory.

# 6. Kali Linux Network Verification

The next stage is to verify the network configuration from inside Kali Linux.

The following commands can be used.

# Check Network Interfaces

```bash
ip a
```

This command displays network interfaces and their assigned IP addresses.

# Check the Routing Table

```bash
ip route
```

This command displays the configured network routes and default gateway, if available.

# Test IP Connectivity

```bash
ping -c 4 8.8.8.8
```

This command tests connectivity to an external IP address. The result depends on the configured network and internet access.

# Test DNS Resolution

```bash
nslookup example.com
```

This command checks whether the domain name can be resolved through the configured DNS service.

**Verification status:** These commands must be executed in Kali Linux, and their actual results must be recorded before connectivity and DNS testing can be reported as successful.

# 7. Project Evidence

The VirtualBox Network Manager recording provides evidence of the following configurations:

* The Host-only Ethernet Adapter and its IPv4 settings.
* The Host-only DHCP server status.
* The `NatNetwork` configuration.
* The NAT Network IPv4 prefix.
* The NAT Network DHCP setting.
* The IPv6 setting for the NAT Network.

Additional screenshots should be collected to document Kali Linux's network configuration, connectivity tests, DNS resolution, and virtual machine snapshots where applicable.

# 8. Key Lessons

This project demonstrates practical exposure to:

* Virtualization and virtual network management.
* IPv4 addressing and subnet masks.
* Host-only networking.
* NAT Network configuration.
* DHCP fundamentals.
* The distinction between different virtual network modes.
* Technical documentation and evidence collection.

# 9. Future Improvements

Planned improvements include:

* Verifying Kali Linux IP addressing and routing.
* Testing network connectivity and DNS resolution.
* Documenting the virtual machine's network adapter settings.
* Creating a clean virtual machine snapshot.
* Developing an isolated environment for authorized network scanning and vulnerability assessment.

# 10. Security and Ethical Considerations

The laboratory is intended for cybersecurity education and authorized security testing.

Future testing activities will be conducted only against systems owned by me or for which I have explicit permission.

# Conclusion

This project establishes a foundation for practical cybersecurity learning by documenting the virtual networking configurations available in Oracle VirtualBox.

The next stage is to verify Kali Linux connectivity, document the test results, and prepare the environment for further cybersecurity exercises.

**Project:** Cybersecurity Lab Setup
**Training Program:** Networkwalks
