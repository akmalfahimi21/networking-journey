# Module 1.2 - IP Addressing & Subnetting

## Key Concepts

- IP address = 32 bits, written in 4 octets (dotted decimal)
- Computers see IP addresses as binary (1s and 0s)
- Every IP address has two parts: Network + Host

## IP Address Classes
- Class A: 1-126    /8  → 16,777,214 hosts
- Class B: 128-191  /16 → 65,534 hosts
- Class C: 192-223  /24 → 254 hosts

## Private IP Ranges
- 10.0.0.0/8
- 172.16.0.0/16
- 192.168.0.0/24

## Subnet Mask
- Tells us where network ends and host begins
- 255.255.255.0 = /24 (24 network bits, 8 host bits)

## Subnetting Formula
- Host bits = 32 - prefix length
- Usable hosts = 2^(host bits) - 2
- Block size = 2^(host bits)
- Subnets needed = 2^(borrowed bits)

## VLSM - Variable Length Subnet Masking
- Different sized subnets for different needs
- Always start with biggest subnet first
- Each subnet is its own separate network
- Need a router to communicate between subnets

## Example - 192.168.10.0/24 into 8 subnets
- Borrowed bits: 3 (2^3=8)
- New prefix: /27
- Block size: 32
- Usable hosts per subnet: 30

