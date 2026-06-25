# Day 02 — Ubuntu Server VM Setup & SSH Connection

**Date:** June 25, 2026
**Status:** - Complete

---

## VM Details
- **OS:** Ubuntu Server 22.04.5 LTS
- **Kernel:** Linux 5.15.0-181-generic x86_64
- **Hypervisor:** VMware Workstation 17 Player
- **Location:** D:\virtualB\Ubuntu
- **Username:** meowwie
- **IP Address:** 192.168.248.138
- **Disk:** 9.75GB allocated
- **RAM:** 3.8GB

---

## Installation Steps
1. Downloaded Ubuntu Server 22.04.5 ISO
2. Created new VM in VMware (30GB disk, single file)
3. Booted Ubuntu ISO — selected "Try or Install Ubuntu Server"
4. Continued without updating installer
5. Configured guided storage — entire disk with LVM
6. Installation completed successfully
7. Reset password via GRUB recovery mode
8. Successfully logged in

---

## Post-Installation Steps
1. Updated package list: `sudo apt update`
2. Upgraded packages: `sudo apt upgrade -y`
3. Removed unused packages: `sudo apt autoremove -y`
4. Rebooted to apply updates

---

## SSH Setup
```bash
# Install SSH server on Ubuntu
sudo apt install openssh-server -y

# Verify SSH is running
sudo systemctl status ssh
# Result: active (running) ✅
```

---

## SSH Connection from Kali → Ubuntu
```bash
# Run this from Kali terminal
ssh meowwie@192.168.248.138

# Accept fingerprint: yes
# Enter Ubuntu password
# Result: Successfully connected ✅
```

---

## Commands Tested
```bash
whoami          # returns: meowwie
uname -a        # shows kernel version
ip a            # shows IP: 192.168.248.138
free -h         # RAM: 3.8GB total, 3.3GB free
df -h           # Disk: 9.8GB total, 6.1GB free
```
[Kali Linux]              [Ubuntu Server]

192.168.248.136  ──SSH──► 192.168.248.138

---

## Next Steps
- [x] Install Wazuh SIEM on Ubuntu
- [ ] Add Kali as Wazuh agent
- [ ] Run first Nmap scan from Kali
---

## Network Setup
