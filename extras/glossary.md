# Glossary

Plain-English definitions for terms used across this repo (**PC Basics**).  
See also: [How the Internet Works](how-internet-works.md) · [AI & GPUs](ai-and-gpus.md) · [Operating Systems](basics/operating-systems.md)

**Jump to:** [A](#a) · [B](#b) · [C](#c) · [D](#d) · [E](#e) · [F](#f) · [G](#g) · [H](#h) · [I](#i) · [J](#j) · [K](#k) · [L](#l) · [M](#m) · [N](#n) · [O](#o) · [P](#p) · [Q](#q) · [R](#r) · [S](#s) · [T](#t) · [U](#u) · [V](#v) · [W](#w) · [X](#x) · [Y](#y) · [Z](#z)

---

## A

### Anycast
One IP address announced from many locations; you’re routed to the **nearest** one.  
*See also:* CDN, Routing, BGP.

### ARP (Address Resolution Protocol)
Maps an IP address to a **MAC** address on a local network (L2↔L3 boundary).  
*See also:* MAC, Ethernet, IP.

### Authoritative Nameserver
The DNS server that holds the **official** records for a domain.  
*See also:* DNS, Resolver, TTL.

---

## B

### Bandwidth
How much data can pass per second (capacity), not the same as **latency** (delay).  
*See also:* Latency, Throughput.

### Batch Size (AI)
Number of samples processed together in one training or inference step; larger batches can speed up but require more VRAM.  
*See also:* VRAM, Quantization.

### BGP (Border Gateway Protocol)
The routing protocol the **internet’s big networks** use to exchange paths.  
*See also:* Routing, AS (Autonomous System).

### BIOS
Basic Input/Output System; firmware that initializes hardware and boots the OS.  
*See also:* UEFI, Firmware, Bootloader.

### Bootloader
Software that loads the OS kernel into memory during startup.  
*See also:* Kernel, BIOS, UEFI.

### Bottleneck
The slowest part of a system that limits overall performance.  
*See also:* Profiling, Throughput.

---

## C

### CA (Certificate Authority)
A trusted org that signs website certificates so browsers can verify identity.  
*See also:* TLS, Certificate, Chain of trust.

### Cache / Caching
Storing responses to reuse later and go faster (browser, CDN, proxy).  
*See also:* Cache-Control, ETag, CDN.

### Cache-Control (HTTP)
Headers that tell caches **what** and **for how long** they may store.  
*See also:* ETag, Last-Modified.

### CDN (Content Delivery Network)
A network of edge servers that serve content from **near** the user.  
*See also:* Anycast, Cache, Origin.

### CDN PoP
Point of Presence; a location where CDN servers are deployed to cache and deliver content.  
*See also:* CDN, Edge Compute.

### Certificate (TLS)
A signed document proving a site’s identity (includes public key).  
*See also:* CA, TLS, Chain.

### Chipset
A set of electronic components on the motherboard that manage data flow between the CPU, memory, and peripherals.  
*See also:* Motherboard, CPU.

### CLI (Command Line Interface)
Text-based way to interact with a computer using commands.  
*See also:* GUI, Shell.

### Context Window (AI)
The maximum amount of text an LLM can consider at once for generating responses.  
*See also:* LLM, Token.

### CORS (Cross-Origin Resource Sharing)
Browser rules allowing/denying web requests across different origins.  
*See also:* HTTP, Same-origin policy.

### CPU (Central Processing Unit)
General-purpose processor with a **few powerful cores**; great for varied tasks.  
*See also:* GPU, iGPU.

### CSP (Content Security Policy)
HTTP header that helps prevent XSS and other code injection attacks by restricting resource loading.  
*See also:* HTTP, Security.

### CUDA
NVIDIA's parallel computing platform for GPU-accelerated applications, especially AI.  
*See also:* GPU, ROCm.

### cuDNN
NVIDIA's library for deep neural networks, optimizing performance on CUDA-enabled GPUs.  
*See also:* CUDA, GPU.

### CIDR (Classless Inter-Domain Routing)
Compact way to write subnets, e.g., `192.168.1.0/24`.  
*See also:* Subnet, IP.

### CNAME (Canonical Name)
DNS record that makes one name an **alias** of another name.  
*See also:* DNS, A/AAAA.

---

## D

### Datagram
A self-contained packet of data (term often used with **UDP**).  
*See also:* UDP, Packet.

### dGPU (Discrete GPU)
A separate graphics card with its own memory and processing power, more powerful than integrated GPUs.  
*See also:* GPU, iGPU.

### DHCP (Dynamic Host Configuration Protocol)
Automatically assigns IP addresses and network settings to devices on a network.  
*See also:* IP, NAT.

### DNS (Domain Name System)
The internet’s **phonebook**: maps names (e.g., example.com) to IPs.  
*See also:* Resolver, Authoritative, TTL, DNSSEC, DoH/DoT.

### DNSSEC
Security extensions that **sign** DNS data to prevent tampering.  
*See also:* DNS.

### DoH / DoT
DNS over HTTPS/TLS for **encrypted** DNS lookups.  
*See also:* DNS, TLS, HTTPS.

### Driver
Software that allows the OS to communicate with hardware devices.  
*See also:* Kernel, Firmware.

---

## E

### Edge Compute
Running small pieces of code at CDN edges, closer to users.  
*See also:* CDN, Latency.

### Environment Variable
A dynamic value that can affect the way running processes behave on a computer.  
*See also:* Shell, Process.

### Ephemeral Port
A temporary client-side port used for a connection.  
*See also:* Port, TCP.

### Ethernet
Wired LAN technology (frames, MAC addresses, switches).  
*See also:* MAC, Switch, L2.

### ETag
HTTP validator token; lets caches revalidate without re-downloading.  
*See also:* Cache-Control, Last-Modified.

---

## F

### Filesystem
A method for storing and organizing files on a storage device.  
*See also:* SSD, HDD, Path.

### Firewall
Filters traffic based on rules (IP, port, app, content).  
*See also:* NAT, Ports, L3/L4/L7.

### Firmware
Low-level software embedded in hardware that provides control and data manipulation.  
*See also:* BIOS, UEFI, Driver.

### Forward Secrecy (PFS)
TLS property where past sessions stay safe even if long-term keys leak.  
*See also:* TLS, ECDHE.

### FP32/FP16/INT8/FP8 (Precision)
Floating-point and integer formats for numbers in AI models; lower precision reduces size and speeds up computation.  
*See also:* Quantization, VRAM.

---

## G

### Gateway
A router that connects your local network to other networks (e.g., the internet).  
*See also:* Router, NAT.

### Goodput
The useful data transferred per second, excluding protocol overhead.  
*See also:* Throughput, Bandwidth.

### GPU (Graphics Processing Unit)
Thousands of small cores for **parallel math**; accelerates AI and graphics.  
*See also:* VRAM, Tensor Cores, CPU.

### GUI (Graphical User Interface)
Visual way to interact with a computer using windows, icons, and menus.  
*See also:* CLI, Shell.

---

## H

### Handshake
Initial setup phase to agree on parameters/keys (e.g., TCP, TLS).  
*See also:* TCP, TLS.

### Hash
A fixed-size string of characters generated from input data, often used for integrity checks or passwords.  
*See also:* Salt, Security.

### HDD (Hard Disk Drive)
Magnetic storage device for data; slower but cheaper than SSDs.  
*See also:* SSD, NVMe.

### Head-of-Line Blocking
When one slow request blocks others in a queue, common in HTTP/1.1.  
*See also:* HTTP/2, Multiplexing.

### Heatsink
A device that absorbs and dissipates heat from components like CPUs and GPUs.  
*See also:* Thermal Throttling, TDP.

### HSTS (HTTP Strict Transport Security)
HTTP header that forces browsers to use HTTPS for a site, preventing downgrade attacks.  
*See also:* HTTPS, TLS.

### HTTP
The web’s application protocol (methods, headers, status codes).  
*See also:* HTTP/1.1, HTTP/2, HTTP/3, HTTPS.

### HTTP/2
Adds **multiplexing** and header compression over one connection.  
*See also:* HTTP/1.1, HTTP/3.

### HTTP/3
HTTP running over **QUIC** (UDP); faster handshakes, less head-of-line blocking.  
*See also:* QUIC, UDP.

### HTTPS
HTTP inside a **TLS** tunnel (encrypted and authenticated).  
*See also:* TLS.

---

## I

### ICMP
Control/diagnostic protocol (e.g., what **ping** uses).  
*See also:* Ping, IP.

### iGPU (Integrated GPU)
Graphics built into the CPU; efficient but less powerful than discrete GPUs.  
*See also:* GPU, CPU.

### IP (Internet Protocol)
Addresses and routes packets between networks (IPv4/IPv6).  
*See also:* Subnet, Router, NAT.

### IPSec
Suite for securing IP traffic (VPNs, tunnels).  
*See also:* VPN, IP, TLS.

### IPS/IDS (Intrusion Prevention/ Detection System)
Monitors network traffic for malicious activity and can block or alert on threats.  
*See also:* Firewall, Security.

### IPv4 / IPv6
Two versions of IP addressing; IPv6 has a **much larger** address space.  
*See also:* IP.

---

## J

### Jitter
Variation in latency over time, affecting real-time applications like video calls.  
*See also:* Latency, RTT.

### JSON
Text format for structured data (key/value, arrays).  
*See also:* HTTP APIs.

---

## K

### Kernel
The core part of an OS that manages hardware and runs processes.  
*See also:* Process, Thread, Driver.

### Kernel Mode
Privileged mode where the kernel runs with full access to hardware.  
*See also:* Kernel, User Mode.

### Kernel Panic
A critical error in the kernel that causes the system to halt.  
*See also:* Kernel, Crash.

### KVM (Kernel-based Virtual Machine)
Linux kernel module for hardware-assisted virtualization.  
*See also:* Virtualization, Kernel.

---

## L

### Latency
Time it takes for data to travel (delay), not the same as **bandwidth**.  
*See also:* Bandwidth, RTT.

### Load Balancer
Distributes traffic across multiple servers (L4 or L7).  
*See also:* Reverse Proxy, Scaling.

### LLM (Large Language Model)
A type of AI model trained to predict/generate text.  
*See also:* Parameters, Quantization, VRAM.

### Logging
Recording events and messages for debugging and monitoring system behavior.  
*See also:* Telemetry, Profiling.

---

## M

### M.2
A form factor for SSDs that connects directly to the motherboard for high-speed storage.  
*See also:* SSD, NVMe, SATA.

### MAC Address
A hardware address used on local networks (L2).  
*See also:* Ethernet, ARP.

### MFA (Multi-Factor Authentication)
Security method requiring two or more verification factors to access an account.  
*See also:* Security, OAuth.

### Model (AI)
The learned program (its **parameters**) that makes predictions.  
*See also:* Parameters, Tensor.

### Motherboard
The main circuit board that connects all components of a computer.  
*See also:* CPU, RAM, Chipset.

### MPS (Metal Performance Shaders)
Apple's framework for GPU-accelerated computing on macOS and iOS.  
*See also:* GPU, CUDA.

### MTU (Maximum Transmission Unit)
Largest packet size a link can carry without fragmentation.  
*See also:* Fragmentation, Path MTU.

### Multiplexing
Carrying multiple logical streams over one connection (HTTP/2).  
*See also:* HTTP/2, Streams.

---

## N

### NAT (Network Address Translation)
Many private devices share one **public** IP (home routers).  
*See also:* Router, Firewall.

### NAT Traversal
Techniques to allow devices behind NAT to connect directly over the internet.  
*See also:* NAT, STUN.

### Nameserver
A DNS server; can be **recursive** (resolver) or **authoritative** (source of truth).  
*See also:* DNS.

### NPU (Neural Processing Unit)
Power-efficient accelerator for on-device AI tasks.  
*See also:* GPU, TPU.

### NVMe (Non-Volatile Memory Express)
High-speed interface for SSDs, faster than SATA.  
*See also:* SSD, PCIe.

---

## O

### OAuth
Open standard for access delegation, commonly used for third-party logins.  
*See also:* OpenID Connect, Security.

### ONNX (Open Neural Network Exchange)
Format for representing AI models to enable interoperability across frameworks.  
*See also:* Model, Quantization.

### OpenID Connect
Identity layer on top of OAuth for authentication.  
*See also:* OAuth, Security.

### OpenVINO
Intel's toolkit for optimizing and deploying AI models on various hardware.  
*See also:* GPU, NPU.

### Origin (Server)
The “source” server behind a CDN or reverse proxy.  
*See also:* CDN, Reverse Proxy.

### OSI Model
Seven-layer reference model for networking (L1–L7).  
*See also:* [OSI overview](how-internet-works.md#osi-7-layer-model--simple-user-friendly-guide).

---

## P

### Packet
A unit of data at the IP (network) layer.  
*See also:* Frame, Segment, PDU.

### Parameters (AI)
The numbers a model learns; more params usually means a bigger model.  
*See also:* Model, Tensor, VRAM.

### Path
The location of a file or directory in the filesystem.  
*See also:* Filesystem, Environment Variable.

### PCIe (Peripheral Component Interconnect Express)
High-speed interface for connecting components like GPUs and SSDs to the motherboard.  
*See also:* Motherboard, NVMe.

### PDU (Protocol Data Unit)
Generic term for the “data unit” at each layer (Frame/Packet/Segment).  
*See also:* Encapsulation.

### Port
A numbered “door” for services on a host (e.g., 80=HTTP, 443=HTTPS).  
*See also:* TCP, UDP.

### Presentation Layer
OSI layer for formats/encryption/compression (often folded into “application”).  
*See also:* TLS, OSI.

### Process
An instance of a running program with its own memory and resources.  
*See also:* Thread, Kernel.

### Profiling
Analyzing software performance to identify bottlenecks and optimize code.  
*See also:* Bottleneck, Telemetry.

### PSU (Power Supply Unit)
Component that converts AC power to DC for computer components.  
*See also:* Motherboard, TDP.

---

## Q

### Quantization (AI)
Compressing model numbers (e.g., 16-bit → 4-bit) to save VRAM and speed up.  
*See also:* Precision, VRAM.

### Quantization-Aware Training
Training AI models with quantization in mind to maintain accuracy at lower precision.  
*See also:* Quantization, Precision.

### QUIC
Modern transport running over **UDP** with TLS built in; used by HTTP/3.  
*See also:* HTTP/3, UDP, TLS.

---

## R

### RAM (Random Access Memory)
Volatile memory for temporary data storage; faster than storage but loses data on power off.  
*See also:* ROM, SSD.

### Resolver (DNS)
The DNS **helper** your device queries first; it does the lookups for you.  
*See also:* DNS, Authoritative.

### REST (Representational State Transfer)
Architectural style for designing networked applications, often used in web APIs.  
*See also:* HTTP, JSON.

### Reverse DNS
Mapping IP addresses back to domain names.  
*See also:* DNS, IP.

### Reverse Proxy
Server in front of app servers that routes, caches, compresses, or secures.  
*See also:* CDN, Load Balancer.

### ROCm
AMD's open-source platform for GPU computing, similar to CUDA.  
*See also:* GPU, CUDA.

### ROM (Read-Only Memory)
Non-volatile memory that stores firmware and cannot be easily changed.  
*See also:* RAM, Firmware.

### Router
Forwards packets between networks based on routing tables.  
*See also:* IP, BGP, NAT.

### Routing
Choosing paths through networks; on the internet, BGP coordinates this.  
*See also:* BGP, Router.

### RTT (Round Trip Time)
Time for a packet to go to a destination and back; measures latency.  
*See also:* Latency, Jitter.

---

## S

### Salt
Random data added to passwords before hashing to prevent rainbow table attacks.  
*See also:* Hash, Security.

### SATA (Serial ATA)
Interface for connecting storage devices like HDDs and SSDs.  
*See also:* SSD, NVMe.

### Segment
A unit of data at the **TCP** transport layer.  
*See also:* Packet, Frame, PDU.

### Shell
Command-line interpreter that processes commands and scripts.  
*See also:* CLI, Environment Variable.

### SNI (Server Name Indication)
TLS extension that tells the server **which hostname** you want.  
*See also:* TLS, HTTPS, Virtual hosting.

### SPF/DKIM/DMARC
Email authentication protocols: SPF checks sender IP, DKIM verifies signatures, DMARC enforces policies.  
*See also:* Email, Security.

### SSD (Solid State Drive)
Flash-based storage; faster and more reliable than HDDs.  
*See also:* HDD, NVMe.

### STUN/TURN/ICE
Protocols for NAT traversal: STUN discovers public IP, TURN relays traffic, ICE combines them.  
*See also:* NAT Traversal, WebRTC.

### Subnet
A logical slice of an IP network, defined with **CIDR** notation.  
*See also:* CIDR, IP.

### Switch
Connects devices on a local network and forwards **frames** (L2).  
*See also:* Ethernet, MAC.

---

## T

### TDP (Thermal Design Power)
Maximum amount of heat a component is designed to generate.  
*See also:* Heatsink, Thermal Throttling.

### Telemetry
Collection and transmission of data for monitoring and analysis.  
*See also:* Logging, Profiling.

### Tensor (AI)
A multi-dimensional array of numbers; the basic data structure for models.  
*See also:* Model, Parameters.

### Tensor Cores (or Matrix Cores)
Special GPU units that accelerate tensor/matrix math.  
*See also:* GPU, VRAM, Precision.

### Thermal Throttling
Reducing performance to prevent overheating when TDP is exceeded.  
*See also:* TDP, Heatsink.

### Thread
A lightweight process within a program that can run concurrently.  
*See also:* Process, Kernel.

### Throughput
Amount of data processed or transferred per unit time.  
*See also:* Bandwidth, Goodput.

### TLS (Transport Layer Security)
Encrypts/authenticates connections (HTTPS = HTTP over TLS).  
*See also:* Certificate, CA, PFS.

### TLS Handshake
The process of establishing a TLS connection, exchanging keys and certificates.  
*See also:* TLS, Handshake.

### Token (AI)
A unit of text in an LLM, like a word or subword, used for processing.  
*See also:* Context Window, LLM.

### TTL (Time To Live)
How long DNS answers (and other data) may be cached before refresh.  
*See also:* DNS, Cache.

---

## U

### UDP (User Datagram Protocol)
Connectionless, lightweight messages; great for **low latency**.  
*See also:* TCP, QUIC, Datagram.

### UEFI (Unified Extensible Firmware Interface)
Modern replacement for BIOS with more features and security.  
*See also:* BIOS, Firmware.

### URL
The address of a web resource (scheme + host + path + etc.).  
*See also:* HTTP, DNS.

---

## V

### VLAN
Virtual LAN that segments a physical network at Layer 2.  
*See also:* Switch, Trunking.

### VRM (Voltage Regulator Module)
Circuitry on the motherboard that supplies power to the CPU.  
*See also:* Motherboard, PSU.

### VPN (Virtual Private Network)
Creates a secure, encrypted connection over a public network.  
*See also:* IPSec, Security.

### VRAM (Video RAM)
Memory on the GPU. Limits **model size/batch** for local AI workloads.  
*See also:* GPU, Quantization.

---

## W

### WAN / LAN
**WAN**: wide-area (across cities/countries). **LAN**: local network (home/office).  
*See also:* Router, Switch.

### WebSocket
Protocol for full-duplex communication over a single TCP connection, often used for real-time web apps.  
*See also:* HTTP, TCP.

### Wi-Fi (802.11)
Wireless LAN; speed/latency depend on band, distance, interference.  
*See also:* Ethernet, Channels.

---

## X

### X.509
Standard for public key certificates used in TLS and other security protocols.  
*See also:* Certificate, TLS.

### XML
Markup language for encoding documents in a human-readable format.  
*See also:* JSON, HTTP.

---

## Y

### YAML
Human-readable data serialization format, often used for configuration files.  
*See also:* JSON, Filesystem.

---

## Z

### Zero Trust
Security model that assumes no user or device is trusted by default.  
*See also:* Security, MFA.

### ZFS
Advanced filesystem with features like snapshots, compression, and data integrity.  
*See also:* Filesystem, SSD.

---

## Contributing
Missing a term? Add it alphabetically with a short, plain-English definition and optional *See also* links to related pages in this repo.
