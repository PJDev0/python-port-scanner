Python Port Scanner

A high-performance, multi-threaded port scanner developed in Python. This tool assists in network reconnaissance by identifying open ports and grabbing service banners.

Legal Disclaimer

This tool is for educational purposes ONLY. Network scanning without explicit permission is illegal in many jurisdictions. Do NOT scan networks you do not own or have written permission to test. The author assumes no liability for misuse of this software.


Features:

    Concurrent Scanning: Uses Python's ThreadPoolExecutor to scan hundreds of ports simultaneously.
    Banner Grabbing: Attempts to retrieve server information (e.g., Apache, Nginx, OpenSSH) from open ports.
    Flexible Input: Supports port ranges (e.g., 1-1024) and specific port lists (e.g., 80,443).
    Robust Error Handling: Handles unexpected disconnections and invalid data gracefully without crashing.

Installation:

No external dependencies are required. This uses the Python Standard Library.

git clone https://github.com/PJDev0/python-port-scanner.git







Usage:

Scan Localhost; 
python scanner.py -t 127.0.0.1 -p 1-1000


Scan a Specific Server on Common Ports;
python scanner.py -t 192.168.1.1 -p 80,443,8080,22




Arguments
| Argument | Required | Description |
|----------|----------|-------------|
| `-t, --target` | Yes | Target IP address or hostname |
| `-p, --ports` | No | Port range (default: 1-1024) |



Example Output

[*] Starting Scan...
[*] Target: 127.0.0.1
[*] Ports: 1-100
--------------------------------------------------
[+] Port 22 is OPEN
     Banner: SSH-2.0-OpenSSH_8.2p1 Ubuntu-4ubuntu0.5
[+] Port 80 is OPEN
--------------------------------------------------
Scan complete! Found 2 open ports.

Author
Created by PJDev0



