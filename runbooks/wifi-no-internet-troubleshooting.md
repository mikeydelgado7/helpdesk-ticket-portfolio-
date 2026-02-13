# Runbook: Wi-Fi Connected But No Internet (Gateway vs DNS)

## Purpose
Quickly isolate whether the issue is Wi-Fi signal, DHCP/gateway, internet path, or DNS.

## Steps
1. Confirm Wi-Fi connected and signal is strong.
2. Run `ipconfig /all` and verify:
- IP address
- Default gateway
- DNS servers
3. Test:
- Ping default gateway (local network)
- Ping a public IP (internet without DNS)
- `nslookup` a known domain (DNS resolution)
4. Based on results:
- Gateway ping fails → DHCP/Wi-Fi/router issue
- Public IP works but DNS fails → DNS issue
5. Fix common items:
- Renew IP: `ipconfig /release` then `ipconfig /renew`
- Flush DNS: `ipconfig /flushdns`
6. Restart device and retest.

## Escalation
Escalate to Network Team/ISP if:
- Multiple users impacted
- DHCP/AP outage suspected
Include: SSID, location, IP info, ping/nslookup results, timestamps.
