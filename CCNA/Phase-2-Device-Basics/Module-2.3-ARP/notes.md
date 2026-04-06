# Module 2.3 - ARP (Address Resolution Protocol)

## What is ARP?
- Bridges gap between Layer 3 (IP) and Layer 2 (MAC)
- When device knows destination IP but not MAC address
- ARP finds the MAC address automatically

## ARP Process
1. PC broadcasts "Who has 192.168.1.2? Tell 192.168.1.1"
2. Every device receives the broadcast
3. Only 192.168.1.2 (router) responds
4. Router sends UNICAST reply directly to PC
5. PC stores MAC in ARP cache
6. Communication can now happen ✅

## ARP Packet Structure
- OPCODE 0x0001 → ARP Request (broadcast)
- OPCODE 0x0002 → ARP Reply (unicast)
- Request: TARGET MAC = 0000.0000.0000 (unknown)
- Reply: TARGET MAC = filled in! ✅

## Key Observations
- ARP Request  → sent to FFFF.FFFF.FFFF (everyone)
- ARP Reply    → sent directly to requester (unicast)
- ARP only exists at Layer 2 (Layers 3-7 empty!)
- ICMP ping waits for ARP to complete first
- Gratuitous ARP = device announcing itself on startup

## Gratuitous ARP
- Device announces its own IP/MAC when it comes online
- Used to detect IP conflicts on the network
- If anyone replies = someone else has the same IP!

## Commands
- show arp      → view router's ARP cache
- arp -d        → clear ARP cache on PC

## Packet Tracer Simulation Mode
- Switch to Simulation mode (bottom right)
- Filter by ARP and ICMP only
- Watch packets travel hop by hop
- Click each packet to see PDU details

## PDU (Protocol Data Unit)
- Just means "data chunk at a specific layer"
- Layer 4 = Segment
- Layer 3 = Packet
- Layer 2 = Frame
- Layer 1 = Bits

## In Layers vs Out Layers
- In Layers  = what the device RECEIVED
- Out Layers = what the device SENT OUT

## Lab Topology
PC (192.168.1.1) ──── R1 (192.168.1.2)
