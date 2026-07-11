# CCNA Commands CheatSheet

## Device Basics
```text
show running-config
show startup-config
copy running-config startup-config
show version
show clock
show history
```

## Interfaces
```text
show ip interface brief
show ipv6 interface brief
show interfaces
show interfaces status
show running-config interface <interface>
no shutdown
shutdown
```

## VLANs and Trunks
```text
show vlan brief
show interfaces trunk
show interfaces switchport
show mac address-table
vlan 10
 name USERS
interface fa0/1
 switchport mode access
 switchport access vlan 10
```

## Routing
```text
show ip route
show ipv6 route
show ip protocols
show arp
show ipv6 neighbors
ping <ip-address>
traceroute <ip-address>
```

## Static Routes
```text
ip route <network> <mask> <next-hop>
ip route 0.0.0.0 0.0.0.0 <next-hop>
ipv6 route <prefix>/<length> <next-hop>
ipv6 route ::/0 <next-hop>
```

## OSPF
```text
show ip ospf neighbor
show ip ospf interface brief
show ip route ospf
router ospf 1
 router-id 1.1.1.1
 network 192.168.1.0 0.0.0.255 area 0
```

## EtherChannel
```text
show etherchannel summary
show interfaces port-channel 1
interface range g0/1 - 2
 channel-group 1 mode active
```

## STP
```text
show spanning-tree
show spanning-tree vlan 10
spanning-tree mode rapid-pvst
spanning-tree vlan 10 root primary
```

## CDP and LLDP
```text
show cdp neighbors
show cdp neighbors detail
show lldp neighbors
show lldp neighbors detail
```

## Security
```text
show access-lists
show port-security
show port-security interface <interface>
show ip dhcp snooping
show users
show ssh
```

## Management Access
```text
hostname SW1
ip domain-name example.local
crypto key generate rsa
ip ssh version 2
username admin secret <password>
line vty 0 15
 login local
 transport input ssh
```

## Save Your Work
```text
copy running-config startup-config
write memory
```
