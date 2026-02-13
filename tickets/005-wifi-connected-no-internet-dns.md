## Ticket
**Ticket #:** 005
**Category:** Network
**Priority:** P2
**Reported by:** User
**Channel:** Phone

### Summary
User is connected to Wi-Fi but cannot access websites; apps report no internet.

### Impact / Urgency
- **Impact:** User cannot access web-based tools/email; work blocked.
- **Urgency:** High
- **Priority Rationale:** User unable to work online → P2.

### Environment
- Device / OS: Windows 10/11 laptop
- Connection: Wi-Fi (on-site or home)
- Network: LAN/VPN (if remote, may require VPN after internet restored)

### Clarifying Questions Asked
- Are other devices on the same Wi-Fi working?
- Are you on-site or remote?
- Are you connected to VPN right now?
- What exact message do you see (browser/app)?

### Troubleshooting & Actions Taken (Timeline)
1. Confirmed Wi-Fi is connected and signal strength is adequate; toggled Wi-Fi off/on.
2. Checked network configuration using `ipconfig /all` (IP, gateway, DNS).
3. Tested connectivity to isolate the layer of failure:
- Ping default gateway (local network)
- Ping a public IP (internet path without DNS)
- `nslookup` a known domain (DNS resolution)
4. If gateway ping failed: renewed IP (`ipconfig /release` then `/renew`) and checked DHCP connectivity.
5. If public IP worked but DNS failed: flushed DNS (`ipconfig /flushdns`) and restored known-good DNS settings (per policy).
6. Restarted device and re-tested browsing and required apps.

### Root Cause
DNS misconfiguration or stale network configuration (determined by ping/nslookup results).

### Resolution
Restored working network/DNS settings and confirmed internet connectivity.

### Validation
- User can browse websites successfully.
- User can access required apps; VPN connects if needed for company resources.

### Escalation Notes (If Needed)
- **Escalate to:** Network Team (on-site) or ISP/Home router support (remote)
- **When to escalate:** Multiple users impacted, DHCP/AP outage suspected, or network equipment issue.
- **Info to include:** Location/SSID, IP info, gateway/public IP/nslookup results, timestamps, affected user count.

### Documentation / Prevention
- Documented a repeatable “gateway vs internet vs DNS” test process for faster triage.
