# Runbook: AD Password Reset & Account Unlock

## Purpose
Restore user access when they’re locked out or forgot their password.

## When to use
- User receives “account locked” or cannot log in
- Password expired or forgotten

## Prereqs / Access
- Help Desk permissions in Active Directory
- Identity verification completed per policy

## Steps
1. Verify the user’s identity (per policy).
2. Open **Active Directory Users and Computers**.
3. Search for the user account.
4. Check account status:
- Locked out / Disabled / Password expired
5. If locked out, **unlock** the account.
6. **Reset password** to a temporary password (per policy).
7. Set **User must change password at next logon** (if required).
8. Have the user log in and confirm successful access.

## If it fails
- Confirm correct username and domain
- Check if the account is disabled
- Look for repeated lockouts (cached credentials on phone, mapped drives, old devices)

## Escalation
Escalate to Systems/AD Admin if:
- Repeated lockouts continue after reset
- Suspicious activity is suspected
