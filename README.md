# NETMAP // LOCAL SECURITY CONSOLE

A local security console for one Windows or Linux PC and its home network, styled as a lo-fi 80s amber CRT terminal. No cloud, no accounts, no subscriptions.

**This repository holds downloads only. The source code is not public.**

## Download
Open the [Releases page](../../releases), pick the newest one, and download the file for your system. Python isn't needed.

| System | File | How to run |
|---|---|---|
| Windows 10 / 11 | `NetMap-<version>-windows-x64.zip` | Unzip it and run `NetMap.exe` |
| Ubuntu 22.04+, Debian 12+, Mint 21+ | `netmap-soc_<version>_amd64.deb` | `sudo apt install ./netmap-soc_<version>_amd64.deb`, then open NetMap from the app menu or run `netmap` |
| Other 64-bit Linux (2022 or newer) | `NetMap-<version>-linux-x64.tar.gz` | `tar -xzf NetMap-<version>-linux-x64.tar.gz`, then `sh NetMap/install.sh` (no root needed; `sh NetMap/uninstall.sh` removes it) |

**Windows may warn you the first time**, because the app isn't code-signed. If you trust this download, choose **More info**, then **Run anyway**.

Each release lists SHA-256 checksums so you can check your copy:

```
Get-FileHash NetMap-<version>-windows-x64.zip -Algorithm SHA256     # Windows (PowerShell)
sha256sum netmap-soc_<version>_amd64.deb                            # Linux
```

On Linux, install `tcpdump` if you want the PACKET CAPTURE tab (for example `sudo apt install tcpdump`).

NetMap is a beta, so expect some rough edges. The Linux version is new.

## What it does
- **SOC // LIVE:** live traffic, connections and recent alerts
- **ALERTS:** baseline rules with offline MITRE ATT&CK mapping
- **NETWORK MAP:** a 3D map and inventory of devices on your network
- **EVENTS:** a security event timeline and reports (Windows event logs, or the Linux system journal)
- **CONNECTIONS:** live sockets, listening services and process checks
- **PERSISTENCE:** startup items, scheduled tasks and services (on Linux: cron jobs, timers, services and autostart entries)
- **TRUSTED:** a reviewed allowlist
- **NETWORK VAULT:** a history of each network you join
- **ACTIVE DEFENSE:** local honeypots, bait files, firewall blocking and self-audits
- **PACKET CAPTURE:** record this PC's own traffic (needs admin / root) and read captures with colour-coded protocols and Wireshark-style detail

## Privacy and ground rules
- Your data stays on your PC: `%LOCALAPPDATA%\NetMap` on Windows, `~/.local/share/NetMap` on Linux. Nothing is uploaded.
- A new install starts with a blank account and never uses your system account name.
- Online look-ups only open in your browser when you click them.
- It only scans your own local subnet. Port checks are opt-in, rate-limited and limited to that subnet.
- Nothing attacks anything outside your network. Only use NetMap on networks you own or have permission to test.
- Features that need admin or root rights say so and ask first.

## Licence
Free to download and use. See [LICENSE](LICENSE). Copying, reselling or redistributing NetMap isn't allowed.
