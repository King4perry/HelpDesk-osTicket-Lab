# Help Desk Ticket Report Template

## Ticket Details
- Ticket ID: 444463
- Date/Time Opened: 09/25/25
- Department: Service Desk L1
- Priority / SLA: High/P1-Urgent
- Help Topic: Password Reset/Account Unlock
- Status: Open

## User Description
I have failed multiple times trying to log in to my account now I am locked out of my account.

## Initial Assessment
Steps Taken:
1. Verified user identity and gathered environment details.
2. Checked similar tickets or alerts.
3. Scoped impact (single user vs multiple users).

Findings:
Summarize early observations.

## Troubleshooting Actions
**Step 1 – Verified Account Exists**
``bash
sudo mysql -u root -p
sql
Copy code
USE osticket;
SELECT id, username, email FROM ost_staff;
php -r "echo password_hash('NewPassword123!', PASSWORD_BCRYPT);"
$2y$12$D2YQjYs4BoSLJx96vj6BX.8DK1ZfnZ/s3ukjukl1/VYeiaiigHMhq
UPDATE ost_staff
SET passwd = '$2y$12$D2YQjYs4BoSLJx96vj6BX.8DK1ZfnZ/s3ukjukl1/VYeiaiigHMhq'
WHERE username = 'newadmin';
EXIT;
sudo systemctl restart apache2
sudo systemctl restart mysql

## Root Cause
Describe the underlying issue.

## Resolution
Password was successfully reset by:
- Verifying the account in MySQL
- Generating a new bcrypt hash
- Updating the hash in the ost_staff table
- Restarting Apache/MySQL to clear sessions

## Verification / Evidence
- Screenshots
- Logs
- User confirmation

## Knowledge Base Reference
- KB Article: Password
- Canned Response: Password Reset Template

## Lessons Learned / Prevention
A preventive measure would be to implement a MFA method as an alternative for users to go into account.

## Final Status
- Resolved By: Germaine Perry
- Resolution Type: Password Reset
- Time to Resolution: 2 hours
EOF
