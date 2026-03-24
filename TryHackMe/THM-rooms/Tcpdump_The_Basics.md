# Tcpdump: The Basics

Tcpdump is built on **libpcap**, a portable C/C++ library for network traffic capture.

## Getting Started

### Check Available Network Interfaces

```bash
ip a s
```

### Basic Capture

```bash
sudo tcpdump -i ens5 -c 5 -n
```

## Core Options

| Command | Explanation |
|---------|-------------|
| `tcpdump -i INTERFACE` | Captures packets on a specific network interface |
| `tcpdump -w FILE` | Writes captured packets to a file |
| `tcpdump -r FILE` | Reads captured packets from a file |
| `tcpdump -c COUNT` | Captures a specific number of packets |
| `tcpdump -n` | Don't resolve IP addresses |
| `tcpdump -nn` | Don't resolve IP addresses and don't resolve protocol numbers |
| `tcpdump -v` | Verbose display; verbosity can be increased with `-vv` and `-vvv` |

## Filtering Traffic

### Capture by Host

```bash
sudo tcpdump host example.com -w http.pcap
```

### Capture by Port

```bash
sudo tcpdump -i ens5 port 53 -n
```

### Filter Options

| Command | Explanation |
|---------|-------------|
| `tcpdump host IP` or `tcpdump host HOSTNAME` | Filters packets by IP address or hostname |
| `tcpdump src host IP` | Filters packets by a specific source host |
| `tcpdump dst host IP` | Filters packets by a specific destination host |
| `tcpdump port PORT_NUMBER` | Filters packets by port number |
| `tcpdump src port PORT_NUMBER` | Filters packets by the specified source port number |
| `tcpdump dst port PORT_NUMBER` | Filters packets by the specified destination port number |
| `tcpdump PROTOCOL` | Filters packets by protocol (e.g., `ip`, `ip6`, `icmp`) |

## Advanced Examples

### Filter ARP by Host

```bash
sudo tcpdump -r traffic.pcap arp and host 192.168.124.137
```

### Count TCP Reset Packets

```bash
sudo tcpdump -r traffic.pcap 'tcp[tcpflags] == tcp-rst' | wc -l
```

## Display Options

| Command | Explanation |
|---------|-------------|
| `tcpdump -q` | Quick and quiet: brief packet information |
| `tcpdump -e` | Include MAC addresses |
| `tcpdump -A` | Print packets as ASCII encoding |
| `tcpdump -xx` | Display packets in hexadecimal format |
| `tcpdump -X` | Show packets in both hexadecimal and ASCII formats |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
