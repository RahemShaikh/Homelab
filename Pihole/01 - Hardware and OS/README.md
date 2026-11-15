# 01 - Hardware and OS

## Overview
Prepare and provision a Raspberry Pi for use as a dedicated Pi-hole DNS server.

## Hardware
- **Device:** Raspberry Pi 3B+
- **Storage:** 32GB SDHC
- **Network:** Ethernet Cat-6

## Raspberry Pi Imager

Used Raspberry Pi Imager to install Raspberry Pi OS onto the SD card.

### Configuration

| Setting | Configuration |
|---|---|
| Operating System | Raspberry Pi OS Lite 64 bit|
| Hostname | `pihole` |
| Username | `homelab` |
| SSH | Enabled |
| Network Connection | Ethernet |
| Raspberry Pi Connect | Disabled |

## Imager

![Raspberry Pi Imager](Images/pi-imaging.png)

## Initial Access

After imaging the SD card, the Raspberry Pi was connected to the network through Ethernet and powered on.

SSH was used to remotely access the device from a Windows machine.

**SSH Command:**

```bash
ssh homelab@pihole
```

The device was successfully accessed using its hostname.

![SSH Remote Access](images/ssh.png)

## Verification

The following commands were used to verify the initial setup:

| Command | Purpose |
|---|---|
| `hostname` | Verify device hostname |
| `whoami` | Verify logged-in user |

## What I Learned

- How to provision a Raspberry Pi using Raspberry Pi Imager.
- How to configure a hostname and user account during initial setup.
- How to enable SSH for headless administration.
- How to remotely access a Linux device using its hostname.
