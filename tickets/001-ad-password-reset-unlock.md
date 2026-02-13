## Ticket
**Ticket #:** 001
**Category:** Access
**Priority:** P2
**Reported by:** User (Employee)
**Channel:** Phone

### Summary
User is locked out of their account after multiple failed login attempts and needs a password reset.

### Impact / Urgency
- **Impact:** User cannot access workstation/email to start work.
- **Urgency:** High (active work shift)
- **Priority Rationale:** Single user blocked from working → P2.

### Environment
- Device / OS: Windows 10/11 workstation
- Location: On-site
- Network: Corporate LAN

### Clarifying Questions Asked
- Are you receiving “account locked” or “incorrect password”?
- Did you recently change your password on another device?
- Are you able to sign into any other system?

### Troubleshooting & Actions Taken (Timeline)
1. Verified user identity per standard process (name, department, manager confirmation or security questions).
2. Checked Active Directory for account status (locked out / password expired).
3. Unlocked the account.
4. Reset password and checked “User must change password at next logon” (policy dependent).
5. Confirmed user can log in and update password successfully.

### Root Cause
User entered an outdated password multiple times, triggering account lockout policy.

### Resolution
Unlocked account and reset password per policy.

### Validation
- User successfully logged in on the workstation.
- User confirmed access to email and required apps.

### Escalation Notes (If Needed)
- **Escalate to:** Systems/AD Admin
- **When to escalate:** If repeated lockouts occur in a short period (possible cached credentials, mapped drives, mobile device, or suspicious activity).
- **Info to include:** Username, time of lockouts, workstation name, recent password changes, any devices using old credentials.

### Documentation / Prevention
- Advised user to update password on mobile/other devices to prevent repeat lockouts.
