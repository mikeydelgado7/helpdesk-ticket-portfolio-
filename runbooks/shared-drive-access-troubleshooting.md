# Runbook: Shared Drive Access (Access Denied)

## Purpose
Resolve “Access Denied” errors to file shares and mapped drives.

## When to use
- User cannot open \\server\share
- Mapped drive is missing or disconnected
- User receives “Access Denied”

## Steps
1. Confirm the exact path (UNC) and capture the error text.
2. Confirm connectivity to the server:
- Verify user is on-site or connected to VPN (if remote)
3. Check scope:
- Only this user or multiple users affected?
4. Verify access is group-based:
- Check user’s AD group membership for the share
5. Review permissions:
- Share permissions + NTFS permissions alignment
6. If membership was updated (approved), have user:
- Sign out/sign in (or reboot) to refresh permissions token

## If it fails
- Check for broken inheritance/ACL issues
- Confirm user is not using cached credentials
- Validate DFS path (if applicable)

## Escalation
Escalate to File Server Admin with:
- Share path, username, groups checked, error message, VPN/on-site status, timestamps
