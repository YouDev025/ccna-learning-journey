# VLAN CheatSheet

## Key Facts
- VLANs create separate Layer 2 broadcast domains.
- Devices in different VLANs need Layer 3 routing to communicate.
- Access ports carry one data VLAN.
- Trunk ports carry multiple VLANs.
- 802.1Q is the standard trunk tagging method.
- VLAN 1 is the default VLAN on Cisco switches.

## VLAN Commands
```text
show vlan brief
vlan 10
 name USERS
vlan 20
 name VOICE
```

## Access Port
```text
interface fastEthernet0/10
 switchport mode access
 switchport access vlan 10
 spanning-tree portfast
```

## Voice VLAN
```text
interface fastEthernet0/11
 switchport mode access
 switchport access vlan 10
 switchport voice vlan 20
 spanning-tree portfast
```

## Trunk Port
```text
interface gigabitEthernet0/1
 switchport mode trunk
 switchport trunk native vlan 999
 switchport trunk allowed vlan 10,20,99
```

## Verify Trunks
```text
show interfaces trunk
show interfaces switchport
show running-config interface <interface>
```

## Inter-VLAN Routing with SVI
```text
ip routing
interface vlan 10
 ip address 192.168.10.1 255.255.255.0
 no shutdown
interface vlan 20
 ip address 192.168.20.1 255.255.255.0
 no shutdown
```

## Router-on-a-Stick
```text
interface gigabitEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
```

## Native VLAN
- Native VLAN carries untagged trunk traffic.
- Default native VLAN is VLAN 1.
- Both trunk ends should match.
- Best practice: use an unused native VLAN.

## Exam Traps
- VLAN must exist before access assignment is useful.
- Missing VLAN on allowed trunk list breaks connectivity.
- Native VLAN mismatch causes problems.
- Inter-VLAN routing needs a router or Layer 3 switch.
