# OSPF CheatSheet

## Key Facts
- OSPF is a link-state routing protocol.
- OSPFv2 is for IPv4.
- Metric is cost.
- Administrative distance is 110.
- Single-area OSPF usually uses area 0.
- SPF algorithm calculates best paths.

## Basic Configuration
```text
router ospf 1
 router-id 1.1.1.1
 network 192.168.12.0 0.0.0.255 area 0
 network 10.1.1.0 0.0.0.255 area 0
```

## Interface Configuration
```text
interface gigabitEthernet0/0
 ip ospf 1 area 0
```

## Router ID Selection
1. Manually configured router ID.
2. Highest loopback IP address.
3. Highest active physical interface IP address.

## Neighbor Requirements
- Same area.
- Same subnet.
- Same hello/dead timers.
- Same authentication settings.
- Compatible network type.
- Interfaces are not passive.

## DR/BDR
- Used on broadcast multiaccess networks such as Ethernet.
- Highest OSPF priority wins.
- Tie-breaker is highest router ID.
- Priority `0` means the router cannot become DR/BDR.

## Useful Commands
```text
show ip ospf neighbor
show ip ospf interface brief
show ip ospf interface <interface>
show ip route ospf
show ip protocols
show running-config | section router ospf
```

## Passive Interface
```text
router ospf 1
 passive-interface gigabitEthernet0/1
```
Advertises the network but prevents neighbor formation on that interface.

## Common Problems
- Area mismatch.
- Wrong wildcard mask.
- Passive interface on router-to-router link.
- Timer mismatch.
- Authentication mismatch.
- Interface down.

## Exam Traps
- Process ID is locally significant.
- Router ID does not automatically change until OSPF process resets or device reloads.
- Wildcard masks are inverse masks, not subnet masks.
