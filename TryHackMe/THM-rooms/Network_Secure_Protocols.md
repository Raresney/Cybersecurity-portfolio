# Network Secure Protocols

## SFTP (SSH File Transfer Protocol)

**SFTP** stands for SSH File Transfer Protocol and allows secure file transfer. It is part of the SSH protocol suite and shares the same port number, **22**.

If enabled in the OpenSSH server configuration, you can connect using:

```bash
sftp username@hostname
```

Once logged in, you can issue commands such as:

```bash
get filename    # Download a file
put filename    # Upload a file
```

Generally speaking, SFTP commands are Unix-like and can differ from FTP commands.

## FTPS (File Transfer Protocol Secure)

**SFTP should not be confused with FTPS.** FTPS stands for File Transfer Protocol Secure and is secured using **TLS**, just like HTTPS.

| Protocol | Port | Security |
|----------|------|----------|
| FTP | 21 | None |
| FTPS | 990 | TLS |
| SFTP | 22 | SSH |

FTPS requires certificate setup, and it can be tricky to allow over strict firewalls as it uses separate connections for control and data transfer.

## TLS-Based Secure Protocols

Setting up an SFTP server is as easy as enabling an option within the OpenSSH server. Like **HTTPS**, **SMTPS**, **POP3S**, **IMAPS**, and other protocols that rely on TLS for security, FTPS requires a proper TLS certificate to run securely.

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
