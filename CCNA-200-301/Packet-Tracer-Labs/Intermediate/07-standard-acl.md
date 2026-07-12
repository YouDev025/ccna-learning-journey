# Lab 07: Standard ACL

## Objective

Configure a standard access control list to restrict traffic from a specific source network.

## Topology

- 2 routers
- 2 LANs
- 2 PCs
- 1 server

## Scenario

One user LAN should be blocked from reaching the server network, while other traffic remains allowed.

## Tasks

1. Configure IP addressing and routing.
2. Verify full connectivity before applying the ACL.
3. Create a standard ACL.
4. Apply the ACL close to the destination.
5. Test blocked and permitted traffic.

## Example Commands

```text
access-list 10 deny 192.168.10.0 0.0.0.255
access-list 10 permit any
interface g0/1
ip access-group 10 out
```

## Verification

```text
show access-lists
show ip interface
ping
```

## Notes

- Save the completed Packet Tracer file as `07-standard-acl.pkt`.

