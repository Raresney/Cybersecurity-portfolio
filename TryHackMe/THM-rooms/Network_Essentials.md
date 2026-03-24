# Network Essentials

## Address Resolution Protocol (ARP)

### Analyzing ARP with tshark

```bash
tshark -r arp.pcapng -Nn
```

### Analyzing ARP with tcpdump

If we use tcpdump, the packets will be displayed differently. It uses the terms **ARP Request** and **ARP Reply**.

```bash
tcpdump -r arp.pcapng -n -v
```

**Example output:**

```
17:23:44.506615 ARP, Ethernet (len 6), IPv4 (len 4), Request who-has 192.168.66.1 tell 192.168.66.89, length 28
17:23:44.510182 ARP, Ethernet (len 6), IPv4 (len 4), Reply 192.168.66.1 is-at 44:df:65:d8:fe:6c, length 28
```

## Routing Protocols

- **OSPF** - Open Shortest Path First
- **EIGRP** - Enhanced Interior Gateway Routing Protocol
- **BGP** - Border Gateway Protocol
- **RIP** - Routing Information Protocol

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
