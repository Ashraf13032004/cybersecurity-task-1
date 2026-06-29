# cybersecurity-task-1
# Task 1: Scan Local Network for Open Ports.

## Objective

The objective of this task was to discover active devices and identify open ports on the local network using Nmap.

## Tools Used

* Nmap
* Windows Command Prompt

## Network Range

192.168.56.0/24

## Devices Found

1 active device was discovered:

* 192.168.56.xxx (IP masked for privacy)

## Open Ports Found

| Port | State | Service      |
| ---- | ----- | ------------ |
| 135  | Open  | msrpc        |
| 139  | Open  | netbios-ssn  |
| 445  | Open  | microsoft-ds |

## Commands Used

### Host Discovery

```bash
nmap -sn 192.168.56.0/24
```

### TCP SYN Scan

```bash
nmap -sS 192.168.56.0/24
```

### Save Results

```bash
nmap -sS 192.168.56.0/24 -oN scan_results.txt
```

## Security Observations

* Open ports indicate active network services.
* Port 135 is used for Microsoft RPC services.
* Port 139 is associated with NetBIOS services.
* Port 445 is used for SMB (Windows file sharing).
* Unnecessary open ports should be secured using firewalls and proper access controls.

## Outcome

This task provided hands-on experience with:

* Network reconnaissance
* Host discovery
* Port scanning
* Understanding common network services
* Basic network security assessment

## Author

Ashraf Hussain
