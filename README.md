# Home Enterprise Lab — Joel Shaffer

A self-built, enterprise-style home network and storage environment designed for hands-on experience in systems administration, network engineering, security monitoring, and infrastructure management.

## Overview

| Component | Technology |
|---|---|
| NAS / Storage Server | Dell PowerEdge R420 - TrueNAS SCALE |
| Storage Pool | ZFS - Mirrored vdevs - ~7TB usable |
| Network Core | Managed Cisco Switch - VLAN segmentation |
| DNS Filtering | Pi-hole |
| Firewall | Raspberry Pi custom firewall |
| SIEM / Logging | Splunk |
| OS Platforms | Windows, Rocky Linux, Kali Linux |

## Server and Storage

- Server: Dell PowerEdge R420 (4-bay rack server)
- Boot Drive: SATA SSD (migrated from failed USB boot)
- Storage: 4x HDDs — ~14TB raw, ~7TB usable
- RAID Controller: Dell PERC H310
- Pool: vault1 — 2x mirrored vdevs (RAID10-equivalent)
- Usable Capacity: ~7TB — Health: ONLINE
- Migrated from TrueNAS CORE to TrueNAS SCALE
- Resolved NFSv4 ACL vs POSIX permission conflicts
- Fixed Windows SMB credential caching issues

## Network Architecture

- Fully hardwired home network with managed Cisco switch
- VLAN segmentation across management, servers, and devices
- Trunk ports configured across primary and secondary switches
- IPv4 subnetting, DNS/DHCP, port forwarding and NAT
- VPN and remote access, email server configuration
- Geolocation and IP routing troubleshooting
- Wi-Fi and mesh diagnostics, Wireshark packet analysis

## Security Stack

- Pi-hole: network-wide DNS sinkhole for ad and tracker blocking
- Raspberry Pi custom firewall with iptables traffic filtering
- Splunk SIEM: log ingestion, monitoring, alert triage, SPL dashboards

## SMB File Services

- Per-user datasets with NFSv4 ACL isolation (least privilege)
- Shared datasets for collaborative access (Media, UHT)
- Windows credential-based SMB authentication

## Enterprise Concepts Applied

| Concept | Implementation |
|---|---|
| Network segmentation | VLAN design across managed switches |
| Least privilege | Per-user NFSv4 ACL isolation |
| Redundant storage | ZFS mirrored vdev pool |
| Centralized file services | TrueNAS SMB multi-user shares |
| DNS filtering | Pi-hole network-wide sinkhole |
| Log monitoring | Splunk SIEM with dashboards |
| Firewall hardening | Raspberry Pi custom traffic filtering |

## Roadmap

- Convert PERC H310 to IT mode for true ZFS passthrough
- ZFS snapshots and automated replication
- Full Splunk stack with custom detection rules
- NetFlow / SNMP network monitoring
- Proxmox hypervisor for VM workloads
- Active Directory / LDAP integration

## Skills and Technologies

TrueNAS SCALE | ZFS | SMB | NFSv4 ACLs | Splunk | Pi-hole | Cisco IOS | VLANs | Trunking | IPv4 Subnetting | DNS/DHCP | Port Forwarding | NAT | VPN | Wireshark | Kali Linux | Rocky Linux | Raspberry Pi | PowerShell

## Contact

Joel Shaffer — Cybersecurity | IT | AI Builder
- LinkedIn: https://linkedin.com/in/joel-shaffer-7a489a2b4
- GitHub: https://github.com/anonymoose48
