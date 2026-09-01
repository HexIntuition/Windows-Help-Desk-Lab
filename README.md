# Windows Help Desk Lab

Hands-on Windows support lab built around simulated end-user incidents. Each ticket documents the reported symptom, troubleshooting process, root cause, resolution, and verification.

> **Lab disclosure:** These are simulated support scenarios created for hands-on practice and portfolio documentation. They are not real customer incidents.

## Ticket Index

| Ticket | Scenario | Focus | Status |
|---|---|---|---|
| [Ticket 01 — DNS Resolution Failure](./01-dns-resolution/) | Workstation has IP connectivity but cannot resolve hostnames | DNS, TCP/IP, Command Prompt | ✅ Resolved |
| [Ticket 02 — Print Spooler Service Failure](./02-print-spooler/) | Windows printing fails because the Print Spooler service is stopped | Windows Services, Printing, CLI | ✅ Resolved |
| [Ticket 03 — Outlook Offline Mode](./03-outlook-offline-mode/) | Outlook cannot send or receive while Work Offline is enabled | Outlook, Exchange, TCP/IP, DNS | ✅ Resolved |
| [Ticket 04 — Windows NTFS Permissions / Access Denied](./04-windows-ntfs-permissions/) | User cannot access a required folder because the account lacks NTFS permissions | NTFS, ACLs, `icacls`, `takeown` | ✅ Resolved |

## Troubleshooting Workflow

1. Confirm the reported symptom.
2. Establish the scope of the issue.
3. Test the simplest likely causes first.
4. Isolate the failing component or service.
5. Apply the least disruptive fix.
6. Verify service restoration.
7. Document findings and resolution.

## Skills Demonstrated

- Windows 11 troubleshooting
- End-user support methodology
- TCP/IP and DNS diagnostics
- Windows Services
- Printer troubleshooting
- Microsoft Outlook troubleshooting
- Microsoft Exchange client connectivity
- Windows NTFS permissions and ACL troubleshooting
- File/folder ownership and access recovery
- Command Prompt diagnostics
- Root-cause isolation
- Resolution verification
- Technical documentation

## Privacy

Screenshots used in this public portfolio are reviewed and sanitized to remove unrelated usernames, device identifiers, and other unnecessary personal information.
