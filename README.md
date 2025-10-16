# Help Desk Ticketing System (osTicket Lab)

This project simulates a real-world IT Help Desk environment using osTicket deployed on AWS EC2 (Ubuntu).  
It demonstrates ticket creation, troubleshooting, escalation, and documentation processes aligned with ITIL best practices.

## Tech Stack
- AWS EC2 (Ubuntu Server 22.04)
- Apache2, MySQL (MariaDB), PHP 8.2
- osTicket v1.18.x
- Linux CLI Tools: ping, netplan, ufw, cups, tar, mysqldump

## Project Overview
- Built and configured a Help Desk ticketing system using osTicket.
- Created and resolved multiple simulated tickets:
  - Password Reset / Account Unlock
  - Wi-Fi / DNS Connectivity
  - Printer Offline
  - VPN Failure
  - Email Client Crash
- Developed a Knowledge Base with standardized solutions.
- Configured SLAs, Departments, and Canned Responses.
- Performed security hardening and backups.

## Repository Structure
---

## Visual Walkthrough

### 1. Server Setup and Installation
Below is the successful Apache and PHP setup on the Ubuntu EC2 instance.

![Apache Installed](screenshots/Step1_Apache_Install.png)

osTicket installation page loaded correctly through the browser.

![osTicket Installer](screenshots/Step2_osTicket_Installer.png)

---

### 2. Help Desk Configuration
Departments, SLAs, and help topics were configured to simulate an enterprise IT environment.

![osTicket Admin Panel](screenshots/Step3_Admin_Panel.png)

---

### 3. Troubleshooting a Password Reset Issue
Ticket created for a user locked out after a password expiration.

**Before Fix:**
![Ticket Before Fix](screenshots/Ticket001_Before_Fix.png)

**After Fix:**
![Ticket After Fix](screenshots/Ticket001_After_Fix.png)

---

### 4. Knowledge Base and Reporting
Example of a KB article created to document standard operating procedures.

![KB Article](screenshots/KB001_Password_Reset.png)

Dashboard reports show SLA compliance and closed tickets.

![Dashboard Reports](screenshots/Dashboard_Reports.png)

---

## Summary
This lab demonstrates full lifecycle IT support skills:
- Ticket creation, troubleshooting, and resolution
- Documentation through Knowledge Base articles
- System administration in Linux and AWS environments
- Backup and security hardening of web applications

