<img width="1920" height="1080" alt="wireshark1 1" src="https://github.com/user-attachments/assets/82c4dbcc-230c-4afe-977a-173dde62e0b5" />
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
- The single most important skill in networking. Binary to decimal, subnet masks, CIDR notation, calculating network/broadcast addresses, and VLSM. We drill this until it's second nature.
Binary/Decimal | IPv4 classes | Subnet masks |CIDR | VLSM | Subnetting practice
- [x] Module 1.3 - Wireshark Fundamentals — Reading Real Packets
- Learn to use Wireshark before we need it. Capture live traffic on your own machine, understand the interface, apply filters, and read packet details. This tool will be your best friend.
Wireshark interface | Capture filters | Display filters | Packet anatomy | Protocol layers in captures

### Phase 2 - Device Basics ✅
- [x] Module 2.1 - IOS Navigation & Basic Setup
- Getting comfortable with the CLI — modes, navigation shortcuts, help system, and basic device hardening. Every command typed with intention, not just copying syntax.
User/Privileged/Config modes | Hostname | Passwords | Banner MOTD | Console & VTY lines | SSH setup | show commands
- [x] Module 2.2 - Interface Configuration
Assigning IP addresses to interfaces, bringing them up, verifying with show commands. Understanding what "no shutdown" actually means and why interfaces default to down.
ip address command | no shutdown | show ip interface brief | show interfaces | Loopback interfaces
- 🔬 First real lab: Connect 2 PCs via a router, configure IPs, get them pinging each other
- [x] Module 2.3 - ARP— The Glue Between Layer 2 and Layer 3
How does a device find the MAC address for an IP? ARP. We'll watch ARP requests and replies happen in real time in Wireshark and simulate it in Packet Tracer's simulation mode.
ARP request/reply | ARP cache | show arp | Gratuitous ARP | Proxy ARP
- [x] Module 2.4 - Saving Configs & Device Management
- The difference between running-config and startup-config. What happens when a router reboots without saving. CDP and LLDP for discovering neighbors.
running-config vs startup-config |copy run start |CDP/LLDP |show version |Clock & timezone
### Phase 3 - Switching 🔄
- [ ] Module 3.1 - How Switches Work — MAC Tables & Forwarding
- Switches aren't magic. Understand how they learn MAC addresses, build their CAM table, and make forwarding decisions. The difference between switches, hubs, and bridges.
MAC address table |Learning/Flooding/Forwarding/Filtering |show mac address-table | Aging timers
- [ ] Module 3.2 - VLANs
- VLANs are one of the most important concepts in networking. Understand the problem they solve, how to create them, assign ports, and verify. Access ports vs trunk ports explained properly.
VLAN creation | Access ports | Trunk ports | 802.1Q tagging | Native VLAN | show vlan brief
- 🔬 Lab: Build a network with 3 VLANs, verify traffic isolation between them
- [ ] Module 3.3 - Inter-VLAN Routing— Getting VLANs Talking
VLANs isolate traffic — but sometimes different VLANs need to communicate. Router-on-a-Stick and Layer 3 switches. Understanding subinterfaces and why we need them.
Router-on-a-stick| Subinterfaces | encapsulation dot1Q | Layer 3 switch SVIs | ip routing
- [ ] Module 3.4 - Spanning Tree Protocol— Preventing Loops
What happens when you have redundant switch links? Broadcast storms. STP prevents this. Understand the election process, port roles/states, and why STP does what it does.
Broadcast storms| Root bridge election | Port roles | Port states | RSTP | PortFast / BPDU Guard
- [ ] Module 3.5 - EtherChannel— Bundling Links Together
- Instead of one fast link, bundle multiple links into one logical channel. More bandwidth, redundancy. LACP vs PAgP, and how STP sees EtherChannel.
EtherChannel concept | LACP | PAgP | Static EtherChannel | show etherchannel summary

