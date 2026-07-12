# Lab 04: OSPF Single Area

## Objective

Configure single-area OSPF and verify dynamic route learning.

## Topology

- 3 routers
- 3 LANs
- Serial or Ethernet WAN links

## Tasks

1. Configure IP addresses on all router interfaces.
2. Enable OSPF process 1.
3. Advertise connected networks into area 0.
4. Verify OSPF neighbors.
5. Verify the routing table.
6. Test end-to-end connectivity.

## Example Commands

```text
router ospf 1
network 192.168.1.0 0.0.0.255 area 0
network 10.0.0.0 0.0.0.3 area 0
```

## Verification

```text
show ip ospf neighbor
show ip route ospf
show ip protocols
```

## Notes

- Save the completed Packet Tracer file as `04-ospf-single-area.pkt`.

