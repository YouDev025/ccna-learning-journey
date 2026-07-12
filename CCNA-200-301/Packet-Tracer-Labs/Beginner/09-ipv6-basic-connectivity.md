# Lab 09: IPv6 Basic Connectivity

## Objective

Configure basic IPv6 addresses and test connectivity between devices.

## Topology

- 1 router
- 1 switch
- 2 PCs

## Addressing Table

| Device | Interface | IPv6 Address |
| --- | --- | --- |
| R1 | G0/0 | 2001:db8:acad:1::1/64 |
| PC1 | FastEthernet0 | 2001:db8:acad:1::10/64 |
| PC2 | FastEthernet0 | 2001:db8:acad:1::20/64 |

## Tasks

1. Build the topology.
2. Enable IPv6 unicast routing on the router.
3. Configure the router IPv6 address.
4. Configure IPv6 addresses on both PCs.
5. Test IPv6 connectivity.

## Example Commands

```text
ipv6 unicast-routing
interface g0/0
ipv6 address 2001:db8:acad:1::1/64
no shutdown
```

## Verification

```text
show ipv6 interface brief
ping 2001:db8:acad:1::1
```

## Notes

- Save the completed Packet Tracer file as `09-ipv6-basic-connectivity.pkt`.

