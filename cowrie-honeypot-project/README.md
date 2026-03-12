# 🦠 Automated Malware Analysis Toolkit

A professional-grade malware analysis lab environment designed for safe execution and behavioral study of suspicious binaries — combining static analysis, dynamic network monitoring, and automated orchestration in a single workflow.

> Copyright (c) 2026 Bighiu Rares — [github.com/Raresney](https://github.com/Raresney)

---

## 📋 Features

| Module                        | Description                                                        |
| ----------------------------- | ------------------------------------------------------------------ |
| 🔍 Static Analysis            | Automated MD5/SHA256 hashing and IoC extraction                    |
| 🌐 Dynamic Network Monitoring | Real-time packet inspection (DNS, TCP, UDP) to detect C2 callbacks |
| ⚙️ Automated Orchestration    | Bash-based workflow — full analysis with a single command          |

---

## ⚙️ Requirements

- Python 3.7+
- `scapy`
- Bash (Linux / WSL)

```bash
pip install scapy
```

---

## 🚀 Usage

```bash
# Set permissions
chmod +x run_lab.sh

# Run full analysis on a sample
./run_lab.sh suspicious_sample.exe

# Review generated report
cat analysis_log_*.txt
```

---

## 📊 Output

Each run generates a timestamped log file:

```
analysis_log_2026-03-12_14-32-01.txt
```

Containing:

- File hashes (MD5, SHA256)
- Extracted IoCs
- DNS queries, TCP/UDP connections
- Potential C2 callback patterns

---

## 🗂️ Repository Structure

```
Malware-Lab/
├── run_lab.sh              # Main orchestration script
├── static_analysis.py      # Hashing & IoC extraction
├── network_monitor.py      # Scapy-based packet inspection
├── samples/                # Place suspicious binaries here
├── logs/                   # Generated analysis reports
└── README.md
```

---

## 🛠️ Skills Demonstrated

- Static malware analysis (hashing, IoC extraction)
- Network traffic analysis with Scapy
- C2 callback pattern detection
- Digital forensics — structured, timestamped evidence capture
- Threat intelligence & malware behavior profiling
- Bash scripting & workflow automation

---

## ⚠️ Disclaimer

This toolkit is designed for use in **isolated, controlled lab environments only**.  
Never run malware samples on a production machine or network. Always use a dedicated VM with network isolation.
