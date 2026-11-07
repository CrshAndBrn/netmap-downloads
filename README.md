# NETMAP // LOCAL SECURITY CONSOLE

A local security console for one Windows PC and its home network, styled as a lo-fi 80s amber CRT terminal. No cloud, no accounts, no subscriptions.

**This repository holds downloads only. The source code is not public.**

## Download
1. Open the [Releases page](../../releases) and pick the newest one.
2. Download `NetMap-<version>-windows-x64.zip`.
3. Unzip it and run `NetMap.exe`. Python isn't needed.

**Windows may warn you the first time**, because the app isn't code-signed. If you trust this download, choose **More info**, then **Run anyway**. Each release lists a SHA-256 checksum so you can check your copy:

```
Get-FileHash NetMap-<version>-windows-x64.zip -Algorithm SHA256
```

NetMap is a beta, so expect some rough edges.

## What it does
- **SOC // LIVE:** live traffic, connections and recent alerts
- **ALERTS:** baseline rules with offline MITRE ATT&CK mapping
- **NETWORK MAP:** a 3D map and inventory of devices on your network
- **EVENTS:** a Windows event timeline and reports
- **CONNECTIONS:** live sockets, listening services and process checks
- **PERSISTENCE:** startup items, scheduled tasks and services
- **TRUSTED:** a reviewed allowlist
- **NETWORK VAULT:** a history of each network you join
- **ACTIVE DEFENSE:** local honeypots, bait files, firewall blocking and self-audits

## Privacy and ground rules
- Your data stays on your PC, in `%LOCALAPPDATA%\NetMap`. Nothing is uploaded.
- Online look-ups only open in your browser when you click them.
- It only scans your own local subnet. Port checks are opt-in, rate-limited and limited to that subnet.
- Nothing attacks anything outside your network. Only use NetMap on networks you own or have permission to test.
- Features that need admin rights say so and ask first.

## Licence
Free to download and use. See [LICENSE](LICENSE). Copying, reselling or redistributing NetMap isn't allowed.
