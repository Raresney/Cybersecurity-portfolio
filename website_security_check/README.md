# 🔒 Simple Website Security Check Tool

A lightweight Python CLI tool that performs basic security checks on any website — HTTPS verification, security headers audit, WAF detection, CMS fingerprinting, and directory listing exposure.

> Copyright (c) 2026 Bighiu Rares — [github.com/Raresney](https://github.com/Raresney)

---

## 📋 Features

| Check                | Description                                                                                                                                  |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| ✅ HTTPS             | Verifies if the site uses a secure connection                                                                                                |
| 🔍 Security Headers  | Detects missing headers (`Content-Security-Policy`, `X-Frame-Options`, `Strict-Transport-Security`, `Referrer-Policy`, `Permissions-Policy`) |
| 🛡️ WAF Detection     | Identifies Web Application Firewalls and CDN signatures                                                                                      |
| 🧩 CMS Detection     | Fingerprints WordPress, Joomla, Drupal, Magento                                                                                              |
| 📂 Directory Listing | Flags exposed directory indexes                                                                                                              |
| 💾 Export Reports    | Save results as JSON or HTML                                                                                                                 |

---

## ⚙️ Requirements

- Python 3.7+
- `requests`

```bash
pip install requests
```

---

## 🚀 Usage

```bash
python security_check.py <url> [--output json|html]
```

### Examples

```bash
# Basic scan (terminal output only)
python security_check.py https://example.com

# Save report as JSON
python security_check.py https://example.com --output json

# Save report as HTML
python security_check.py example.com --output html
```

> If you omit `https://`, the tool adds it automatically.

---

## 📊 Sample Output

```
HTTPS: ✅ HTTPS is active.
Missing Security Headers: Permissions-Policy, Content-Security-Policy
WAF Detection: Server: nginx, CF-RAY: abc123def456
CMS Detection: WordPress
Directory Listing: Directory listing not found.
```

When `--output` is used, a file is saved in the current directory:

| Format | Filename example                   |
| ------ | ---------------------------------- |
| JSON   | `security_report_example_com.json` |
| HTML   | `security_report_example_com.html` |

---

## 🗂️ Project Structure

```
security_check.py   # Main script — all logic included
README.md           # This file
```

---

## ⚠️ Disclaimer

This tool is intended for **educational and authorized testing purposes only**.  
Do not use it against websites you do not own or have explicit permission to scan.

---

## 📄 License

Copyright (c) 2026 Bighiu Rares  
[github.com/Raresney](https://github.com/Raresney)
