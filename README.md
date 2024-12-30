# CodeAlpha--Network-Intrusion-Detection-System
In this project, I use Wireshark to monitor network traffic and apply filters to detect various types of attacks, including:

Port Scanning (SYN Flood)
Data Exfiltration (Large Packet Detection)
ARP Spoofing (Duplicate ARP Messages)
Denial of Service (DoS) (TCP Retransmissions)
ICMP Flooding (Ping-based DoS Attack)
The project demonstrates how these attacks can be detected using packet capture tools and how to filter and analyze traffic to uncover suspicious activities.

Filters Used
tcp.flags == 0x02: Detects SYN packets, commonly used in port scanning.
frame.len > 1500: Detects large packets that might signal data exfiltration attempts.
arp.duplicate-address-detected: Identifies ARP spoofing attacks by detecting duplicate ARP messages.
tcp.analysis.retransmission: Detects frequent TCP retransmissions, potentially signaling a DoS attack.
icmp: Captures ICMP traffic, helping detect potential DoS attacks like ICMP floods.
How to Use This Repository
Clone or Download: Clone or download the repository to access the Wireshark capture file.
bash
Copy code
git clone https://github.com/yourusername/network-intrusion-detection-with-wireshark.git
Install Wireshark: Ensure that you have Wireshark installed on your system. You can download it from the official Wireshark website.
Open the Capture File: Open the .pcap Wireshark capture file provided in this repository using Wireshark.
Apply Filters: Apply the mentioned filters in the Wireshark display filter bar to detect potential intrusions or suspicious activity.
Video Demonstration
A video demonstrating how to use the filters in action and how they help identify network intrusions is available. Watch the video to understand the practical application of the filters.

Watch the Video https://www.linkedin.com/posts/mariana-masry_cybersecurity-wireshark-networksecurity-activity-7279574476567056385-1mbi?utm_source=share&utm_medium=member_desktop
