# Ticket 002 - Windows User Account Management

## Issue

Simulated a Help Desk request to create a Windows account for a new employee.

The account needed standard user permissions, a password change at first login, and restricted access to administrator functions.

## Environment

- Windows 11 Pro ARM
- UTM virtual machine
- Computer Management
- Local Users and Groups
- Command Prompt

## Troubleshooting Steps

1. Opened Computer Management and navigated to Local Users and Groups.
2. Created a local account named TestEmployee.
3. Assigned the account to the standard Users group.
4. Enabled the option requiring a password change at the next login.
5. Signed in using the new account and completed the password change.
6. Opened Command Prompt and ran `whoami` to verify the account.
7. Ran `net session` to check administrative access.
8. Ran `whoami /groups` to verify group membership.

## Results

| Test | Result |
|---|---|
| Account creation | Successful |
| First-login password change | Successful |
| `whoami` | TestEmployee |
| `net session` | System error 5 - Access denied |
| `whoami /groups` | Administrators group not present |

## Findings

The TestEmployee account was successfully created with standard user permissions.

The account was able to sign in and change its password but did not have administrator privileges.

The access-denied result from `net session`, together with the group membership check, supported that the account was operating with restricted permissions.

## Resolution

Verified that the account was created correctly and had the intended permissions.

No additional changes were required.

Status: Closed - Account Provisioning Verified

## Skills Used

- Windows user account management
- Local Users and Groups
- User provisioning
- Access control
- Principle of least privilege
- Command Prompt
- Technical documentation

## Notes

This was a simulated Help Desk scenario completed in my Windows 11 home lab. No actual employee account or production system was involved.