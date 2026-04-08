# Server-Side Request Forgery (SSRF)

SSRF vulnerabilities enable an attacker to trigger malicious server-to-server requests to unintended URLs. The server's trust relationship with internal systems can be abused to access data, functionality, and services not meant to be exposed externally.

---

## Labs Completed (6/6)

| # | Lab | Level |
| --- | --- | --- |
| 1 | Basic SSRF against the local server | Apprentice |
| 2 | Basic SSRF against another back-end system | Apprentice |
| 3 | SSRF with blacklist-based input filter | Practitioner |
| 4 | SSRF with whitelist-based input filter | Expert |
| 5 | SSRF with filter bypass via open redirection | Practitioner |
| 6 | Blind SSRF with out-of-band detection | Practitioner |

---

## Key Concepts

### Basic SSRF
- Manipulating server-side requests to target `localhost` or internal IPs
- Accessing admin panels via `http://127.0.0.1/admin`
- Scanning internal network ranges (e.g., `192.168.0.x`)

### Bypassing SSRF Defenses
- Blacklist bypass: URL encoding, alternative IP representations (`127.1`, `2130706433`), DNS rebinding
- Whitelist bypass: URL parsing inconsistencies, embedded credentials (`user@host`), fragment tricks
- Open redirection: chaining SSRF with open redirects to reach internal targets

### Blind SSRF
- No direct response — detected via out-of-band techniques (Burp Collaborator)
- Useful for confirming internal infrastructure and triggering further attacks
