IT Support Ticket: Expired Password (INC0012855)

A documented walkthrough of how I resolved a High priority password incident in ServiceDesk Simulator, a practice help desk environment.

Overview

A lead developer returned from a 3-week vacation and could not log in. Her password had expired and the login screen would not let her change it. She had a sprint deadline on Friday, so I handled the ticket as a priority.

This repository records my full process, from opening the ticket to closing it, with a screenshot for each step.

Ticket Summary
Field	Detail
Ticket	INC0012855
Priority	High
Reported by	Maria Garcia (Engineering, Floor 3, x6102)
Assignee	Thabang Norman Lesotho
Issue	Cannot log in, password expired after 3-week absence
Business impact	Sprint deadline Friday. User is lead developer on the payment processing module.
Platform	ServiceDesk Simulator
Skills Demonstrated
Incident triage and prioritisation
User identity verification before account changes
Account status checks (enabled, locked, MFA, password expiry)
Password reset and secure credential handling
Clear ticket documentation and closure
Tools Used
ServiceDesk Simulator
Ticket Queue
Directory (Authentication tab)
Identity Verification
Company Chat
Workflow

Resolution Notes

I verified that the user's password had expired due to extended inactivity during a 3-week vacation. The account was enabled, not locked, and MFA was enrolled. I verified the user's identity by sending a verification code to the registered phone number, which the user confirmed via Company Chat. I reset the password from the Directory Authentication tab and issued a temporary password, which I sent to the user via Company Chat. The Password expired status changed to No after the reset. The user is to change the temporary password at next logon. Ticket resolved.

Classification
Field	Value
Incident Type	Authentication Issue
Category	Password Management
Subcategory	Expired Password
Root Cause

The password expired while the user was away on vacation and had not logged in for several weeks, preventing authentication at the Windows login screen.

Key Takeaways
Always verify identity before resetting credentials.
Check account state first (locked, disabled, expired, MFA) so the fix targets the real cause.
Share temporary passwords through a secure channel and never record them in ticket notes.
Real-World Equivalent

In a production Active Directory environment, this reset would be done in Active Directory Users and Computers (ADUC) with the option to require a password change at next logon.

Security Note

Verification codes and temporary passwords have been blacked out in all screenshots.
