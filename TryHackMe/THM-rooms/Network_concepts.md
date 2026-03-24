# Network Concepts

## OSI Model Layers

| Layer | Name | Mnemonic | Function |
|-------|------|----------|----------|
| 1 | Physical | **P**lease | Physical data transmission media |
| 2 | Data Link | **D**o | Reliable data transfer between adjacent nodes |
| 3 | Network | **N**ot | Logical addressing and routing between networks |
| 4 | Transport | **T**hrow | End-to-end communication and data segmentation |
| 5 | Session | **S**picy | Establishing, maintaining, and synchronising sessions |
| 6 | Presentation | **P**izza | Data encoding, encryption, and compression |
| 7 | Application | **A**way | Providing services and interfaces to applications |

## Common Protocols

| Abbreviation | Full Name |
|-------------|-----------|
| **HTTP** | Hyper Text Transfer Protocol |
| **FTP** | File Transfer Protocol |
| **DNS** | Domain Name System |
| **POP3** | Post Office Protocol Version 3 |
| **SMTP** | Simple Mail Transfer Protocol |
| **IMAP** | The Internet Message Access Protocol |
| **MIME** | Multipurpose Internet Mail Extensions |
| **UDP** | User Datagram Protocol |
| **TCP** | Transmission Control Protocol |

## Private IP Address Ranges

| Range | CIDR |
|-------|------|
| 10.0.0.0 - 10.255.255.255 | 10/8 |
| 172.16.0.0 - 172.31.255.255 | 172.16/12 |
| 192.168.0.0 - 192.168.255.255 | 192.168/16 |

## Ports

A port number uses two octets; consequently, it ranges between **1** and **65535**; port **0** is reserved. The number 65535 is calculated by the expression `2^16 - 1`.

## Telnet

**Telnet** allows you to connect to and communicate with a remote system and issue text commands.

```bash
telnet 10.10.183.129 80
```

**Example session:**

```
Trying 10.10.183.129...
Connected to 10.10.183.129.
Escape character is '^]'.
GET / HTTP/1.1
Host: telnet.thm
```

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
