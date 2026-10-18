# Help Desk Ticket #002 — Windows Local User Account Provisioning

**Category:** User Account Management / Access Control  
**Environment:** Windows 11 Pro ARM (UTM Virtual Machine)  
**Account:** TestEmployee  
**Status:** Provisioning successful; final group-token verification pending

## Issue / Service Request
Provision a new employee account with standard Windows permissions and require a password change upon first login.

## Troubleshooting and Actions Performed
1. Accessed Computer Management → Local Users and Groups → Users.
2. Created a local user account named `TestEmployee`.
3. Assigned a temporary password and enabled **User must change password at next logon**.
4. Verified that the account belonged to the local Users group and was not listed in Administrators.
5. Successfully signed in using the employee account.
6. Confirmed that Windows required the temporary password to be changed.
7. Attempted to launch an elevated Command Prompt and investigated the unexpected absence of a UAC prompt.
8. Executed `whoami` to confirm the active account was `TestEmployee`.
9. Executed `net session`, which returned **System error 5 — Access is denied**.

## Findings
- The new employee account was created successfully.
- The first-login password change requirement functioned correctly.
- Local group membership was consistent with standard-user access.
- The attempted privileged operation was denied, indicating the Command Prompt session did not have the required administrative privileges.

## Resolution
Account provisioning and initial permission checks were successful. Final verification with `whoami /groups` is pending.

## Skills Demonstrated
Windows 11 Administration, Local User Management, Group Membership Verification, Least Privilege, User Account Control, Command-Line Diagnostics, Access Control Troubleshooting, IT Ticket Documentation.