# HD-003: DNS Troubleshooting

## Incident Summary

Penny Paws reported that her domain-joined workstation was unable to access network resources or resolve **RockyPetSupply.local**. Initial troubleshooting indicated a DNS configuration issue affecting Active Directory name resolution.

## Environment

- **Domain:** `RockyPetSupply.local`
- **Domain Controller:** `RPS-DC01`
- **DNS Server:** `192.168.10.10`
- **Workstation:** `RPS-WS01`
- **User:** Penny Paws

## Investigation

To identify the cause of the issue, I:

- Verified network connectivity between the workstation and domain controller.
- Tested DNS resolution using `nslookup`.
- Reviewed the workstation's DNS configuration.
- Compared the configured DNS server with the domain controller's settings.

## Root Cause

The workstation was configured to use an incorrect DNS server, preventing it from resolving Active Directory domain resources.

## Resolution

- Updated the **Preferred DNS Server** to `192.168.10.10`.
- Flushed the DNS resolver cache using `ipconfig /flushdns`.
- Retested domain name resolution with `nslookup`.

## Verification

Penny successfully resolved **RockyPetSupply.local**, and access to domain resources was restored, confirming the issue had been resolved.

## Supporting Screenshots

DNS configuration
<img width="1022" height="851" alt="Workstation Joined to Domain" src="https://github.com/user-attachments/assets/df0ecf48-9aae-4d44-979e-acf0a1dcf2cc" />
Failed name resolution
<img width="1022" height="848" alt="DNS wrong" src="https://github.com/user-attachments/assets/18b7cd18-2c39-4963-b791-4e664dd474b6" />
DNS correction
<img width="1402" height="1122" alt="Correct DNS (Rocky)" src="https://github.com/user-attachments/assets/6e46bdab-9db8-47bc-9583-e53bae4a93cf" />
Successful nslookup
<img width="1020" height="849" alt="Resolution" src="https://github.com/user-attachments/assets/4bc8d727-ad40-4bc1-9919-d3438f8157dc" />
