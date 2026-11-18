# DNS Configuration

DNS Server was installed on DC001 as part of the domain controller setup. The lab uses the `lab.local` domain.

## Forward lookup zones

The DNS Manager console contains these forward lookup zones:

- `lab.local`
- `_msdcs.lab.local`

The `lab.local` zone contains host records for the domain controller and workstation.

| Host | Expected IPv4 address |
|---|---|
| `dc001.lab.local` | `192.168.56.10` |
| `PC001.lab.local` | `192.168.56.100` |

The PC001 record should match the address assigned by its DHCP reservation.

## Verification

From PC001:

```cmd
ping DC001.lab.local
nslookup DC001.lab.local
nslookup PC001.lab.local
```
