# KB-001: Resetting a User Password in Linux

## Problem Summary
User reports being unable to log in after returning from vacation. Account appears locked or password expired.

## Affected Systems
- Operating System: Ubuntu 22.04
- Application: Local Linux user accounts
- User Group: All workstation users

## Symptoms
- “Authentication failed” or “Password expired” errors
- User unable to access system console or SSH
- Admin sees account listed as locked or expired

## Root Cause
User passwords were set to expire after a defined interval (`chage -d 0` forced expiration) or account lockout policy triggered.

## Resolution Steps
1. Log into the server as root or admin:
   ```bash
   sudo su -
2. Verify account status:
   sudo chage -l demo.user
3. Reset password:
   sudo passwd demo.user
4. Unlock account if needed:
   sudo usermod -U demo.user
5. Verify login works by switching user:
   su - demo.user
Verification / Validation
- User successfully logs in with the new password.
- System logs show successful authentication.
- Ticket marked as “Resolved” in osTicket.

Prevention / Best Practices
- Encourage users to reset passwords before expiration.
- Add password change reminders in user onboarding emails.
- Maintain a secure password policy (minimum 12 characters, complexity).
