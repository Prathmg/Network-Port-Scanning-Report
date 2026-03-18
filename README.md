# Network-Port-Scanning-Report
The Network Port Scanner GUI is a lightweight and user-friendly cybersecurity tool developed using Python and Tkinter. The primary purpose of this application is to scan a target system (IP address or hostname) and identify open TCP ports within a specified range.

Network Port Scanning Report
📌 1. Objective

The objective of this scan is to identify open TCP ports on the target system and analyze the services running on those ports to assess potential security risks.

📍 2. Target Information

Target IP Address: 192.000.000.000
Scan Range: Ports 1 to 1024
Scan Type: TCP Connect Scan
Tool Used: Python-based Network Port Scanner GUI

⚙️ 3. Methodology

The scan was performed using a multi-threaded port scanner developed in Python. The tool attempts to establish TCP connections to each port in the specified range.
Protocol: TCP
Threads Used: 500
Timeout: 0.5 seconds
Technique: Socket-based connection (connect_ex method)

📊 4. Scan Results
Port	Status	Service
53	Open	DNS (Domain Name System)
110	Open	POP3 (Post Office Protocol v3)
🔍 5. Analysis of Open Ports

🔹 Port 53 – DNS
Responsible for resolving domain names into IP addresses
Essential for network communication and internet access
Open DNS ports may indicate a DNS server running on the system

🔹 Port 110 – POP3
Used for receiving emails from a mail server
Common in legacy email systems

Typically works without encryption unless secured (POP3S uses port 995)

⚠️ 6. Security Implications

Port 53 (DNS):
If misconfigured, it can be exploited for DNS amplification attacks
Open DNS resolvers can be abused for distributed attacks
Port 110 (POP3):
Transmits data in plain text (insecure)
Vulnerable to credential sniffing if not encrypted
May expose email access if not properly secured

🔐 7. Recommendations

Restrict access to port 53 using firewall rules if not publicly required
Ensure DNS server is properly configured and secured
Avoid using POP3; prefer secure alternatives like IMAP over SSL (port 993)
Use encryption (SSL/TLS) for email services
Regularly monitor open ports and disable unused services

✅ 8. Conclusion

The scan identified 2 open ports (53 and 110) on the target system. These ports are associated with DNS and email services, respectively. While they serve important functions, they may pose security risks if not properly configured and secured.
