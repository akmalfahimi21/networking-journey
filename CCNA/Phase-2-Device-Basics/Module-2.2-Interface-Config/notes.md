# Module 2.2 - Interface Configuration & IP Addressing

## Key Concepts
- Each router interface = one network
- Interface must have IP address + no shutdown to work
- Default gateway = router's IP on the same network as PC

## Interface Configuration Commands
- interface GigabitEthernet0/0  → enter interface config
- ip address 192.168.1.2 255.255.255.0  → assign IP
- no shutdown                   → bring interface up
- exit                          → back to global config

## Verification Commands
- show ip interface brief       → quick status all interfaces
- show interfaces G0/0          → detailed interface info
- show arp                      → view ARP cache

## Important show interfaces fields
- up/up                → fully working
- Hardware address     → interface MAC address
- Internet address     → IP address configured
- MTU 1500 bytes       → max packet size
- Full-duplex          → send and receive simultaneously
- reliability 255/255  → 100% reliable, no errors

## Lab Topology
PC (192.168.1.1) ──F0────G0/0── R1 (192.168.1.2)

## ARP Table from Router
- show arp shows:
  → Router's own IP/MAC (age = -)
  → Connected devices IP/MAC (age = minutes)

## Key Rules
- Same network = can communicate directly
- Different network = need router to communicate
- One interface = one network only
