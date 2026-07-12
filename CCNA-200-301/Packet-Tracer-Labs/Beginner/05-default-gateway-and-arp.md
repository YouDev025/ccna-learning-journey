# Lab 05: Default Gateway and ARP

## Objective

Observe how hosts use ARP and default gateways to communicate inside and outside the local network.

## Topology

- 1 router
- 1 switch
- 2 PCs

## Tasks

1. Configure two PCs in the same subnet.
2. Ping between PCs and inspect the ARP table.
3. Configure the router interface as the default gateway.
4. Ping the router from each PC.
5. Clear ARP entries and repeat the test.

## PC Commands

```text
arp -a
arp -d
ping
```

## Router Commands

```text
show arp
show ip interface brief
```

## Questions

- When does a PC send an ARP request?
- Why does a PC need a default gateway?
- What MAC address is used when sending traffic to another network?

## Notes

- Save the completed Packet Tracer file as `05-default-gateway-and-arp.pkt`.

