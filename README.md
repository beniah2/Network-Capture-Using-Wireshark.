# Network Capture Using Wireshark.

## Scenario: Hired as a Network Traffic Monitor

You were hired by NetSecure Corp, a mid-size company worried about strange activities on their network. Your mission is to capture live traffic on their router, filter for common protocols, identify insecure transmissions, and document suspicious patterns.

## 1. Setting up the Capture

Story: You arrive at NetSecure Corp’s office. The manager hands you access to their router interface. You fire up your laptop with Kali Linux and get ready to capture live packets.

Action: Start a live capture on the router’s interface.

Command:
sudo wireshark & (Choose the correct network interface, for example eth0 or wlan0)

<img width="1915" height="1007" alt="image" src="https://github.com/user-attachments/assets/53e2c510-ee00-4438-a40b-0b064ea39103" />

## 2. Filtering for HTTP Traffic

Story: While packets fly across the screen, you recall that many attacks target unencrypted HTTP traffic. You apply a filter to zoom in.

Action: Apply a filter to only show HTTP packets.

Command / Filter:
http

<img width="1915" height="988" alt="image" src="https://github.com/user-attachments/assets/573fcfb0-243b-4f50-8ac0-a2872abb8972" />

## 3. Filtering for DNS Queries

Story: You notice the network making hundreds of domain lookups. Some of them might be suspicious or point to malware command-and-control servers.

Action: Filter and review all DNS traffic.

Command / Filter:
dns

<img width="1915" height="989" alt="image" src="https://github.com/user-attachments/assets/370e63d1-2bec-4df8-b764-83f5bfbe44c8" />

## 4. Checking for TCP Credentials

Story: The company still uses an old TCP server. You decide to check.

Action: Filter for TCP traffic.

Command / Filter:
tcp or tcp.port == 21

<img width="1915" height="960" alt="image" src="https://github.com/user-attachments/assets/72370b13-661a-4c2c-8677-7677a3ba5ede" />