### Phase 4 - Routing
- [ ] Module 4.1 - Routing Fundamentals & Static Routes
- How routers make forwarding decisions. The routing table, longest prefix match, administrative distance. Static routes — when to use them and how to configure them properly.
Routing table | Longest prefix match | AD | Static routes | Default route | Floating static routes
- [ ] Module 4.2 - OSPF— Open Shortest Path First
The most important dynamic routing protocol for CCNA. How routers discover each other, build a topology map, and calculate the best path. Single-area OSPF deeply understood, multi-area introduced.
Link-state vs distance vector | OSPF neighbor adjacency | Hello packets | LSA/LSDB | DR/BDR election | Cost metric | show ip ospf neighbor
- 🔬 Lab: Multi-router topology, watch OSPF hellos in Wireshark, verify full adjacency
- [ ] Module 4.3 - First Hop Redundancy — HSRP
- What happens if your default gateway router goes down? HSRP provides a virtual IP so end devices don't notice. Understanding active/standby, preemption, and failover.
HSRP concept | Virtual IP/MAC | Active/Standby | Priority & preemption | show standby
### Phase 5 - Network Services
- [ ] Module 5.1 - DHCP— Automatic IP Assignment
- How devices get their IP addresses automatically. Configure a router as a DHCP server, watch the DORA process happen in Wireshark — Discover, Offer, Request, Acknowledge.
DORA process | DHCP server config | Excluded addresses|DHCP relay agent |ip helper-address
- [ ] Module 5.2 - DNS— Translating Names to Addresses
How DNS actually works under the hood. Recursive vs iterative queries, DNS hierarchy, and watching DNS queries happen in Wireshark. Configure basic DNS in Packet Tracer.
DNS hierarchy | Recursive queries | A records | PTR records | DNS in Wireshark | ip domain-lookup
- [ ] Module 5.3 - NAT— Network Address Translation
- How your private home IP becomes a public IP when traffic leaves to the internet. Static NAT, Dynamic NAT, and PAT (the one your home router actually uses). Configure and verify.
Private vs Public IP | Static NAT | Dynamic NAT | PAT/NAT Overload | show ip nat translations | inside/outside
- [ ] Module 5.4 - TCP vs UDP— Transport Layer Deep Dive
- When do applications use TCP vs UDP and why? Watch the TCP 3-way handshake in Wireshark. Understand ports, sessions, and what connection-oriented really means.
TCP 3-way handshake | TCP 4-way termination|Sequence/Acknowledgement | UDP use cases | Well-known ports| Wireshark TCP stream
### Phase 6 - Security & Advanced
- [ ] Module 6.1 - ACLs
- Filtering traffic based on rules. Standard vs extended ACLs, where to place them, how they're processed (top-down, first match). The implicit deny at the end.
Standard ACL | Extended ACL | Named ACL | Placement rules | Wildcard masks | show access-lists
- [ ] Module 6.2 - Switch Security— Port Security & Layer 2 Attacks
- How attackers can exploit Layer 2 (MAC flooding, VLAN hopping). Port security to limit MAC addresses per port. DHCP snooping, Dynamic ARP Inspection.
Port security | Sticky MAC | Violation modes | DHCP snooping | DAI | Storm control
- [ ] Module 6.3 - IPv6
- The world is moving to IPv6. Address format, types, how IPv6 replaces ARP with NDP, and basic router/interface configuration. Why IPv6 was necessary.
IPv6 address format|EUI-64|Link-local/Global unicast |NDP vs ARP | SLAAC | OSPFv3
- [ ] Module 6.4 - Wireless
- How WiFi works, the role of APs and WLCs, BSS vs ESS, frequency bands, and security standards. Configure basic wireless in Packet Tracer.
802.11 standards | 2.4GHz vs 5GHz | BSS/ESS/IBSS| WPA2/WPA3 | Lightweight AP + WLC
- [ ] Module 6.5 - Network Automation
- Network Automation & Programmability
The modern network engineer's toolkit. REST APIs, JSON, YANG/NETCONF, and how tools like Ansible are changing network management. Your Python knowledge will shine here!
REST API basics |JSON/XML | NETCONF/RESTCONF |Ansible intro |SDN concepts | Python + Netmiko

## Note
This repo documents my real hands-on learning journey.
Every lab was built and configured by me, not copied.

### The Goal
By the end of this course, you won't just know how to configure a network — you'll understand why every command exists, what's happening at every layer, and how to troubleshoot when things go wrong. That's what separates a real network engineer from someone who just passed a test.


