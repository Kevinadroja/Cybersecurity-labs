title:                   "Nmap Basic Scan - Metasploitable 2"
target_ip:          192.168.56.102
environment:    "Kali Linux (Host), Metasploitable2 (VM), VirtualBox Host-Only                                        Network"

--------------------------------------------------------

1. Title :-
   Nmap Basic Scan - Metasploitable 2

2. Objectives :-
   - Learn host discovery using Nmap.
   - Enumerate open ports and running services.
   - Identify operating system and software versions.
   - Perform vulnerability scanning using NSE scripts.

3. Environment & Setup :-
   - Host OS: Windows 10
   - Attacker VM: Kali Linux (VirtualBox)
   - Target VM: Metasploitable 2 (VirtualBox)
   - Network: Host-Only (192.168.56.0/24)
   - Tool: Nmap
   - Target IP: 192.168.56.102

4. Date & Time :-
   - Start : 04-12-2025 18:22 IST
   - End   : 

5. Commands Executed :-

   A. Host Discovery:
      - ping 192.168.56.102

   B. TCP Scans:
      - sudo nmap -sS 192.168.56.102           (SYN Stealth Scan)
      - nmap -sT 192.168.56.102                (TCP Connect Scan)
      - sudo nmap -sS -p- 192.168.56.102       (Full TCP Port Scan - 1 to 65535)

   C. UDP Scan:
      - sudo nmap -sU 192.168.56.102           (UDP Port Scan)

   D. ACK Scan:
      - sudo nmap -sA 192.168.56.102           (Firewall/Filter Detection)

   E. Version Detection:
      - nmap -sV 192.168.56.102

   F. OS Detection:
      - sudo nmap -O 192.168.56.102

   G. NSE Script Scans:
      1. Default Scripts:
         - sudo nmap -sC -sV 192.168.56.102
      2. FTP Anonymous Check:
         - nmap --script ftp-anon -p21 192.168.56.102
      3. SMB OS Discovery:
         - nmap --script smb-os-discovery -p445 192.168.56.102
      4. SMB Share Enumeration:
         - nmap --script smb-enum-shares -p445 192.168.56.102
      5. HTTP Directory Enumeration:
         - nmap --script http-enum -p80 192.168.56.102
      6. Vulnerability Scan:
         - nmap --script vuln 192.168.56.102
      7. Heartbleed Check (if SSL present):
         - nmap --script ssl-heartbleed -p443 192.168.56.102
6. Output :
