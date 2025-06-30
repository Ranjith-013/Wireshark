# 🧪 Wireshark Packet Capture Lab

This lab demonstrates how to use **Wireshark** to capture and analyze network packets across various protocols such as **DNS, ICMP, HTTP, TLS**, and **TCP**.

---

## Step-by-Step Instructions

### 1. Install Wireshark
- Download from: [https://www.wireshark.org/download.html](https://www.wireshark.org/download.html)
- Install using default options.
  - On Windows, ensure **Npcap** or **WinPcap** is selected during installation.


### 2. Start Capturing on Active Network Interface
- Launch **Wireshark**.
- Identify the **active interface** (the one showing active traffic).
- **Double-click** the interface to begin capturing.


### 3. Generate Network Traffic
Open:
- A browser → visit `https://example.com`
- Command Prompt → run:
  ping google.com
## 4. Stop the Capture
Let it run for ~1 minute.

Click the red square Stop button in Wireshark to end the capture.

## 5. Apply Protocol Filters
In the Display Filter bar, use these filters to isolate traffic:

## wireshark

dns      // Domain Name System traffic
http     // Hypertext Transfer Protocol (non-HTTPS)
icmp     // Internet Control Message Protocol (ping)
tcp      // Transmission Control Protocol
tls      // Encrypted traffic (HTTPS)
udp      // User Datagram Protocol
Apply one at a time to explore packet types.

## 6. Identify at Least 3 Protocols
Based on browsing + ping traffic, you should see:

## Protocol	Description
DNS	Resolves domain names (e.g., google.com)
ICMP	Echo Request/Reply used by ping
TCP	Manages connections (SYN, ACK, FIN)
HTTP	Web traffic (GET/POST on port 80)
TLS	Encrypted HTTPS traffic (port 443)
UDP	Lightweight transport (e.g., DNS queries)

## Sample Protocol Analysis
Protocol	Packet Details Example
DNS	Standard query 0x1234 A google.com
ICMP	Echo request → 8.8.8.8, Echo reply ← 8.8.8.8
TCP	SYN → SYN-ACK → ACK (3-way handshake)
HTTP	GET / HTTP/1.1 Host: example.com
TLS	Client Hello, Server Hello, Certificate Exchange

## Notes
Use "Follow TCP Stream" to view complete HTTP conversations.

Use "Statistics > Protocol Hierarchy" for protocol summary.

Export captures as .pcap using File > Export Specified Packets.

## Useful Resources
Wireshark Docs

Wireshark Display Filters Reference

Task Completed: Identified 3+ protocols, captured and analyzed packet types using Wireshark.


---

Let me know if you'd like this as a downloadable `.md` file or want to include screenshots of filtered packets.
