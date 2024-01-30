---
title: Network Request 2023-12-10
created: 2024-01-22T09:59:10
modified: 2024-01-30T04:14:49
---

# Network Request 2023-12-10

Redbrick admins sent a request to ISS to open up some ports and to update them on the current state of Redbrick. This is the document that was sent outlining the changes and reasoning behind them.

## Ports

All IPs are part of 136.206.16.0/24 

| IP | Port | Reason |
| -- | ---- | ------ |
| [4,5,6,50] | 80 | HTTP traffic (only used for generating certs). |
| [4,5,6,50] | 443 | HTTPS traffic (also used for headscale). |
| [4] | 1194 | Management VPN for admins. |
| [50] | 4500-4510 | Various ports for exposing isolated containerised game servers. Used by both Redbrick and others. See [Games](#Games) |
| [50] | 6667 | IRC |
| [50] | 8448 | Matrix Federation requirement |

### Redbrick Firewall Information

Recently Redbrick acquired a new "external" firewall ([see docs](https://docs.redbrick.dcu.ie/aperture/firewall/)). This means we have audit logs, traffic identification (and categorisation), well defined access rules and fail2ban-esque blocking.

### Redbrick Internal Scans

We run a free version (limited to 16 ips) of nessus on the internal side of the 16.0/24 address range. This should alert us to vulnerabilities before they are exposed. We're inside the DCU wide scan also and action information from weekly scans.

[Link to job](https://github.com/redbrick/nomad/blob/master/jobs/nessus.hcl)

### Games

Initially we plan to run Minecraft, Factorio and Terarria servers. These will all be running inside containers with tightly restricted port access (docker network isolation) and will run using the `UID`+`GID` of a `noshell` user on the host.

### Other Access Notes

The admins have a VPN (using OpenVPN) for ssh, access to internal web UIs and switch/firewall configuration. 

### Expected Plan for the Future

The image below shows our hopeful plan for our new servers. Over the Christmas we plan to start work towards this, and some time in the new year we can discuss it further.

![](../res/ingress_topology_aperture.bmp)

## DNS

Redbrick once upon a time had `rb.dcu.ie` alongside `redbrick.dcu.ie`. If possible we'd like to acquire this again. For now `rb.dcu.ie` can be delegated to the same domain name server as `redbrick.dcu.ie`. In the future we will change our DNS system to a more robust service.
