# Lab 12: DNS and Web Server Test

## Objective

Configure a simple server and test access by IP address and hostname.

## Topology

- 1 switch
- 1 server
- 2 PCs

## Addressing Table

| Device | IP Address | Subnet Mask |
| --- | --- | --- |
| Server1 | 192.168.100.10 | 255.255.255.0 |
| PC1 | 192.168.100.20 | 255.255.255.0 |
| PC2 | 192.168.100.30 | 255.255.255.0 |

## Tasks

1. Configure IP addresses on the server and PCs.
2. Enable HTTP service on the server.
3. Enable DNS service on the server.
4. Add a DNS record for `www.lab.local`.
5. Configure PCs to use the server as their DNS server.
6. Test web access using the hostname.

## Verification

```text
ping 192.168.100.10
```

From a PC web browser:

```text
http://www.lab.local
```

## Notes

- Save the completed Packet Tracer file as `12-dns-and-web-server-test.pkt`.

