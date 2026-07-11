# IPv6 CheatSheet

## Key Facts
- IPv6 is 128 bits.
- Written in hexadecimal.
- Uses 8 groups of 16 bits.
- Common LAN prefix length is `/64`.
- IPv6 does not use broadcast.
- Neighbor Discovery replaces many ARP functions.

## Address Shortening Rules
- Remove leading zeros in a group.
- Replace one continuous all-zero section with `::`.
- Use `::` only once per address.

## Example
```text
2001:0db8:0000:0001:0000:0000:0000:0010
2001:db8:0:1:0:0:0:10
2001:db8:0:1::10
```

## Address Types
| Type | Prefix/example | Purpose |
|---|---|---|
| Global unicast | `2000::/3` | Public routable IPv6 |
| Link-local | `fe80::/10` | Local link communication |
| Unique local | `fc00::/7` | Private-like internal addressing |
| Multicast | `ff00::/8` | One-to-many communication |
| Loopback | `::1/128` | Local host |
| Unspecified | `::/128` | No address |

## Common Multicast
| Address | Meaning |
|---|---|
| `ff02::1` | All nodes on local link |
| `ff02::2` | All routers on local link |
| `ff02::5` | OSPFv3 routers |
| `ff02::6` | OSPFv3 DR/BDR |

## Useful Commands
```text
show ipv6 interface brief
show ipv6 route
show ipv6 neighbors
ping ipv6 <address>
traceroute ipv6 <address>
ipv6 unicast-routing
```

## Static Route Examples
```text
ipv6 route 2001:db8:20::/64 2001:db8:12::2
ipv6 route ::/0 2001:db8:12::2
```

## Exam Traps
- `::` can appear only once in an address.
- Link-local addresses are not routed beyond the local link.
- IPv6 has no broadcast.
- Multiple IPv6 addresses can exist on one interface.
