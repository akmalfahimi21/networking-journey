# Module 2.1 - Cisco IOS Navigation & Basic Setup

## IOS Modes
- Router>         → User EXEC mode (read only)
- Router#         → Privileged EXEC mode (full access)
- Router(config)# → Global Configuration mode (make changes)

## Sub-modes
- Router(config-line)# → Line config (console/VTY)
- Router(config-if)#   → Interface config

## Navigation Commands
- enable            → User EXEC → Privileged EXEC
- configure terminal → Privileged EXEC → Global Config
- exit              → go back one level
- end               → jump straight back to R1#

## Basic Setup Commands
- hostname R1                    → rename router
- enable secret cisco123         → password for privileged mode
- service password-encryption    → encrypt plain text passwords
- banner motd #message#          → warning message on login

## Password Types
- enable secret → Type 5 (MD5) → STRONG, use this always!
- service password-encryption → Type 7 → WEAK, easily decoded

## Console Password
- line console 0
- password cisco123
- login

## VTY Password (Remote Access)
- line vty 0 4    → configure all 5 remote access lines
- password cisco123
- login

## Saving Configuration
- copy running-config startup-config → save to NVRAM
- running-config → RAM (lost on reboot)
- startup-config → NVRAM (survives reboot)

## Verification Commands
- show running-config      → current active config
- show startup-config      → saved config
- show ip interface brief  → all interfaces and status

## Interface Status Cheat Sheet
- admin down / down → interface is shutdown (manual)
- down / down       → no cable connected
- up / down         → Layer 2 problem
- up / up           → fully working ✅
