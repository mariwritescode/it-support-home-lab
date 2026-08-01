# HD-001: User Unable to Access Accounting Share

## Incident Summary

Penny Paws reported receiving an **"Access Denied"** error when attempting to open the Accounting department shared folder from her domain-joined workstation.

## Environment

- **Domain:** RockyPetSupply.local
- **Domain Controller:** RPS-DC01
- **Workstation:** RPS-WS01
- **User:** Penny Paws
- **Security Group:** Accounting_Users

## Investigation

To isolate the issue, I:

- Verified the user account was active.
- Confirmed membership in the **Accounting_Users** security group.
- Reviewed the Accounting share permissions.
- Inspected NTFS permissions on the shared folder.

## Root Cause

The **Accounting_Users** security group had been removed from the folder's NTFS permissions, preventing authorized users from accessing the shared resource.

## Resolution

- Restored the required NTFS permissions.
- Verified permission inheritance.
- Tested access from the user's workstation.

## Verification

Penny successfully accessed the Accounting share and opened the **Quarterly_Budget.txt** file, confirming the issue was resolved.

## Supporting Screenshots

User group membership
<img width="1061" height="847" alt="Penny Paws - Accounting Group" src="https://github.com/user-attachments/assets/31c2bd6c-6e90-45ee-a4f0-ba32fa84cf18" />
Access denied message
<img width="1375" height="1144" alt="Penny Paws - Unauthorized Access to Accounting Files (dog)" src="https://github.com/user-attachments/assets/20e24be6-f27e-4aa2-ace0-aed9d2478de0" />
Incorrect permissions
<img width="1057" height="849" alt="Accounting Group - Security Properties Incorrect" src="https://github.com/user-attachments/assets/e97a8603-ed53-41e1-9a74-106480a8e583" />
Corrected permissions
<img width="1054" height="849" alt="Accounting Group - Security Properties Correct" src="https://github.com/user-attachments/assets/6b0b2d2d-6651-4b26-b247-d9fc15c3246d" />
Successful file access
<img width="1376" height="1143" alt="Penny Paws - Access to File Shares" src="https://github.com/user-attachments/assets/3bfd251c-d07f-4cec-ba3e-023db323c6bc" />
