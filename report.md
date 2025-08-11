# Packet Analysis Report

## Objective
To capture live network traffic, identify multiple protocols, and analyze their characteristics.

## Capture Overview
- **Date of Capture:** 10 August 2025
- **Duration:** ~1 minute
- **Packets Captured:** 452
- **File:** `capture_session.pcap`

## Observed Protocols
1. **DNS (Domain Name System)**
   - Requests for resolving `wikipedia.org` and other domains.
   - Standard query responses with IPv4 addresses.
   - Example: `Standard query 0x1c29 A wikipedia.org`

2. **TCP (Transmission Control Protocol)**
   - Handshakes and established connections.
   - Port 443 traffic for HTTPS.
   - Example: `TCP 192.168.0.105 → 91.198.174.192 [SYN] Seq=0 Win=64240`

3. **HTTP (HyperText Transfer Protocol)**
   - GET requests to fetch webpage resources.
   - Response headers from servers.
   - Example: `GET /wiki/Main_Page HTTP/1.1`

## Screenshots
### Wireshark Capture Window
![Wireshark Capture Window](screenshots/capture_window.png)

### Protocol Hierarchy
![Protocol Hierarchy](screenshots/protocol_hierarchy.png)

## Filtering Examples
- Show only DNS packets: `dns`
- Show only TCP traffic: `tcp`
- Show HTTP requests: `http`

## Insights
- Most traffic was HTTPS encrypted (TLS over TCP).
- DNS queries were plain text, making them easily identifiable.
- TCP handshakes were clearly visible before secure data transfer.

## Conclusion
The exercise demonstrated how to capture and filter network packets, identify key protocols, and interpret their basic functionality.
