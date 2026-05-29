# Ali's Enterprise Security Lab

> Network & Security Engineer | Check Point · Cisco · Wazuh · VMware ESXi · Active Directory

## Overview
A physical enterprise-grade security lab built on real hardware,
simulating a corporate network environment with perimeter security,
multi-VLAN segmentation, centralized SIEM monitoring, and Active Directory.

## Architecture
```
Internet → Check Point 1570 → Cisco 2960 Switch → Dell Server (ESXi)
                                                          │
                              ┌───────────────────────────┤
                              │                           │
                         VLAN 10 (Servers)          VLAN 20 (Clients)
                         VLAN 88 (Management)       VLAN 30 (Home)
```

## Technologies
| Component      | Technology              | Purpose                        |
|----------------|-------------------------|--------------------------------|
| Firewall       | Check Point 1570        | Perimeter Security / NAT / VPN |
| Switch         | Cisco 2960              | L2 Segmentation / Trunking     |
| Hypervisor     | VMware ESXi             | Virtual Infrastructure         |
| SIEM           | Wazuh 4.14              | Log Analysis / Alerting        |
| Identity       | Windows Server 2025 AD  | DNS / DHCP / GPO               |
| IDS (Phase B)  | Suricata                | Network Threat Detection       |

## Key Implementations
- ✅ Check Point 1570: Security Policy (Stealth, Cleanup, Blacklist), NAT, IPSec/SSL VPN, NTP, Syslog → Wazuh
- ✅ Cisco 2960: VLANs, 802.1Q Trunking, DHCP Snooping, Port Security, RSTP + BPDUGuard
- ✅ VMware ESXi: 4 vSwitches — VLAN 10/20/88 + isolated SPAN for IDS
- ✅ Wazuh SIEM v4.14: 3 active agents + 3 syslog sources (Check Point, Cisco, ESXi)
- ✅ Windows Server 2025: AD DS, DNS, DHCP, OUs, GPO Security Baseline, Audit Policy
- ✅ Domain-joined Windows 10 client with user/admin accounts

## Lab Phases
| Phase | Description | Status |
|-------|-------------|--------|
| A | Foundation: Firewall, Switch, Wazuh, Windows AD | ✅ Complete |
| B | IDS: SPAN port + Suricata + YARA rules | 🔄 In Progress |
| C | SOC: TheHive + Cortex + MISP | ⬜ Planned |
| D | Dashboards: ELK Stack + PRTG | ⬜ Planned |
| E | Automation: Python + Ansible + AWS VPN | ⬜ Planned |

## Skills Demonstrated
`Check Point Firewall` `Cisco IOS` `VLANs & Trunking` `Network Segmentation`
`Wazuh SIEM` `VMware ESXi` `Windows Server 2025` `Active Directory`
`GPO` `Network Hardening` `VPN (IPSec/SSL)` `Log Analysis`
`DHCP Snooping` `Port Security` `STP/RSTP`

## Certifications
- CEH — Certified Ethical Hacker | EC-Council (2022)
- CSA — Certified SOC Analyst | EC-Council (2023)
- LPIC-1 — Linux Professional Institute (2024)
- CCNA — Course completed | Exam: November 2026

## Contact
- LinkedIn: https://www.linkedin.com/in/ali-ahmad-mahmud-112903225
- Email: ahmadmahmudali1@gmail.com 
