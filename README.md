# Week 1 – Kali Linux Attacker Machine Setup

## Overview
This project sets up the base of a penetration-testing lab. It uses VirtualBox
as the virtualization platform and Kali Linux as the attacking (hacker) machine,
connected through a dedicated NAT Network.

## Objectives
- Use VirtualBox (latest recommended version) as the hypervisor
- Set up Kali Linux as the attacker machine
- Configure a NAT Network with the subnet 10.0.0.0/24
- Enable bidirectional clipboard and drag & drop between host and VM
- Enable a shared folder (/downloads) from the host machine
- Assign Kali Linux the static IP address 10.0.0.2/24
- Verify full Internet access from the Kali VM

## Lab Configuration

| Setting            | Value                                                      |
|--------------------|------------------------------------------------------------|
| Hypervisor         | VirtualBox (latest recommended)                            |
| Guest OS           | Kali Linux                                                 |
| Kali version       | 2026.3                                                     |
| Role               | Attacker / hacker machine                                  |
| IP configuration   | Manual (static)                                            |
| Gateway            | 10.0.0.1                                                   |
| DNS server         | 8.8.8.8                                                    |
| Network type       | NAT Network                                                |
| Subnet             | 10.0.0.0/24                                                |
| Kali IP address    | 10.0.0.2/24                                                |
| Clipboard          | Bidirectional                                              |
| Drag & Drop        | Bidirectional                                              |
| Shared folder      | \Downloads\kali-linux-2026.3-virtualbox-amd64 (from host)  |
| Internet access    | Full                                                       |

## Setup Summary
1. Installed the latest recommended version of VirtualBox.
2. Created a NAT Network in VirtualBox with the CIDR 10.0.0.0/24.
3. Created the Kali Linux VM and attached it to the NAT Network.
4. Enabled shared clipboard and drag & drop in the VM settings.
5. Configured a shared folder pointing to the host's /downloads directory.
6. Set the Kali IP address to 10.0.0.2/24.
7. Verified connectivity (e.g., `ip a`, `ping 8.8.8.8`).

## Verification
- [x] Kali shows IP 10.0.0.2/24
- [x] Internet reachable (ping by IP and by domain name)
- [x] Clipboard copy/paste works between host and VM
- [x] File drag & drop works
- [x] Shared /downloads folder is accessible from Kali

## Screenshots

### 1. NAT Network (10.0.0.0/24)
![NAT Network](screenshots/01-nat-network.png)

### 2. VM network adapter
![VM network adapter](screenshots/02-vm-network-adapter.png)

### 3. Clipboard and drag & drop enabled
![Clipboard and drag drop](screenshots/03-clipboard-dragdrop.png)

### 4. Shared folder (/downloads)
![Shared folder](screenshots/04-shared-folder.png)

### 5. Kali IP address (10.0.0.2/24)
![Kali IP address](screenshots/05-kali-ip-address.png)

### 6. Internet access test
![Ping test](screenshots/06-internet-ping.png)

## Notes
This environment is for educational and authorized security testing only.
