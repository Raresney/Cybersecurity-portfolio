# 🍯 SSH Honeypot – Cowrie Project

Deployment and monitoring of an SSH honeypot using **Cowrie** on a Kali Linux VM.  
The honeypot captures real attacker behavior — login attempts, executed commands, session replays, and potential malware download attempts — mimicking a SOC Analyst workflow focused on threat detection and behavioral analysis.

> Copyright (c) 2026 Bighiu Rares — [github.com/Raresney](https://github.com/Raresney)

---

## 📋 What Gets Captured

- SSH login attempts & brute-force patterns
- Executed commands and system enumeration
- IP address, timestamp, session ID
- TTY session replay (keystroke-by-keystroke)
- Potential malware download attempts

---

## ⚙️ Environment

| Component      | Details                            |
| -------------- | ---------------------------------- |
| OS             | Kali Linux (VirtualBox)            |
| Network        | Bridged Adapter                    |
| Honeypot       | Cowrie (SSH mode)                  |
| Listening Port | 22                                 |
| Python         | Virtual environment (`cowrie-env`) |

---

## 🚀 Setup

### 1. Install Cowrie

```bash
git clone https://github.com/cowrie/cowrie.git
cd cowrie
python3 -m venv cowrie-env
source cowrie-env/bin/activate
pip install --upgrade pip
pip install -e .
```

### 2. Configure Port 22

Edit `etc/cowrie.cfg`:

```ini
# Change this:
listen_endpoints = tcp:2222:interface=0.0.0.0

# To this:
listen_endpoints = tcp:22:interface=0.0.0.0
```

Allow binding to privileged port 22:

```bash
sudo touch /etc/authbind/byport/22
sudo chown <username> /etc/authbind/byport/22
sudo chmod 755 /etc/authbind/byport/22
```

### 3. Start the Honeypot

```bash
source cowrie-env/bin/activate
cowrie start
cowrie status

# Verify port binding
sudo ss -tulnp | grep 22
```

Expected output:

```
tcp   LISTEN   0   50   0.0.0.0:22   ...
```

---

## 🔍 Monitoring

### Real-Time JSON Log (commands, IPs, timestamps)

```bash
tail -f var/log/cowrie/cowrie.json
```

Example entry:

```json
{
  "eventid": "cowrie.command.input",
  "input": "uname",
  "session": "abc123",
  "protocol": "ssh"
}
```

### Standard Log

```bash
tail -f var/log/cowrie/cowrie.log
```

### TTY Session Replay

```bash
cowrie-tty-playback var/lib/cowrie/tty/<session-id>
```

Replays exactly what the attacker typed, keystroke by keystroke.

---

## 🧪 Attacker Simulation

From another device on the same network (Termux / Termius):

```bash
ssh root@<honeypot-ip>
```

Cowrie accepts any password and drops the attacker into a fake shell:

```
root@svr04:~#
```

Every command typed is logged silently.

---

## 📊 Captured Behavior Examples

| Behavior              | Description                                       |
| --------------------- | ------------------------------------------------- |
| System fingerprinting | `uname`, `cat /etc/*release`                      |
| Directory enumeration | `ls`, `pwd`, `find`                               |
| History inspection    | `cat ~/.bash_history`                             |
| Botnet patterns       | Incorrect POSIX syntax, rapid open/close sessions |
| Brute-force           | Multiple login attempts with common credentials   |

---

## 🗂️ Repository Structure

```
cowrie-honeypot-project/
├── logs/
│   ├── example-cowrie-session.json
│   ├── attacker-commands.txt
│   └── tty-session.txt
├── screenshots/
│   ├── port22-listening.png
│   ├── phone-ssh-connection.png
│   └── cowrie-json-log.png
└── README.md
```

---

## 🛠️ Skills Demonstrated

- Honeypot deployment (Cowrie)
- Linux system administration
- Virtualization & networking (bridged mode)
- JSON log analysis & TTY session replay
- Threat behavior profiling
- SOC incident investigation workflow
- Indicators of Compromise (IOCs) identification

---

## 🔮 Future Improvements

- Integrate with Splunk / ELK Stack (SIEM)
- GeoIP lookup for attacker IPs
- Automated alerting via webhooks
- Additional honeypots (HTTP, FTP, SMB)
- WAN exposure with strict network isolation

---

## ⚠️ Disclaimer

This project is conducted in a **controlled, isolated environment** for educational purposes only.  
Do not deploy honeypots on networks you do not own or without explicit authorization.
