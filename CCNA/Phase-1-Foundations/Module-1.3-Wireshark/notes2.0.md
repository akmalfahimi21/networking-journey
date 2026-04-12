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
<img width="1920" height="1080" alt="wireshark1 1" src="https://github.com/user-attachments/assets/3124d681-77e4-4b64-afd1-f310da294a1a" />

If we click on the Wifi, we can see real live network traffic is going on here.

Time        → when the packet was captured
Source      → who sent it (IP or MAC address)
Destination → who it's going to
Protocol    → what type of traffic (DNS, TCP, HTTP etc)
Length      → size of the packet in bytes
Info        → quick summary of what the packet is doing

The trafiic in going superfast. So we will capture 







