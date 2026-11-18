# Active Directory Domain Services

Active Directory Domain Services was installed on DC001 through Server Manager. The server was promoted to a domain controller and configured as a new forest.

| Setting | Value |
|---|---|
| Domain | `lab.local` |
| NetBIOS name | `LAB` |
| Domain controller | `DC001` |

A Directory Services Restore Mode (DSRM) password was set during promotion.

## Organisational structure

An organisational unit named `Staff` was created under `lab.local`. The domain user `lwandle` was created for workstation sign-in and placed in the Staff OU.

| Object | Name |
|---|---|
| Domain | `lab.local` |
| OU | `Staff` |
| User | `lwandle` |
| User principal name | `lwandle@lab.local` |

The lab account's password setting was configured for this practice environment. A password that never expires should not be used in a production environment.

## Verification

```powershell
Get-ADDomain
Get-ADUser -Filter *
```
