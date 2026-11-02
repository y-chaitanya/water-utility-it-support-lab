# Help Desk Ticket Log (Simulated)

Simulated tickets for practice. These are not real users, devices or systems. The steps show how I would work each ticket at first-level support and when I would escalate.

## Summary

| Ticket | Opened | Contact | Category | Priority | Issue | Result | First-contact resolved |
|---|---|---|---|---|---|---|---|
| T-001 | 11/01/2026 09:05 | Phone | Access | P2 | User locked out of account | Resolved | Yes |
| T-002 | 11/01/2026 09:40 | Portal | Software | P3 | Outlook not syncing email | Resolved | Yes |
| T-003 | 11/01/2026 10:15 | Phone | Printer | P3 | Printer shows offline | Resolved | Yes |
| T-004 | 11/01/2026 10:50 | Phone | Network | P2 | One user has no internet | Resolved | Yes |
| T-005 | 11/01/2026 11:20 | Phone | Network | P1 | Whole team cannot open shared drive | Escalated to Tier 2 network | No |
| T-006 | 11/01/2026 13:00 | Portal | Hardware | P3 | New hire laptop setup | Resolved | Yes |
| T-007 | 11/01/2026 14:10 | Email | Security | P2 | User reports a phishing email | Escalated to security team | No |
| T-008 | 11/01/2026 15:30 | Portal | Software | P4 | Excel closes when opening a large file | Resolved | Yes |

**First-contact resolution:** 6 of 8 (75%). **Escalated:** T-005 (team-wide outage, beyond first-level access) and T-007 (security incident).

**Priority scale:** P1 = many users or critical work stopped. P2 = one user cannot work. P3 = one user, workaround exists. P4 = minor, no deadline.

## Ticket details

### T-001 Account lockout (P2)
- **Steps:** Verified the caller's identity using the approved questions. Confirmed the account was locked after too many failed sign-ins. Unlocked the account and had the user sign in and set a new password.
- **Result:** Resolved on the call. Reminded the user how to reset a password through self-service next time.

### T-002 Outlook not syncing (P3)
- **Steps:** Confirmed the user had internet access and webmail worked. Restarted Outlook, then opened it in safe mode to rule out add-ins. Repaired the mail profile.
- **Result:** Resolved. Mail synced after the profile repair.

### T-003 Printer offline (P3)
- **Steps:** Checked power, cable and the printer's own display. Cleared stuck jobs from the print queue. Restarted the print spooler service and printed a test page.
- **Result:** Resolved. Test page printed.

### T-004 No internet for one user (P2)
- **Steps:** Ran `ping -c 4` to a known site and to the default gateway. Found the gateway with `route -n get default` and checked DNS with `scutil --dns`. The laptop was on the guest Wi-Fi network, which blocks internal resources. Moved it to the staff network and tested again.
- **Result:** Resolved. Commands practiced in [Exercise 01](../02_network_troubleshooting/01_basic_connectivity_test.md) and [Exercise 04](../02_network_troubleshooting/04_network_configuration_inspection.md).

### T-005 Shared drive down for a whole team (P1)
- **Steps:** Asked how many users were affected and since when; confirmed it was the whole team, so this was not a single-device problem. Notified my supervisor right away.
- **Result:** Escalated to the Tier 2 network team with the scope, start time and what the users saw. Updated the users when Tier 2 confirmed the fix, then closed after users confirmed access.

### T-006 New hire laptop setup (P3)
- **Steps:** Installed the standard software, including Microsoft 365. Added the laptop's model, serial number and assigned user to the hardware inventory. Confirmed the user's account request had been approved before first sign-in.
- **Result:** Resolved. User signed in and opened email.

### T-007 Phishing email reported (P2)
- **Steps:** Told the user not to click links or open attachments. Asked whether they had already clicked or entered a password (they had not). Had them report the message with the report button.
- **Result:** Escalated to the security team with the sender and subject. Thanked the user for reporting it.

### T-008 Excel closes on a large file (P4)
- **Steps:** Opened Excel in safe mode; the file opened, which pointed to an add-in. Disabled add-ins one at a time and found the one causing the crash. Checked that Office was up to date.
- **Result:** Resolved. Excel opened the file with that add-in disabled.

## What this exercise practiced
- Classifying each ticket by category and priority before acting.
- Resolving at first contact where possible and escalating with a clear scope when not.
- Writing steps a teammate could follow, and closing tickets only after the user confirmed.