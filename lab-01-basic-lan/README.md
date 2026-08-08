# Lab 01 — Basic LAN, IPv4 Addressing & ARP

## Objective

This is my first hands-on networking lab built with Cisco Packet Tracer.

The objective was to build a small LAN from scratch, manually configure IPv4 addressing, verify connectivity between devices, and observe how ARP and ICMP operate inside a local network.

## Network Topology

The lab consists of:

- 1 Cisco ISR4331 Router
- 1 Cisco 2960 Switch
- 4 PCs
- 1 Server
- 1 Network Printer

All end devices are connected to the switch.

## IPv4 Network

**Network:** `192.168.1.64/28`  
**Subnet Mask:** `255.255.255.240`  
**Usable Host Range:** `192.168.1.65 - 192.168.1.78`  
**Broadcast Address:** `192.168.1.79`

| Device | IPv4 Address | Subnet Mask | Default Gateway |
|---|---|---|---|
| PC0 | 192.168.1.68 | 255.255.255.240 | 192.168.1.73 |
| PC1 | 192.168.1.69 | 255.255.255.240 | 192.168.1.73 |
| PC2 | 192.168.1.70 | 255.255.255.240 | 192.168.1.73 |
| PC3 | 192.168.1.71 | 255.255.255.240 | 192.168.1.73 |
| Router0 | 192.168.1.73 | 255.255.255.240 | — |
| Server0 | 192.168.1.74 | 255.255.255.240 | 192.168.1.73 |
| Printer0 | 192.168.1.75 | 255.255.255.240 | 192.168.1.73 |

## Connectivity Testing

Connectivity between devices was verified using ICMP Echo Requests.

Examples:

- PC → Router
- PC → PC
- PC → Server

The tests completed successfully.

## Packet Simulation

Packet Tracer Simulation Mode was used to observe traffic moving through the LAN.

During the simulation I observed an ARP Request using the Ethernet broadcast destination:

`FF:FF:FF:FF:FF:FF`

This happens when a host knows the destination IPv4 address but needs to discover the corresponding MAC address on the local network.

## What I Learned

- How to build a basic switched LAN in Cisco Packet Tracer
- How to manually configure IPv4 addresses
- How a `/28` subnet defines the network, host range, and broadcast address
- The role of the default gateway
- How switches forward Ethernet frames inside a LAN
- How ARP resolves an IPv4 address to a MAC address
- Why an ARP Request is sent as a Layer 2 broadcast
- How to use ICMP to verify network connectivity
- How to inspect network traffic using Packet Tracer Simulation Mode

## Next Steps

Future labs will progressively introduce additional networks, routing, network services, and troubleshooting scenarios.
