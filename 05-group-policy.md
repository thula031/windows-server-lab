# Group Policy

## Block Control Panel for Staff

A Group Policy Object named `Block Control Panel - Staff` was created and linked to the `Staff` OU.

The setting is located at:

`User Configuration > Policies > Administrative Templates > Control Panel`

The enabled setting was `Prohibit access to Control Panel and PC settings`.

## Testing

The policy was tested by signing in to PC001 as the `lwandle` domain user and attempting to open Settings. Windows displayed a restriction message.

The test user was in the Staff OU targeted by the policy. This demonstrated the effect of linking a user policy to a specific OU.

## Troubleshooting

During testing, `gpupdate /force` reported that the computer could not contact a domain controller. DC001 was still starting or network connectivity was unavailable. Connectivity was checked before retrying the policy update.

```cmd
ping 192.168.56.10
gpupdate /force
gpresult /r
```

## RDP policy note

An `Enable RDP - Staff` GPO appears in the Group Policy Management screenshot. Remote Desktop has not yet been fully verified. A Computer Configuration policy must apply to the OU containing the workstation computer account. Confirm PC001's OU location and policy application before treating this as completed.
