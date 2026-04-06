# Module 2.4 - Saving Configs & Device Management

## Running vs Startup Config
- running-config → RAM (temporary, lost on reboot)
- startup-config → NVRAM (permanent, survives reboot)
- copy running-config startup-config → saves config

## CDP (Cisco Discovery Protocol)
- Cisco proprietary protocol
- Enabled by default on all Cisco devices
- Discovers directly connected Cisco neighbors
- Shares: hostname, IP, model, IOS version, interface

## CDP Commands
- show cdp neighbors        → quick neighbor summary
- show cdp neighbors detail → full info including IP
- no cdp enable             → disable CDP on interface

## CDP Output Fields
- Device ID    → neighbor hostname
- Local Intrfce → MY port
- Holdtime     → seconds until entry expires
- Capability   → R=Router, S=Switch
- Platform     → device model
- Port ID      → neighbor's port

## LLDP (Link Layer Discovery Protocol)
- Open standard (IEEE 802.1AB)
- Works with ANY vendor (Cisco, Juniper, HP etc)
- Disabled by default on Cisco devices
- Must enable manually with: lldp run

## LLDP Commands
- lldp run              → enable LLDP globally
- show lldp neighbors   → quick neighbor summary
- show lldp neighbors detail → full info
- no lldp transmit      → disable LLDP transmit on interface
- no lldp receive       → disable LLDP receive on interface

## CDP vs LLDP Comparison
- CDP  → Cisco only, enabled by default
- LLDP → Any vendor, disabled by default
- Best practice → run both in mixed environments

## Security Note
- CDP/LLDP advertise device info to anyone connected
- Disable on interfaces facing untrusted networks
- Keep enabled only between trusted network devices

## Lab Topology
PC (192.168.1.1) ──F0────G0/0── R1 ──G0/1────G0/0── R2
                    192.168.1.2  192.168.2.1      192.168.2.2

Network 1: 192.168.1.0/24
Network 2: 192.168.2.0/24
