# Module 1.3 - Wireshark Fundamentals

## What is Wireshark?
- Free and open source packet analyzer
- Captures and reads real live network traffic
- Essential tool for network troubleshooting

## Key Columns
- Time → when packet was captured
- Source → who sent it
- Destination → who it's going to
- Protocol → type of traffic (DNS, TCP, ARP etc)
- Length → packet size in bytes
- Info → quick summary of packet

## OSI Layers in Wireshark
- Frame → Layer 1 (Physical)
- Ethernet II → Layer 2 (Data Link)
- Internet Protocol v4 → Layer 3 (Network)
- TCP/UDP → Layer 4 (Transport)

## Important Display Filters
- dns → show only DNS traffic
- tcp → show only TCP traffic
- arp → show only ARP traffic
- ip.addr == x.x.x.x → filter by IP address

## What We Captured
- DNS query and response (name to IP translation)
- TCP/TLS traffic (encrypted HTTPS on port 443)
- ARP request and reply (MAC address discovery)

## TTL (Time To Live)
- Countdown counter on every packet
- Decrements by 1 at each router hop
- Packet dies when TTL reaches 0
- Prevents packets looping forever
- Windows starts at 128, Linux at 64, Cisco at 255

## Key Observations
- MAC address changes at every hop (Layer 2)
- IP address stays the same entire journey (Layer 3)
- DNS must resolve before ping can be sent
- ARP must complete before ping can be sent
- Private IP 10.x.x.x seen on laptop (hotspot network)
