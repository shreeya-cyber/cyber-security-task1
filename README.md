# cyber-security-task1
Network port scanning using Nmap

# Task1 - scan local network for open ports

## Objective
Learn how to discover open ports on devices in the local network to understand network exposure.

## Tool used
- Nmap 7.99 (via Zenmap GUI)
  
## Command used 
nmap -sS 192.168.31.0/24

## Devices found 
2 hosts were active out of 256 IPs scanned.

## Scan Results

### Device 1: JioFiber Router (192.168.31.1)
| Port | Service | Description |
|------|---------|-------------|
| 53 | DNS | Domain Name Resolution |
| 80 | HTTP | Unencrypted web interface |
| 443 | HTTPS | Secure web interface |
| 7443 | oracleas-https | Alternative secure port |
| 8080 | HTTP-proxy | Secondary web port |
| 8443 | HTTPS-alt | Alternative HTTPS port |

### Device 2: My PC (192.168.31.30)
| Port | Service | Description |
|------|---------|-------------|
| 135 | MSRPC | Windows RPC service |
| 139 | NetBIOS | Windows file sharing |
| 445 | Microsoft-DS | Windows file sharing |
| 3306 | MySQL | Local database service |

## Security Risks Identified
- Ports 80 open on router - unencrypted, could expose login page
- Ports 8080 open - commonly targeted by attackers
- Ports 3306 (MySQL) open on PC - database exposed on local network 

## What I Learnt 
- How to perfrom TCP SYN scan using nmap
- How to identify open ports and their services 
- How to assess basic security risks from open ports 
