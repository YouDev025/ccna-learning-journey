# Lab 06: NAT Overload PAT

## Objective

Configure Port Address Translation so multiple inside hosts can reach an outside network using one public address.

## Topology

- 1 inside router
- 1 ISP router
- 1 switch
- 2 PCs
- 1 server on the outside network

## Tasks

1. Configure inside and outside router interfaces.
2. Configure a default route toward the ISP.
3. Create an ACL matching the inside LAN.
4. Configure NAT overload.
5. Test connectivity from inside PCs to the outside server.

## Example Commands

```text
access-list 1 permit 192.168.10.0 0.0.0.255
ip nat inside source list 1 interface g0/1 overload
interface g0/0
ip nat inside
interface g0/1
ip nat outside
```

## Verification

```text
show ip nat translations
show ip nat statistics
ping
```

## Notes

- Save the completed Packet Tracer file as `06-nat-overload-pat.pkt`.

