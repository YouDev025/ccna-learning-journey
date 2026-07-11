# NAT CheatSheet

## NAT Types
| Type | Meaning | Use |
|---|---|---|
| Static NAT | One private IP maps to one public IP | Public access to internal server |
| Dynamic NAT | Private IP maps to a pool of public IPs | Outbound access with address pool |
| PAT/NAT overload | Many private IPs share one public IP using ports | Common internet access |

## Key Terms
- Inside local: private/internal address before translation.
- Inside global: public/translated address seen outside.
- Outside global: real address of outside host.
- Outside local: outside host address as seen inside, often same as outside global.

## PAT Example
```text
access-list 1 permit 192.168.1.0 0.0.0.255
interface gigabitEthernet0/0
 ip nat inside
interface gigabitEthernet0/1
 ip nat outside
ip nat inside source list 1 interface gigabitEthernet0/1 overload
```

## Static NAT Example
```text
ip nat inside source static 192.168.1.10 203.0.113.10
```

## Dynamic NAT Example
```text
access-list 1 permit 192.168.1.0 0.0.0.255
ip nat pool PUBLIC_POOL 203.0.113.10 203.0.113.20 netmask 255.255.255.0
ip nat inside source list 1 pool PUBLIC_POOL
```

## Verification
```text
show ip nat translations
show ip nat statistics
clear ip nat translation *
show running-config | include ip nat
```

## Troubleshooting Checklist
- Is the inside interface marked `ip nat inside`?
- Is the outside interface marked `ip nat outside`?
- Does the ACL match the correct inside source addresses?
- Is routing correct toward the internet?
- Is return traffic allowed back?

## Exam Traps
- Forgetting `overload` for PAT.
- Reversing inside and outside interfaces.
- ACL does not match the private subnet.
- NAT works only if routing also works.
