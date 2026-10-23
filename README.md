Linux System Information & Network Diagnostics
A practical examination of Linux system configuration, hardware resources, and network connectivity in a Kali Linux virtual machine. The project documents command-line diagnostics, captured terminal evidence, and observed network performance.
Table of Contents
- Project Overview
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Security Relevance
- Author
Project Overview
This project examines a Kali Linux virtual machine using built-in Linux commands. The work covers identification of the active user and working directory, inspection of operating system and hardware information, review of memory and disk usage, and testing of connectivity to a public IP address and a domain name.
Scope: Local system inspection and basic network diagnostics. No penetration testing, vulnerability scanning, or security audit was performed.
Tools and Technologies
- Kali Linux — Linux operating system used for the tests
- Linux terminal — command-line interface for system inspection
- Virtual machine — environment hosting Kali Linux
- ping — ICMP connectivity and round-trip-time testing
- Linux utilities — whoami, hostname, pwd, uname, lscpu, free, df, and uptime
Configuration Steps
1. Verify system identity and working directory
Executed:
whoami
hostname
pwd
The commands returned kali as the username, kali as the hostname, and /home/kali as the working directory.

2. Inspect the operating system and CPU
Executed:
uname -a
lscpu
The uname -a output identified the running Linux kernel as 6.19.14+kali-amd64. The lscpu output provided processor architecture and CPU configuration details for the virtual machine.

3. Review memory and disk resources
Executed:
free -h
df -h
The VM reported approximately 1.9 GiB of total memory. The disk report showed approximately 59 GB of available space on the main filesystem, as recorded in the project report.

4. Check system uptime
Executed:
uptime
The command displayed the system's running time, active user count, and load averages at the time of inspection.

5. Test connectivity to a known IP address
Executed:
ping -c 2 8.8.8.8
Results: 2 packets transmitted, 2 received, 0% packet loss, and 26.494 ms average round-trip time. This demonstrated reachability to the tested IP address during the measurement.

6. Test connectivity and name resolution for a domain
Executed:
ping -c 4 google.com
Results: The domain resolved to 142.250.139.138 during the test. All 4 packets were received with 0% packet loss, and the average round-trip time was 80.973 ms.

Results and Findings
Diagnostic area	Observation
Active user / hostname	kali / kali
Working directory	/home/kali
Linux kernel	6.19.14+kali-amd64
Total memory	Approximately 1.9 GiB
Main filesystem available space	Approximately 59 GB, as documented in the report
IP ping to 8.8.8.8	2/2 received; 0% loss; 26.494 ms average
Domain ping to google.com	4/4 received; 0% loss; 80.973 ms average
Domain resolution	142.250.139.138 at test time


The domain test's higher average latency was influenced by an initial response of approximately 244 ms, while the subsequent responses were approximately 25–28 ms. The cause of this first-response delay was not established by the test.
Both ping tests succeeded during the observed test window. These results show reachability and successful domain resolution for the tested destinations, but do not establish overall network reliability or security.
Security Relevance
- System visibility: Identifying the active user, host, kernel, and resources provides a starting point for operational review and troubleshooting.
- Network diagnostics: Comparing IP-based and domain-based ping tests helps distinguish basic reachability checks from name-resolution checks.
- Evidence-based reporting: Terminal screenshots and recorded measurements support reproducible documentation of observed system behavior.
Author
Concord Ekwonna
