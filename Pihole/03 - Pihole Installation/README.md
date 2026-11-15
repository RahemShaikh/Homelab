# 03 - Pi-hole Installation

## Overview

Install and configure Pi-hole on the Raspberry Pi to provide DNS-based ad and tracker blocking for devices on the local network.

## System Updates

Before installing Pi-hole, the Raspberry Pi operating system was updated to ensure the latest available package information and software updates were installed.

**Commands:**

```bash
sudo apt update
sudo apt upgrade
```

- `apt update` – Refreshes the local package lists.
- `apt upgrade` – Installs available package updates.

## Pi-hole Installation

With the operating system and network configuration complete, Pi-hole was installed using its official installation script.

**Command:**

```bash
curl -sSL https://install.pi-hole.net | bash
```

The installation script launches an interactive setup wizard that guides the configuration process.

## Pi-hole Configuration

The following settings were selected during the installation wizard:

| Setting | Configuration |
|---|---|
| Network Interface | `eth0` |
| Upstream DNS Provider | Google (ECS, DNSSEC) |
| Blocklist | StevenBlack |
| Query Logging | Enabled |
| Privacy Level | 0 (Show Everything) |

### Configuration Details

- **Network Interface (`eth0`):** Ethernet interface used by Pi-hole to communicate with the local network.
- **Upstream DNS:** Google DNS was selected to resolve DNS queries forwarded by Pi-hole.
- **Blocklist:** StevenBlack was selected to filter requests to known advertising and tracking domains.
- **Query Logging:** Enabled to record DNS queries and allow them to be inspected through the dashboard.
- **Privacy Level:** Set to 0, allowing all query information to be displayed in Pi-hole.

## Installation Completion

After completing the installation wizard, Pi-hole displayed a confirmation screen containing the installation details and web interface information.

![Pi-hole Installation Completion](Images/complete-install-pihole.png)

The installation was successfully completed, and the Pi-hole web administration interface was made available for further configuration and monitoring.

## Verification

The following commands were used to verify the installation and manage Pi-hole:

| Command | Purpose |
|---|---|
| `pihole -v` | Display installed Pi-hole component versions |
| `pihole setpassword` | Set or change the Pi-hole web interface password |
| `pihole status` | Display the current Pi-hole blocking status |

## What I Learned

- How to update and upgrade packages on a Debian-based Linux operating system.
- How to install Pi-hole using its official installation script.
- How to configure an upstream DNS provider.
- How query logging provides visibility into DNS traffic.
- How to manage and verify Pi-hole through Linux terminal commands.