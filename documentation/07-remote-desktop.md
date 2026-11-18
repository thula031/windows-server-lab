# Remote Desktop

## Status

Remote Desktop is a planned part of this lab and has not yet been completed and tested. It is not listed as a verified capability of the current environment.

## Planned configuration

The intended approach is to configure Remote Desktop through Group Policy rather than enabling it manually on each workstation.

The planned setting is located at:

`Computer Configuration > Policies > Administrative Templates > Windows Components > Remote Desktop Services > Remote Desktop Session Host > Connections`

Setting: `Allow users to connect remotely by using Remote Desktop Services`.

Before applying the policy, confirm that the PC001 computer account is in the OU to which the computer policy is linked. A user account being in the Staff OU does not, by itself, make a Computer Configuration policy apply to the workstation.

## Planned verification

1. Run `gpupdate /force` on PC001.
2. Use `gpresult /r` to check whether the policy applies.
3. Confirm Remote Desktop is enabled and Windows Firewall permits the connection.
4. From a separate client, connect using `mstsc` to PC001's address.
5. Record the result and add a screenshot only after a successful test.

Do not describe RDP as working until the remote connection has been tested successfully.
