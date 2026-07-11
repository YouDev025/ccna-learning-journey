# Subnetting CheatSheet

## Core Formula
```text
Block size = 256 - interesting octet mask value
Usable hosts = 2^host_bits - 2
```

## Common Prefixes
| Prefix | Mask | Block size | Usable hosts |
|---|---|---:|---:|
| /24 | 255.255.255.0 | 1 in 3rd octet | 254 |
| /25 | 255.255.255.128 | 128 | 126 |
| /26 | 255.255.255.192 | 64 | 62 |
| /27 | 255.255.255.224 | 32 | 30 |
| /28 | 255.255.255.240 | 16 | 14 |
| /29 | 255.255.255.248 | 8 | 6 |
| /30 | 255.255.255.252 | 4 | 2 |
| /31 | 255.255.255.254 | 2 | Point-to-point special use |
| /32 | 255.255.255.255 | 1 | Host route |

## Fast Steps
1. Find the interesting octet.
2. Calculate block size.
3. Count subnet ranges by block size.
4. Locate the IP address inside a range.
5. Identify network, first host, last host, and broadcast.

## Example: 192.168.1.77/26
- Mask: `255.255.255.192`
- Block size: `64`
- Subnets: `0`, `64`, `128`, `192`
- Network: `192.168.1.64`
- First host: `192.168.1.65`
- Last host: `192.168.1.126`
- Broadcast: `192.168.1.127`

## Private IPv4 Ranges
| Range | Prefix |
|---|---|
| 10.0.0.0 - 10.255.255.255 | 10.0.0.0/8 |
| 172.16.0.0 - 172.31.255.255 | 172.16.0.0/12 |
| 192.168.0.0 - 192.168.255.255 | 192.168.0.0/16 |

## Wildcard Quick Reference
| Mask | Wildcard |
|---|---|
| 255.255.255.0 | 0.0.0.255 |
| 255.255.255.128 | 0.0.0.127 |
| 255.255.255.192 | 0.0.0.63 |
| 255.255.255.224 | 0.0.0.31 |
| 255.255.255.240 | 0.0.0.15 |
| 255.255.255.248 | 0.0.0.7 |
| 255.255.255.252 | 0.0.0.3 |

## Exam Traps
- Network and broadcast addresses are not normal host addresses.
- `172.32.0.0` is not RFC 1918 private space.
- A `/30` has 2 usable addresses.
- A `/24` does not always mean class C; classful thinking is mostly legacy.
