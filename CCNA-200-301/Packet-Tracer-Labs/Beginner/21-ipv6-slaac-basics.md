# Lab 21: IPv6 SLAAC Basics

## Objective

Use IPv6 SLAAC to let PCs generate IPv6 addresses automatically.

## Topology

- 1 router
- 1 switch
- 2 PCs

## Tasks

1. Configure an IPv6 address on the router LAN interface.
2. Enable IPv6 unicast routing.
3. Set both PCs to use automatic IPv6 configuration.
4. Verify that each PC receives an IPv6 address.
5. Test connectivity to the router IPv6 address.

## Example Commands

```text
ipv6 unicast-routing
interface g0/0
ipv6 address 2001:db8:acad:21::1/64
no shutdown
```

## Verification

```text
show ipv6 interface brief
show ipv6 interface g0/0
ping 2001:db8:acad:21::1
```

## Notes

- Save the completed Packet Tracer file as `21-ipv6-slaac-basics.pkt`.

