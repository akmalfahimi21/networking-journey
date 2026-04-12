# Wireshark: The Protocol Analyzer

**Wireshark** is a **Packet Sniffer** and **Protocol Analyzer**. 

For CCNA studies, think of it as a **"microscope"** for your network. While a router or switch just moves data, Wireshark allows you to "capture" that data as it travels across the wire and look inside the headers.
---

## Why it’s Essential for CCNA
In the "hard way" of learning, Wireshark proves that the theories you’re studying (like the OSI model) are actually happening in real-time.

* **See the Layers:** When you capture a packet, Wireshark separates it into layers that match the **OSI model** exactly. You can click on the "Network" section to see the IP addresses or the "Transport" section to see the Port numbers.
* **Troubleshooting:** If two devices can't communicate, Wireshark shows you if the **Three-Way Handshake** (SYN, SYN-ACK, ACK) is actually finishing or if one side is sending "Reset" (RST) packets.
* **Learning Protocols:** You can see exactly how **DHCP** discovers an IP address or how **OSPF** neighbors "talk" to each other to share routing tables.

---

## Wireshark vs. Modern Observability Tools

| Feature | Modern Observability (SolarWinds, Datadog) | Wireshark |
| :--- | :--- | :--- |
| **Best For** | Day-to-day monitoring & alerts | Deep "surgical" troubleshooting |
| **Data Type** | High-level charts, traffic volume, uptime | Raw packets and protocol headers |
| **Speed** | Shows "The network is slow right now" | Shows "The network is slow because of a TCP window size issue" |
| **Scale** | Monitors thousands of devices at once | Analyzes one specific connection at a time |


## Implementing Wireshark
So for this part we will be using wireshark to understand how packet are actually being managed from device to device.
<img width="1920" height="1080" alt="Wireshark1 0" src="https://github.com/user-attachments/assets/7b91fbdc-9c14-4126-a23d-a50ced23e322" />
<img width="1920" height="1020" alt="Screenshot 2026-04-12 103941" src="https://github.com/user-attachments/assets/b77e1425-c601-4a3f-957f-348dbe24f4e4" />

If we click on the Wifi, we can see real live network traffic is going on here.

<pre>
Time        → when the packet was captured
Source      → who sent it (IP or MAC address)
Destination → who it's going to
Protocol    → what type of traffic (DNS, TCP, HTTP etc)
Length      → size of the packet in bytes
Info        → quick summary of what the packet is doing
</pre>

🎯 TCP is one of the most important ones to understand.
Click on any TCP packet to select it. And we should see two things appear:

Middle panel — a tree breakdown of the packet showing all its layers
Bottom panel — the raw bytes in hex and ASCII

In the middle panel we can confirmed below:
> Frame
> Ethernet II
> Internet Protocol Version 4
> Transmission Control Protocol

And this is actually the OSI model in real life! 
Each layer we studied in Module 1.1 is showing up as a real section in a real packet. 🔬
<pre>
Frame                          → Layer 1 (Physical)
Ethernet II                    → Layer 2 (Data Link)
Internet Protocol Version 4    → Layer 3 (Network)
Transmission Control Protocol  → Layer 4 (Transport)
</pre>

Click the arrow next to "Ethernet II" to expand it.


## Why my Laptop IP changes

While using Wireshark, I observed that my IP address changed from the previous day. This is due to **DHCP (Dynamic Host Configuration Protocol)**.
In the networking world, whether an IP address changes depends on how it is assigned. There are two main ways this happens: Dynamic and Static.

1. Dynamic IP (The Most Common)
Most devices (like your phone, laptop, or PC) use a protocol called DHCP (Dynamic Host Configuration Protocol).
- How it works: Your router "leases" an IP address to your device for a specific amount of time (e.g., 24 hours).
- Why it changes: When the lease expires, your device might get a different IP address from the pool, especially if it was disconnected for a while or if the router was restarted.
- Analogy: It’s like staying in a hotel. You have a room number today, but if you check out and come back next week, you’ll likely get a different room.

2. Static IP (The Permanent Way)
A Static IP is manually configured and never changes unless a human changes it.
- Who uses it: Servers, printers, and network switches/routers.
- Why: You don't want your printer's address to change every day, or no one would be able to find it to print!
- Analogy: This is like your home address. It stays the same so people always know where to find you.


### Key Concepts:
* **Lease Time:** The amount of time a router allows a device to use an IP address. Once this time is up, the IP can be given to someone else.
* **DORA Process:** The 4-step handshake (Discovery, Offer, Request, Acknowledgment) used to assign an IP.
* **Dynamic IP:** Common for end-user devices (Laptops, Phones). It saves the admin from manually typing IPs into every device.
* **Static IP:** Used for Servers and Network Infrastructure (Routers/Switches) so their address remains constant.

> **Observation:** In Wireshark, filtering for `udp.port == 67 || udp.port == 68` will show these DHCP packets in action.

use ipconfig/all and we can confirmed when our ip address will expired.
Refer below:-
<img width="1115" height="628" alt="Screenshot 2026-04-12 113611" src="https://github.com/user-attachments/assets/d93ff8b0-7294-4284-bd7e-4440d8919c35" />

















