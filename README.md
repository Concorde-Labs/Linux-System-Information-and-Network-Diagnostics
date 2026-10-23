Kali Linux System Information and Network Connectivity Assessment
This project documents a hands-on Linux system administration and network connectivity assessment conducted using a Kali Linux virtual machine. It demonstrates the use of Linux command-line utilities to retrieve system information, examine hardware resources, verify network connectivity, and evaluate network performance through ICMP testing.
Table of Contents
- Project Overview
- Network Topology
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Author
Project Overview
The purpose of this project was to develop practical experience with Linux command-line operations, system inspection, and basic network troubleshooting in a virtualized environment.
The assessment focused on two primary areas:
- System Information: Identifying the current user, hostname, working directory, operating system kernel, available memory, and disk storage.
- Network Connectivity: Testing communication with an external IP address and domain name, evaluating packet transmission, and comparing network response times.
These activities provide foundational skills relevant to IT operations, cybersecurity, and Governance, Risk, and Compliance (GRC), particularly in understanding system environments and verifying network availability.
Network Topology
The assessment was performed using a Kali Linux virtual machine connected to a network with access to external internet resources.
The testing environment consisted of:
- Virtual Machine: Kali Linux
- Username: kali
- Hostname: kali
- Working Directory: /home/kali
- Linux Kernel: 6.19.14+kali-amd64
- Allocated RAM: Approximately 1.91 GiB
- Available Disk Space: Approximately 59 GB
- External IP Tested: 8.8.8.8
- Domain Tested: google.com
The assessment used ICMP echo requests to evaluate connectivity between the Kali Linux virtual machine and external network destinations.
Tools and Technologies
- Kali Linux: Linux distribution used to perform system inspection and connectivity testing.
- Linux Terminal: Command-line interface used to execute administrative and diagnostic commands.
- Virtual Machine: Isolated environment used for the practical exercises.
- ICMP (Internet Control Message Protocol): Protocol used to test connectivity and measure round-trip response times.
- Linux System Utilities: Built-in commands used to retrieve system and hardware information.
Commands Used
- whoami — Identifies the currently logged-in user.
- hostname — Displays the system hostname.
- pwd — Displays the current working directory.
- uname -a — Retrieves operating system and kernel information.
- free -h — Displays system memory information in human-readable format.
- df -h — Displays filesystem disk usage and available storage.
- ping — Tests network connectivity to a specified destination.
- ping -c 2 8.8.8.8 — Sends two ICMP echo requests to a known external IP address.
- ping -c 4 google.com — Sends four ICMP echo requests to a domain name.
Configuration Steps
1. Identify the Current User and System Location
Opened the Kali Linux terminal and executed the following commands:
whoami
hostname
pwd


Results:
- Username: kali
- Hostname: kali
- Current working directory: /home/kali
These commands confirmed the active user account, system identity, and current directory.
2. Retrieve Operating System and Hardware Information
Executed the following commands to inspect the virtual machine:
uname -a
free -h
df -h


Results:
- uname -a identified the running Linux kernel as 6.19.14+kali-amd64.
- free -h indicated approximately 1.91 GiB of total RAM.
- df -h showed approximately 59 GB of available disk space on the main filesystem.
These findings provided an overview of the virtual machine's operating environment and available resources.
3. Test Connectivity to a Known IP Address
Executed the command:
ping -c 2 8.8.8.8


The -c 2 option instructed the system to transmit two ICMP echo requests before stopping automatically.
Results:
- Packets transmitted: 2
- Packets received: 2
- Packet loss: 0%
- Average round-trip time: 26.494 ms
The successful responses confirmed that the virtual machine could communicate with the external IP address 8.8.8.8.
4. Test Connectivity Using a Domain Name
Executed the command:
ping -c 4 google.com


The -c 4 option instructed the system to transmit four ICMP echo requests before terminating.
Results:
- Domain tested: google.com
- Resolved IP address: 142.250.139.138
- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Average round-trip time: 80.973 ms
The successful responses demonstrated that the virtual machine could resolve a domain name to an IP address and communicate with the destination.
5. Compare Network Response Times
Compared the average round-trip times recorded during both connectivity tests.
Destination	Packets Sent	Packet Loss	Average RTT
8.8.8.8	2	0%	26.494 ms
google.com	4	0%	80.973 ms
The domain-based test recorded a higher average response time than the direct IP test.
One notable observation was that the first response from google.com took approximately 244 ms, while subsequent responses ranged between approximately 25–28 ms.
The unusually high initial response contributed to the higher average round-trip time. A temporary network delay was identified as a possible explanation, although the test did not establish its exact cause.
Results and Findings
The assessment successfully demonstrated the use of Linux utilities for system inspection and basic network diagnostics.
Key Findings
- System Identification: Successfully retrieved the active username, hostname, and working directory.
- Hardware Visibility: Identified available memory and disk resources within the Kali Linux virtual machine.
- Operating System Information: Confirmed the running Linux kernel version.
- IP Connectivity: Successfully established communication with 8.8.8.8, recording 0% packet loss.
- DNS Resolution: Successfully resolved google.com to 142.250.139.138.
- Network Availability: Both connectivity tests returned successful responses without packet loss.
- Latency Analysis: Identified a difference in average response times and examined the effect of an unusually slow initial response.
Skills Demonstrated
- Linux command-line navigation
- System information gathering
- Hardware resource inspection
- Basic network troubleshooting
- ICMP connectivity testing
- DNS resolution verification
- Network latency analysis
- Technical documentation and reporting
Conclusion
This project strengthened practical understanding of Linux system administration and fundamental network troubleshooting techniques.
Through the use of built-in Linux utilities, I successfully inspected a virtualized operating environment, verified connectivity to external destinations, and analyzed network performance using packet loss and round-trip time measurements.
The exercise established a foundation for more advanced cybersecurity activities, including network monitoring, vulnerability assessment, security auditing, and infrastructure risk assessment.

Author: Concord Ekwonna

Project Date: August 26, 2026

Focus Areas: Information Security | Network Fundamentals | Linux Administration
