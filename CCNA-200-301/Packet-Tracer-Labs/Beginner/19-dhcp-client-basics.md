# Lab 19: DHCP Client Basics

## Objective

Configure PCs as DHCP clients and verify automatic address assignment.

## Topology

- 1 router or server acting as DHCP server
- 1 switch
- 3 PCs

## Tasks

1. Build a simple LAN.
2. Configure a DHCP service on a router or server.
3. Set each PC to obtain an IP address automatically.
4. Verify each PC receives an IP address, subnet mask, gateway, and DNS server.
5. Test connectivity between PCs.

## Verification

On each PC:

```text
ipconfig
ping
```

On the router, if used as DHCP server:

```text
show ip dhcp binding
```

## Notes

- Save the completed Packet Tracer file as `19-dhcp-client-basics.pkt`.

