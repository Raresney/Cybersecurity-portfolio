# Nmap - The Basics

## Network Scanning

```bash
nmap -sn 192.168.66.0/24    # Scanning a local network
nmap -sn 192.168.11.0/24    # Scanning a remote network
```

## Scan Types

| Option | Explanation |
|--------|-------------|
| `-sT` | TCP connect scan -- complete three-way handshake |
| `-sS` | TCP SYN -- only first step of the three-way handshake |
| `-sU` | UDP scan |
| `-F` | Fast mode -- scans the 100 most common ports |
| `-p[range]` | Specifies a range of port numbers -- `-p-` scans all the ports |

## Service and OS Detection

```bash
nmap -sS -O 192.168.124.211      # OS detection
nmap -sS -sV 192.168.124.211     # Service and version detection
```

| Option | Explanation |
|--------|-------------|
| `-O` | OS detection |
| `-sV` | Service and version detection |
| `-A` | OS detection, version detection, and other additions |
| `-Pn` | Scan hosts that appear to be down |

## Timing Templates

| Timing | Name | Total Duration |
|--------|------|----------------|
| T0 | Paranoid | 9.8 hours |
| T1 | Sneaky | 27.53 minutes |
| T2 | Polite | 40.56 seconds |
| T3 | Normal | 0.15 seconds |
| T4 | Aggressive | 0.13 seconds |

| Option | Explanation |
|--------|-------------|
| `-T<0-5>` | Timing template -- paranoid (0), sneaky (1), polite (2), normal (3), aggressive (4), and insane (5) |
| `--min-parallelism` / `--max-parallelism` | Minimum and maximum number of parallel probes |
| `--min-rate` / `--max-rate` | Minimum and maximum rate (packets/second) |
| `--host-timeout` | Maximum amount of time to wait for a target host |

## Verbosity and Debugging

```bash
nmap -sS 192.168.139.1/24          # Standard scan
nmap 192.168.139.1/24 -v           # Verbose output
```

## Output Formats

| Option | Explanation |
|--------|-------------|
| `-oN <filename>` | Normal output |
| `-oX <filename>` | XML output |
| `-oG <filename>` | grep-able output (useful for `grep` and `awk`) |
| `-oA <basename>` | Output in all major formats |

```bash
nmap -sS 192.168.139.1 -oA gateway
```

## Complete Reference Table

| Category | Option | Explanation |
|----------|--------|-------------|
| **List Scan** | `-sL` | List targets without scanning |
| **Host Discovery** | `-sn` | Ping scan -- host discovery only |
| **Port Scanning** | `-sT` | TCP connect scan -- complete three-way handshake |
| | `-sS` | TCP SYN -- only first step of the three-way handshake |
| | `-sU` | UDP Scan |
| | `-F` | Fast mode -- scans the 100 most common ports |
| | `-p[range]` | Specifies a range of port numbers -- `-p-` scans all the ports |
| | `-Pn` | Treat all hosts as online -- scan hosts that appear to be down |
| **Service Detection** | `-O` | OS detection |
| | `-sV` | Service version detection |
| | `-A` | OS detection, version detection, and other additions |
| **Timing** | `-T<0-5>` | Timing template -- paranoid (0) to insane (5) |
| | `--min-parallelism` / `--max-parallelism` | Minimum and maximum number of parallel probes |
| | `--min-rate` / `--max-rate` | Minimum and maximum rate (packets/second) |
| | `--host-timeout` | Maximum amount of time to wait for a target host |
| **Real-time Output** | `-v` | Verbosity level -- e.g., `-vv` and `-v4` |
| | `-d` | Debugging level -- e.g., `-d` and `-d9` |
| **Report** | `-oN <filename>` | Normal output |
| | `-oX <filename>` | XML output |
| | `-oG <filename>` | grep-able output |
| | `-oA <basename>` | Output in all major formats |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
