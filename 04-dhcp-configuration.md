# DHCP Configuration

The DHCP Server role was installed on DC001 and authorised in Active Directory. A scope named `Lab LAN` was created for the `192.168.56.0/24` network.

| Scope setting | Value |
|---|---|
| Scope name | `Lab LAN` |
| Network | `192.168.56.0/24` |
| Address pool | `192.168.56.50` – `192.168.56.200` |
| Subnet mask | `255.255.255.0` |
| Router option | `192.168.56.1` |
| DNS server option | `192.168.56.10` |
| DNS domain | `lab.local` |

The router option is the value configured in the lab scope; it does not establish that the host-only network provides internet access.

## PC001 reservation

| Field | Value |
|---|---|
| Reservation name | `PC001` |
| Reserved address | `192.168.56.100` |
| MAC address | `08-00-27-F6-8F-1C` |
| Reservation type | DHCP |

An earlier reservation used `192.168.56.10`, which was already assigned statically to DC001. It was corrected to `192.168.56.100`.

## Verification

```cmd
ipconfig /release
ipconfig /renew
ipconfig /all
```

Confirm that DHCP is enabled, the IPv4 address is `192.168.56.100`, and the DNS server is `192.168.56.10`.
