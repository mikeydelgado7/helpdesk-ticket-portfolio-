# Runbook: Outlook Not Syncing (Microsoft 365)

## Purpose
Fix Outlook desktop when emails are not updating/syncing.

## When to use
- Outlook shows old emails
- “Disconnected” / “Trying to connect” status
- Send/Receive not working

## Steps
1. Confirm Outlook Web (webmail) works (isolates client vs account/service issue).
2. In Outlook:
- Ensure **Work Offline** is OFF
- Check connection status at the bottom
3. Restart Outlook and try **Send/Receive**.
4. Confirm the user can sign in and complete any MFA prompts.
5. Rebuild the Outlook profile:
- Control Panel → **Mail** → **Show Profiles** → **Add**
- Set new profile as default and re-add mailbox
6. Allow initial sync to complete and verify new emails arrive.

## If it fails
- Repair Office (Quick Repair)
- Check Windows Credential Manager for old credentials
- Confirm time/date is correct (can break auth)

## Escalation
Escalate to Messaging/O365 Admin if:
- Multiple users impacted
- Auth loop persists
- License/mailbox issue suspected
Include: errors, Outlook version, timestamps, affected users.
