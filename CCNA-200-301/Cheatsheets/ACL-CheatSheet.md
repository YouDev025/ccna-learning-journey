# ACL CheatSheet

## Core Rules
- ACLs are processed top to bottom.
- First match wins.
- Every ACL has an implicit `deny any` at the end.
- Place specific rules before broad rules.
- Standard ACLs filter mainly by source IP.
- Extended ACLs filter by source, destination, protocol, and port.

## Standard ACL Syntax
```text
access-list <1-99> permit|deny <source> <wildcard>
access-list <1-99> permit|deny host <source-ip>
access-list <1-99> permit|deny any
```

## Extended ACL Syntax
```text
access-list <100-199> permit|deny <protocol> <source> <wildcard> <destination> <wildcard> [operator port]
access-list <100-199> permit|deny tcp any host 192.168.1.10 eq 80
```

## Named ACL Syntax
```text
ip access-list standard BLOCK_HOST
 deny host 192.168.10.50
 permit any

ip access-list extended GUEST_FILTER
 deny tcp 192.168.30.0 0.0.0.255 host 192.168.10.10 eq 443
 permit ip any any
```

## Apply ACL to Interface
```text
interface gigabitEthernet0/0
 ip access-group 100 in
```

## Common Ports
| Service | Protocol/Port |
|---|---|
| SSH | TCP 22 |
| Telnet | TCP 23 |
| DNS | UDP/TCP 53 |
| DHCP server | UDP 67 |
| DHCP client | UDP 68 |
| HTTP | TCP 80 |
| HTTPS | TCP 443 |
| SNMP | UDP 161 |
| NTP | UDP 123 |

## Wildcard Masks
| Subnet mask | Wildcard |
|---|---|
| 255.255.255.255 | 0.0.0.0 |
| 255.255.255.0 | 0.0.0.255 |
| 255.255.255.128 | 0.0.0.127 |
| 255.255.255.192 | 0.0.0.63 |
| 255.255.255.224 | 0.0.0.31 |
| 255.255.255.240 | 0.0.0.15 |

## Placement
| ACL type | Best placement |
|---|---|
| Standard | Close to destination |
| Extended | Close to source |

## Verification
```text
show access-lists
show ip interface
show running-config | section access-list
show running-config interface <interface>
```

## Exam Traps
- Forgetting `permit ip any any` after deny statements.
- Applying ACL in the wrong direction.
- Using subnet mask instead of wildcard mask.
- Blocking return traffic.
- Putting a broad permit before a deny.
