# HD-002: Accounting Network Drive Missing

## Incident Summary

Penny Paws reported that the **Accounting (A:)** network drive was no longer visible in File Explorer, preventing access to departmental files stored on the shared network drive.

## Environment

- **Domain:** RockyPetSupply.local
- **Domain Controller:** RPS-DC01
- **Workstation:** RPS-WS01
- **User:** Penny Paws
- **Network Share:** `\\RPS-DC01\Accounting`

## Investigation

To determine the cause of the issue, I:

- Verified connectivity to the domain controller.
- Confirmed the Accounting share was available on the server.
- Reviewed existing mapped network drives.
- Examined the workstation's network drive configuration.

## Root Cause

The Accounting network drive mapping had been removed from the workstation, preventing the shared folder from appearing in File Explorer.

## Resolution

- Remapped drive **A:** to `\\RPS-DC01\Accounting`.
- Enabled **Reconnect at sign-in** to persist the mapping after future logins.
- Verified successful access to the shared folder.

## Verification

The Accounting drive reappeared in File Explorer, and Penny successfully opened **Quarterly_Budget.txt**, confirming the issue was resolved.

## Supporting Screenshots

Accounting drive available to the user
<img width="1369" height="1149" alt="Mapped Drive (dog)" src="https://github.com/user-attachments/assets/aa037ca5-f494-40ca-b6f0-684b7655af38" />
Accounting drive missing from File Explorer
<img width="1376" height="1143" alt="Missing Drive (dog)" src="https://github.com/user-attachments/assets/e31cee60-d111-46db-a1d6-175ec0b4fc78" />
Map Network Drive wizard used to restore access
<img width="1377" height="1142" alt="Re-mapping Drive (dog)" src="https://github.com/user-attachments/assets/d7a0785c-40fa-44df-b6c3-0eaa970326a9" />
Accounting drive restored and Quarterly_Budget.txt opened successfully
<img width="1374" height="1145" alt="Resolution (dog)" src="https://github.com/user-attachments/assets/72eb3a4c-e5e5-402d-984a-41bacc3e92cf" />
