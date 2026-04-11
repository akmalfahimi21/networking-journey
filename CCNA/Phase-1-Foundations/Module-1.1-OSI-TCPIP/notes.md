# Module 1.1 - OSI & TCP/IP Models

## Key Concepts
- OSI model was created to standardize networking
  so different vendors can communicate
- OSI has 7 layers, TCP/IP has 4 layers
- OSI = theory blueprint, TCP/IP = real world implementation

OSI Model was created as a theoretical framework — a universal reference guide. It was never actually fully implemented as a real protocol suite. Think of it like a blueprint.
TCP/IP Model is the real world implementation — the actual protocols the internet runs on today. Think of it like the actual building.

### OSI vs. TCP/IP Model Mapping

| Layer | OSI Model | TCP/IP Model |
| :---: | :--- | :--- |
| **7** | Application | Application |
| **6** | Presentation | Application |
| **5** | Session | Application |
| **4** | Transport | Transport |
| **3** | Network | Internet |
| **2** | Data Link | Network Access |
| **1** | Physical | Network Access |


## The 7 OSI Layers
- Layer 7: Application
- Layer 6: Presentation
- Layer 5: Session
- Layer 4: Transport
- Layer 3: Network
- Layer 2: Data Link
- Layer 1: Physical

Do you ever wonder when you sending a whatsapp text to your friend what is happening?
How the message is being processed?

<pre>
Layer 7: Your message starts as text 
                ⬇️
Layer 6: Data is formatted and encrypted 
                ⬇️
Layer 5: The session is managed 
                ⬇️
Layer 4: TCP breaks it into segments 
                ⬇️
Layer 3: IP addresses are added 
                ⬇️
Layer 2: MAC addresses are added 
                ⬇️
Layer 1: Finally it becomes radio waves (WiFi) and flies to your router.
</pre>
At your friend’s phone — it goes the opposite direction. 
Layer 1 receives the radio waves and passes it up layer by layer until Layer 7 shows them your message. That’s de-encapsulation.


## Encapsulation vs De-encapsulation
- Encapsulation = adding headers going DOWN the stack
- De-encapsulation = stripping headers going UP the stack

## PDU Names
- Layer 4 = Segment
- Layer 3 = Packet
- Layer 2 = Frame
- Layer 1 = Bits

## Layer 2 vs Layer 3
- Layer 2 = MAC address, local delivery, hop to hop
- Layer 3 = IP address, end to end delivery

| Layer | Description |
|---|---|
| **Layer 3  Network** | Handles delivery across different networks. It cares about getting a packet from the source all the way to the final destination, no matter how many routers it crosses. IP addresses are logical — they can be assigned and changed. |
| **Layer 2  Data Link** | Handles delivery within the same local network. It only cares about getting a frame from one device to the next device (hop to hop). MAC addresses are burned into the hardware — they never change and they’re only relevant locally. |


Lets think of real world example:

When you send data from your laptop in KL to a server in the US. What do you think will happen to the IP address and MAC address?

The IP address (Layer 3) stays the same the entire journey. Source IP and destination IP don’t change.
But the MAC address (Layer 2) changes at every single hop. Your laptop talks to your router using your router’s MAC. Your router then talks to the next router using THAT router’s MAC. And so on.
Think of it like this:
	∙	IP address = your final destination address (New York)
	∙	MAC address = the next bus stop








