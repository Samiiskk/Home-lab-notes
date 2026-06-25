# Day 03 — Wazuh SIEM Installation

**Date:** June 26, 2026
**Status:** - Complete

---

## Wazuh Details
- **Version:** Wazuh 4.7
- **Installed on:** Ubuntu Server 22.04
- **Dashboard URL:** https://192.168.248.138
- **Username:** admin

---

## System Requirements Met
| Resource | Required | Available |
|----------|----------|-----------|
| RAM | 2GB minimum | 3.8GB ✅ |
| Disk | 10GB minimum | 6.1GB free ✅ |

---

## Installation Steps
```bash
# Step 1 — Download Wazuh installer
wget https://packages.wazuh.com/4.7/wazuh-install.sh

# Step 2 — Run all-in-one installer
sudo bash wazuh-install.sh -a

# Step 3 — Get credentials
sudo cat wazuh-install-files/wazuh-passwords.txt
```

---

## What Gets Installed
- Wazuh Manager — receives and analyzes logs
- Wazuh Indexer — stores and indexes data
- Wazuh Dashboard — web-based visualization UI

---

## Accessing Dashboard
1. Open browser in Kali Linux
2. Navigate to: `https://192.168.248.138`
3. Accept security certificate warning
4. Login with admin credentials

---

## Dashboard Features
- Security events — browse security alerts
- Integrity monitoring — file change alerts
- Policy monitoring — security policy compliance
- System auditing — user behavior monitoring
- Vulnerability detection — CVE scanning
- Threat intelligence — IOC matching

---

## Architecture
[Kali Linux Browser]

|

| HTTPS

↓

[Ubuntu Server 22.04]

└── Wazuh Manager

└── Wazuh Indexer

└── Wazuh Dashboard

|

| Agent communication

↓

[Endpoints to monitor]

---

## Next Steps
- [ ] Add Kali Linux as Wazuh agent
- [ ] Add Ubuntu as Wazuh agent
- [ ] Monitor first security alerts
- [ ] Run Nmap scan from Kali → observe in dashboard
- [ ] Set up custom detection rules
