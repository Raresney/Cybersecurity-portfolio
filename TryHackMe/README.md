# 🛡️ TryHackMe — Notes & Writeups

Personal notes, commands, and key concepts documented while working through TryHackMe rooms and learning paths.

---

## 🏆 Certifications

| Badge           | Path          | Date             | Duration |
| --------------- | ------------- | ---------------- | -------- |
| ✅ Pre Security | Learning Path | October 12, 2025 | 7h 38min |

> Certificate ID: `THM-K99YJTN5HJ`

---

## 📁 Structure

```
TryHackMe/
├── THM-rooms/
│   ├── Criptography.md
│   ├── LAN_Topologies.md
│   ├── Linux_shells.md
│   ├── Metasploit_and_Hydra.md
│   ├── Network_concepts.md
│   ├── Network_Essentials.md
│   ├── Network_Secure_Protocols.md
│   ├── Nmap_-_The_Basics.md
│   ├── Packets_and_Frames.md
│   ├── Public_Key_Cryptography_Basics.md
│   ├── Security_Information_and_Event_Management.md
│   ├── SOC_fundamentals.md
│   ├── Tcpdump_The_Basics.md
│   ├── Useful_tool-thm.md
│   └── Windows_Powershell.md
├── Pre Security.pdf
└── README.md
```

---

## 📚 Topics Covered

### 🌐 Networking

- **LAN Topologies** — Ring, star, bus topologies; ARP protocol; DHCP flow (Discover → Offer → Request → ACK); OSI model layers
- **Network Concepts** — OSI & TCP/IP models; protocols (HTTP, FTP, DNS, SMTP, IMAP, UDP, TCP); private IP ranges; port numbers
- **Network Essentials** — ARP with `tshark` and `tcpdump`; routing protocols (OSPF, BGP, RIP, EIGRP)
- **Packets and Frames** — Layer 2 vs Layer 3 encapsulation; TCP/IP stack
- **Network Secure Protocols** — SFTP (port 22), FTPS (port 990), TLS-based protocol security

### 🔐 Cryptography

- **Cryptography** — Plaintext/ciphertext/cipher/key definitions; XOR logic; historical ciphers (Caesar, Vigenère, Enigma)
- **Public Key Cryptography** — RSA math (prime factoring); Diffie-Hellman; DSA, ECDSA, Ed25519; GPG; `ssh-keygen`

### 🛠️ Tools & Recon

- **Nmap** — Host discovery, port scanning, service/OS detection, timing templates (T0–T5), output formats
- **Tcpdump** — Interface capture, filters (host, port, protocol), output flags, TCP flag analysis
- **Metasploit** — `msfconsole`, modules overview
- **Hydra** — Brute-force SSH and web forms (GET/POST); key flags (`-l`, `-P`, `-t`, `-V`)

### 💻 OS & Scripting

- **Linux Shells** — Core commands (`pwd`, `ls`, `grep`, `cat`); bash scripting; `chmod +x`; `sudo su`
- **Windows PowerShell** — Cmdlets (`Get-Content`, `Get-ChildItem`, `Get-Command`); piping; comparison operators (`-eq`, `-gt`, `-lt`)
- **Useful Tools (Windows CMD)** — `ipconfig`, `netstat`, `tracert`, `nslookup`, `tasklist`, `taskkill`, `sfc`, `shutdown`

### 🔍 SOC & SIEM

- **SOC Fundamentals** — L1/L2/L3 analyst roles; Detection Engineer; SOC Manager; incident triage (5 Ws)
- **SIEM** — Log collection and correlation; false positive handling; CyberChef for data analysis

---

## 🔧 Quick Reference — Key Commands

```bash
# Nmap
nmap -sS -sV -O <target>          # SYN scan + version + OS detection
nmap -sS -T4 -p- <target>         # Full port scan, aggressive timing
nmap -sS <target> -oA output      # Save results in all formats

# Tcpdump
sudo tcpdump -i eth0 -c 50 -nn             # Capture 50 packets, no resolution
sudo tcpdump -r file.pcap port 80 -A       # Read pcap, filter port 80, ASCII output
sudo tcpdump -r file.pcap 'tcp[tcpflags] == tcp-rst' | wc -l  # Count RST packets

# Hydra
hydra -l admin -P rockyou.txt <IP> ssh -t 4                        # SSH brute-force
hydra -l admin -P rockyou.txt <IP> http-post-form "/login:user=^USER^&pass=^PASS^:F=incorrect" -V

# Metasploit
msfconsole
use exploit/...
set RHOSTS <target>
run
```

---

## 📌 Notes

- Notes are raw and personal — they capture what matters, not everything.
- Commands are tested in TryHackMe's AttackBox unless noted otherwise.
- This folder will grow as more rooms and paths are completed.

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
