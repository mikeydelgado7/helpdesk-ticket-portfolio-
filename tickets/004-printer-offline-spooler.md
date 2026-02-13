## Ticket
**Ticket #:** 004
**Category:** Printing
**Priority:** P3
**Reported by:** User
**Channel:** Walk-up

### Summary
User’s printer shows “Offline” and print jobs are stuck in the queue.

### Impact / Urgency
- **Impact:** User cannot print required documents (may have alternate printer available).
- **Urgency:** Medium
- **Priority Rationale:** Productivity impacted but not a full outage → P3.

### Environment
- Device / OS: Windows 10/11
- Printer Type: Network printer (via print server or IP)

### Clarifying Questions Asked
- Is it only you or are other users impacted?
- What is the printer name/location?
- Any recent changes (printer moved, network outage, new PC)?

### Troubleshooting & Actions Taken (Timeline)
1. Confirmed printer power/network connection (if accessible) and verified printer display shows ready/no error.
2. Checked Windows printer status and cleared stuck print jobs.
3. Restarted the **Print Spooler** service on the workstation.
4. Verified printer connectivity (reachable by name/IP where applicable).
5. Removed and re-added the printer (from print server or “Add printer by IP”).
6. Printed a test page and re-tested the user’s document.

### Root Cause
Stuck print queue / spooler issue or stale printer connection.

### Resolution
Cleared queue, restarted spooler, and re-added printer connection.

### Validation
- Test page printed successfully.
- User printed the original document without errors.

### Escalation Notes (If Needed)
- **Escalate to:** Print Server Admin / Network Team / Vendor
- **When to escalate:** Printer unreachable on network, hardware error codes, or multiple users impacted (site-wide printing issue).
- **Info to include:** Printer model, location, IP, error codes, number of users affected, timestamps.

### Documentation / Prevention
- Added notes for clearing queue + restarting spooler as first steps.
- (Optional) Add KB article: How to add/reinstall a printer.
