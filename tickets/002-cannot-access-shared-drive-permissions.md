## Ticket
**Ticket #:** 002
**Category:** Access / File Shares
**Priority:** P2
**Reported by:** User
**Channel:** Chat

### Summary
User cannot access a shared drive and receives “Access Denied” when opening the network folder.

### Impact / Urgency
- **Impact:** User cannot access team files needed for daily tasks.
- **Urgency:** Medium–High
- **Priority Rationale:** Work blocked for core files → P2.

### Environment
- Device / OS: Windows 10/11
- Location: On-site or VPN
- Network: LAN/VPN

### Clarifying Questions Asked
- What is the exact path? (example: \\FILESERVER\DeptShare)
- Is this a new issue or first-time access request?
- Are coworkers able to access it?
- Are you on VPN if remote?

### Troubleshooting & Actions Taken (Timeline)
1. Confirmed the UNC path and captured the exact error message.
2. Verified network connectivity to the file server (ping / name resolves).
3. Checked whether the user can access other shares (to isolate permissions vs connectivity).
4. Verified user group membership in Active Directory for the share (role-based group).
5. Reviewed share + NTFS permissions alignment with intended access.
6. If access was approved, updated group membership and had user sign out/in (or refresh policy) to obtain updated token.

### Root Cause
User was not in the correct security group for the share (or permissions changed).

### Resolution
Added user to appropriate access group (per approval) and confirmed permissions.

### Validation
- User successfully opened the share and accessed required folders.

### Escalation Notes (If Needed)
- **Escalate to:** Systems/File Server Admin
- **When to escalate:** Permissions appear correct but access still fails (inheritance/ACL issues, DFS issues, server-side problems).
- **Info to include:** Share path, username, groups checked, error text, VPN/on-site status, server name.

### Documentation / Prevention
- Recommend group-based access (avoid direct user permissions).
