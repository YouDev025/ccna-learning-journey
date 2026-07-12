# Lab 03: ACL and NAT Troubleshooting

## Objective

Troubleshoot a network where internal users cannot consistently reach external resources.

## Topics

- NAT inside and outside interfaces
- NAT overload
- Standard and extended ACLs
- Default routes
- Interface status

## Symptoms

- Some inside PCs cannot reach the outside server.
- NAT translations are missing for some traffic.
- Pings to the ISP router may succeed while pings to the server fail.

## Tasks

1. Build or load the broken topology.
2. Verify IP addressing and routing.
3. Inspect NAT configuration.
4. Inspect ACL matches and placement.
5. Correct the configuration.
6. Prove the fix with verification commands.

## Verification

```text
show ip route
show access-lists
show ip nat translations
show ip nat statistics
ping
traceroute
```

## Notes

- Save the completed Packet Tracer file as `03-acl-and-nat-troubleshooting.pkt`.

