# Network Configuration

The lab uses an Oracle VirtualBox Host-Only network with subnet `192.168.56.0/24`. Both virtual machines are connected to this network.

| Device | Hostname | Operating system | IPv4 configuration |
|---|---|---|---|
| Domain controller | `DC001.lab.local` | Windows Server 2019 | `192.168.56.10` — static |
| Workstation | `PC001.lab.local` | Windows 10 | `192.168.56.100` — DHCP reservation |

## DC001

DC001 uses a static address so the domain controller and its network services remain reachable at a consistent address.

- IP address: `192.168.56.10`
- Subnet mask: `255.255.255.0`
- Preferred DNS: `127.0.0.1`

## PC001

PC001 obtains its address from the DHCP service on DC001.

- MAC address: `08-00-27-F6-8F-1C`
- Reserved IPv4 address: `192.168.56.100`
- DNS server: `192.168.56.10`
- DNS suffix: `lab.local`

PC001 initially had a different address configured during network setup. Its DHCP reservation was subsequently corrected to `.100` so it would not use DC001's `.10` address. The workstation lease was renewed and connectivity checked.

## Verification

```cmd
ipconfig /all
ipconfig /release
ipconfig /renew
ping 192.168.56.10
ping DC001.lab.local
```

The final configuration is a DHCP-enabled PC001 using `192.168.56.100`, with DC001 at `192.168.56.10`.
