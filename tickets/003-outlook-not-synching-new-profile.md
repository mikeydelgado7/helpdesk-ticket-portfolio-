## Ticket
**Ticket #:** 003
**Category:** Email (Outlook / Microsoft 365)
**Priority:** P3
**Reported by:** User
**Channel:** Email

### Summary
User reports Outlook is not syncing and shows outdated emails.

### Impact / Urgency
- **Impact:** Email delayed in Outlook desktop; user can still access webmail.
- **Urgency:** Medium
- **Priority Rationale:** Work impacted but workaround exists → P3.

### Environment
- Device / OS: Windows 10/11
- Email Client: Outlook Desktop (Microsoft 365)
- Network: LAN/VPN/Wi-Fi

### Clarifying Questions Asked
- Does Outlook Web (webmail) work?
- What does Outlook status show (Disconnected / Trying to connect / Working Offline)?
- When did this start?
- Any recent password change or MFA prompt?

### Troubleshooting & Actions Taken (Timeline)
1. Confirmed webmail access works (isolates client issue vs account/service outage).
2. Checked Outlook “Work Offline” setting and connection status.
3. Restarted Outlook and tested Send/Receive.
4. Verified credentials/MFA prompts completed successfully.
5. Created a new Outlook profile (Control Panel → Mail → Show Profiles) and re-added mailbox.
6. Allowed mailbox to complete initial sync and verified Cached Exchange Mode settings.

### Root Cause
Corrupted Outlook profile or client sync state causing Send/Receive failures.

### Resolution
Rebuilt Outlook profile and re-synced mailbox.

### Validation
- Inbox updated and new test email received.
- User confirmed sending/receiving works normally.

### Escalation Notes (If Needed)
- **Escalate to:** Messaging / O365 Admin
- **When to escalate:** Profile rebuild fails, auth loops persist, or multiple users are impacted (possible service issue).
- **Info to include:** Error messages, Outlook version, whether MFA prompts occur, affected user count, timestamps.

### Documentation / Prevention
- Documented steps to rebuild Outlook profile.
- (Optional) Add KB article: Outlook not syncing checklist
