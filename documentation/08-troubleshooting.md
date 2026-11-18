# Troubleshooting Notes

## Network path could not be opened

**Issue:** Windows could not find the StaffShare network path.

**Cause:** The UNC path had been entered in File Explorer's search box rather than its address bar.

**Resolution:** Enter the network path in the address bar or Run dialog: `\\192.168.56.10\StaffShare`.

## Staff user could not open Settings

**Issue:** Windows displayed a message that the operation had been cancelled because of restrictions.

**Cause:** The Block Control Panel - Staff policy was applied to the Staff user account.

**Resolution:** This was the intended result of the policy test. Use an account outside the targeted OU for administration rather than weakening the policy for the test user.

## Group Policy update could not contact a domain controller

**Issue:** `gpupdate /force` reported a network connectivity problem when contacting a domain controller.

**Cause:** DC001 was still starting or network connectivity was not yet available.

**Resolution:** Wait for DC001 to finish starting, verify connectivity with `ping 192.168.56.10`, and retry the policy update.

## DHCP reservation used the domain controller's address

**Issue:** An earlier PC001 reservation was set to `192.168.56.10`, already assigned statically to DC001.

**Resolution:** The reservation was corrected to `192.168.56.100` and associated with PC001's MAC address `08-00-27-F6-8F-1C`. PC001's DHCP lease was renewed and connectivity was checked.
