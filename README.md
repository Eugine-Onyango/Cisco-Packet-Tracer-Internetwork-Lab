# Cisco-Packet-Tracer-Internetwork-Lab
Building a 6-network enterprise topology from scratch using Cisco Packet Tracer. Learning routing, switching, and server services.

Internetwork Project

Project Status: 🚧 Under Construction (Sprint 0)

About This Project
Welcome to my Project-Based Learning (PBL) journey! I am building a complete, multi-router internetwork simulation using Cisco Packet Tracer. 

Instead of just memorizing commands, I am treating this network like a "Smart City"(which is my way of learning via PBL:
Routers= The Traffic Control/Police (Directing data traffic)
Switches= The Neighborhood Hubs (Connecting local devices)
Cables= The Roads (Where data travels)
Servers= The Downtown Business District (Web & DNS)

My goal is to configure a fully functional enterprise network with dynamic routing (RIPv2), DHCP, and DNS services from scratch.

Tech Stack
Simulator: Cisco Packet Tracer
Hardware Emulated: Cisco 2621XM Routers, 2960 Switches
Protocols: RIPv2, HTTP, DNS, DHCP, ICMP

The Agile Sprint Plan
I am building this in phases (Sprints) to ensure deep understanding:

Sprint 0: Planning & Setup(Current Phase) - Designing the topology and IP scheme.
Sprint 1: Physical Layer- Placing devices and cabling the "roads".
Sprint 2: Basic Config- Hostnames, passwords, and "waking up" the interfaces.
Sprint 3: The Highway System - Configuring RIPv2 dynamic routing.
Sprint 4: Services District - Setting up Web (HTTP) and Phonebook (DNS) servers.
Sprint 5: Documentation- Final testing and portfolio showcase.

Snapshots
(I will upload screenshots of my progress here as I build the city!)*

---
Follow my journey on LinkedIn!



Sprint 1: The Physical Foundation (Completed)
Goal: Establish Layer 1 (Cabling) and Layer 2/3 (Connectivity) status across the entire topology.

What I Built:
The Golden Triangle: Connected 3x Cisco 2621XM Routers in a mesh topology.
The Neighborhoods:Configured LANs for the Laptop (SW), Web Server (North), and DNS Server (SE).
IP Addressing: Implemented a complex VLSM (Variable Length Subnet Mask) scheme, utilizing `/28` for LANs and `/30` for point-to-point WAN links.

 Lessons Learned:
The Cabling Reality:** I discovered that legacy Cisco 2621XM routers don't support Auto-MDIX. I initially tried connecting Router-to-Server with a Straight-Through cable (failed), but realized that since both transmit on the same pins, I needed a Cross-Over Cable. Swapped it out, and the link went Green immediately!
The CLI: Learned the difference between `User Exec Mode` (`>`), `Privileged Mode` (`#`), and `Config Mode` (`(config)#`). You can't ping from the config mode unless you use the the "do" command infront of the command "ping" e.g #do ping 110.120.x.x.

Current Status: All physical links are UP (Green), and devices can ping their local gateways. Next step: Routing!
