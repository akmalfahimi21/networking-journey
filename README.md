# Introduction
I have always been interested in networking, and for a while, I believed I was on the right track. I watched almost all of Jeremy's IT Lab videos and worked through many past-year exam questions, thinking I was building a solid foundation. But I started to notice something — whenever I took a break from studying for a few weeks, I forgot nearly everything I had covered.
The moment that truly woke me up was during an interview for a Network Engineer position. One of the interviewers asked me a simple question: "What is a VLAN?" I could not answer to their expectation. Not because I had never studied it — but because everything I knew was purely memorized. I had the definition, but I had no real understanding behind it.
That was the turning point. I realized that to build a strong foundation in networking, theory alone is not enough. Real understanding comes from hands-on experience, building things from scratch, and knowing why something works — not just what it is.
This repository documents my structured journey to genuinely learn networking from the ground up — combining deep conceptual understanding with real-world project implementations. The goal is not just to pass the CCNA exam, but to become someone who actually thinks and troubleshoots like a network engineer.
The motto for this course is simple: "Understanding first. Certification second."
 
## How This Course Works
Every module follows the same pattern: Concept → Why it matters → Lab in Packet Tracer → See it in Wireshark (where applicable). 
You don't move to the next module until the current one genuinely makes sense — not just memorized, but understood. 
Each module builds directly on the previous one.


## About
- Guided by a structured 6-phase, 24-module course
- Every concept understood before moving forward
- Hands-on labs in Cisco Packet Tracer
- Real traffic analysis in Wireshark

## Tools
- Cisco Packet Tracer
- Wireshark
- Python (for future network automation)
- GitHub (for portfolio documentation)

## Progress

### Phase 1 - Foundations ✅
- [x] Module 1.1 - OSI & TCP/IP Models— The Real Story
- Not just memorizing layers — understanding WHY the models exist, what each layer actually does, and how data gets encapsulated and de-encapsulated as it travels.
OSI 7 layers | TCP/IP 4 layers | Encapsulation| PDUs |Layer responsibilities
- [x] Module 1.2 - IP Addressing & Subnetting— Deep Dive
-The single most important skill in networking. Binary to decimal, subnet masks, CIDR notation, calculating network/broadcast addresses, and VLSM. We drill this until it's second nature.
Binary/Decimal | IPv4 classes | Subnet masks |CIDR | VLSM | Subnetting practice
- [x] Module 1.3 - Wireshark Fundamentals — Reading Real Packets
-Learn to use Wireshark before we need it. Capture live traffic on your own machine, understand the interface, apply filters, and read packet details. This tool will be your best friend.
Wireshark interface | Capture filters | Display filters | Packet anatomy | Protocol layers in captures

### Phase 2 - Device Basics ✅
- [x] Module 2.1 - IOS Navigation & Basic Setup
- [x] Module 2.2 - Interface Configuration
- [x] Module 2.3 - ARP
- [x] Module 2.4 - Saving Configs & Device Management

### Phase 3 - Switching 🔄
- [ ] Module 3.1 - How Switches Work
- [ ] Module 3.2 - VLANs
- [ ] Module 3.3 - Inter-VLAN Routing
- [ ] Module 3.4 - Spanning Tree Protocol
- [ ] Module 3.5 - EtherChannel

### Phase 4 - Routing
- [ ] Module 4.1 - Static Routes
- [ ] Module 4.2 - OSPF
- [ ] Module 4.3 - HSRP

### Phase 5 - Network Services
- [ ] Module 5.1 - DHCP
- [ ] Module 5.2 - DNS
- [ ] Module 5.3 - NAT
- [ ] Module 5.4 - TCP vs UDP

### Phase 6 - Security & Advanced
- [ ] Module 6.1 - ACLs
-Filtering traffic based on rules. Standard vs extended ACLs, where to place them, how they're processed (top-down, first match). The implicit deny at the end.
Standard ACL | Extended ACL | Named ACL | Placement rules | Wildcard masks | show access-lists
- [ ] Module 6.2 - Switch Security— Port Security & Layer 2 Attacks
- How attackers can exploit Layer 2 (MAC flooding, VLAN hopping). Port security to limit MAC addresses per port. DHCP snooping, Dynamic ARP Inspection.
Port security | Sticky MAC | Violation modes | DHCP snooping | DAI | Storm control
- [ ] Module 6.3 - IPv6
-The world is moving to IPv6. Address format, types, how IPv6 replaces ARP with NDP, and basic router/interface configuration. Why IPv6 was necessary.
IPv6 address format|EUI-64|Link-local/Global unicast |NDP vs ARP | SLAAC | OSPFv3
- [ ] Module 6.4 - Wireless
-How WiFi works, the role of APs and WLCs, BSS vs ESS, frequency bands, and security standards. Configure basic wireless in Packet Tracer.
802.11 standards | 2.4GHz vs 5GHz | BSS/ESS/IBSS| WPA2/WPA3 | Lightweight AP + WLC
- [ ] Module 6.5 - Network Automation
-Network Automation & Programmability
The modern network engineer's toolkit. REST APIs, JSON, YANG/NETCONF, and how tools like Ansible are changing network management. Your Python knowledge will shine here!
REST API basics |JSON/XML | NETCONF/RESTCONF |Ansible intro |SDN concepts | Python + Netmiko

## Note
This repo documents my real hands-on learning journey.
Every lab was built and configured by me, not copied.

### The Goal
By the end of this course, you won't just know how to configure a network — you'll understand why every command exists, what's happening at every layer, and how to troubleshoot when things go wrong. That's what separates a real network engineer from someone who just passed a test.


