# Module 1.1 - OSI & TCP/IP Models

## Key Concepts
- OSI model was created to standardize networking
  so different vendors can communicate
- OSI has 7 layers, TCP/IP has 4 layers
- OSI = theory blueprint, TCP/IP = real world implementation

## The 7 OSI Layers
- Layer 7: Application
- Layer 6: Presentation
- Layer 5: Session
- Layer 4: Transport
- Layer 3: Network
- Layer 2: Data Link
- Layer 1: Physical

Do you ever wonder when you sending a whatsapp text to your friend what is happening?
How the message is being processing?

Your message starts at Layer 7 as text →
     Simple Down
gets formatted and encrypted at Layer 6 → 
a session is managed at Layer 5 → 
TCP breaks it into segments at Layer 4 →
IP addresses are added at Layer 3 →
MAC addresses added at Layer 2 → 
finally becomes radio waves (WiFi) at Layer 1 and flies through the air to your router.
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
