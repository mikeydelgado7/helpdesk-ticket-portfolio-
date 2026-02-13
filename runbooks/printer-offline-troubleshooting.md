# Runbook: Printer Offline / Stuck Print Queue

## Purpose
Restore printing when printer shows Offline or jobs are stuck.

## When to use
- Printer is Offline in Windows
- Print jobs stuck in queue
- User cannot print

## Steps
1. Confirm scope (one user or multiple users).
2. Clear the print queue (cancel stuck jobs).
3. Restart **Print Spooler** service:
- Services → Print Spooler → Restart
4. Verify printer connectivity:
- Confirm printer is powered on and connected to network
- If possible, confirm it is reachable (name/IP)
5. Remove and re-add printer:
- From print server OR add by IP
6. Print a test page.

## If it fails
- Try a different user/computer to confirm scope
- Confirm printer has no hardware error codes
- Check if print server is down (if used)

## Escalation
Escalate to Print Server Admin/Network/Vendor if:
- Printer is unreachable
- Hardware errors present
- Multiple users affected
Provide: printer name, location, IP, error codes, affected users.
