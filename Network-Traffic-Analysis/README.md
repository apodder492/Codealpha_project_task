# Network Traffic Analysis and Protocol Inspection

A practical cybersecurity project focused on sniffing, capturing, and analyzing live network packets to identify security risks and protocol behaviors using **Wireshark**.

## Project Objectives
* Capture and inspect real-time network packets (HTTP, DNS, TCP).
* Understand the security risks associated with unencrypted (Plain Text) protocols.
* Perform deep packet inspection to analyze protocol headers and payloads.

## Tools Used
* **Wireshark** (Network Protocol Analyzer)
* **tcpdump** (Optional packet capture tool)

## Key Findings & Analysis

### 1. HTTP vs HTTPS Inspection
* **Observation:** Captured standard HTTP traffic and verified that data (including URLs, cookies, and form inputs) is transmitted in clear text.
* **Risk:** Highly vulnerable to Man-in-the-Middle (MitM) sniffing attacks.

### 2. DNS Query Tracking
* **Observation:** Analyzed standard UDP Port 53 traffic to trace website domain resolutions and identified how easily an attacker can map a user's browsing history.


## Mitigation & Recommendation
* Always enforce **HTTPS** using HSTS policies to secure data in transit.
* Implement **DNS over HTTPS (DoH)** or **DNS over TLS (DoT)** to encrypt domain queries.
* Use trusted **VPNs** when accessing public or untrusted Wi-Fi networks.
