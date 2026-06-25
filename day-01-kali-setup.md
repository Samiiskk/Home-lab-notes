# Day 01 — Kali Linux VM Setup

**Date:** June 23, 2026
**Status:** - Complete

---

## VM Details
- **OS:** Kali Linux 2026.1
- **Hypervisor:** VMware Workstation 17 Player
- **Location:** D:\Kali\kali-linux-2026.1
- **Username:** kali
- **Password:** kali
- **IP Address:** 192.168.248.136

---

## Setup Steps Completed
1. Downloaded Kali Linux 2026.1 VMware image
2. Extracted to D:\Kali\
3. Opened .vmx file in VMware Workstation 17 Player
4. Powered on VM — booted successfully
5. VMware Tools already pre-installed
6. Logged in with kali/kali credentials

---

## Commands Tested
```bash
whoami        # returns: kali
ifconfig      # shows IP: 192.168.248.136
```

---

## Tools Available in Kali
- Nmap — network scanning
- Wireshark — packet analysis
- Metasploit — exploitation framework
- Burp Suite — web application testing
- Hydra — password cracking
- Gobuster — directory enumeration

---

## Next Steps
- [x] Install Ubuntu Server VM
- [x] Set up SSH between VMs
- [x] Install Wazuh SIEM
- [ ] Run first Nmap scan
- [ ] Add agents to Wazuh
