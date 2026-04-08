# OS Command Injection

Command injection vulnerabilities enable an attacker to execute arbitrary operating system commands on the server, giving them full control over the application and all of its data.

---

## Labs Completed (5/5)

| # | Lab | Level |
| --- | --- | --- |
| 1 | OS command injection, simple case | Apprentice |
| 2 | Blind OS command injection with time delays | Practitioner |
| 3 | Blind OS command injection with output redirection | Practitioner |
| 4 | Blind OS command injection with out-of-band interaction | Practitioner |
| 5 | Blind OS command injection with out-of-band data exfiltration | Practitioner |

---

## Key Concepts

### What is OS Command Injection?
- Injecting OS commands via application parameters that are passed to system shell functions
- Enables full server compromise

### Useful Commands
- Linux: `whoami`, `uname -a`, `ifconfig`, `cat /etc/passwd`
- Windows: `whoami`, `ver`, `ipconfig`, `type C:\boot.ini`

### Injecting OS Commands
- Shell metacharacters: `; | || & && \` \` $() > <`
- Simple case: injecting directly into vulnerable parameters (e.g., `; whoami`)

### Blind Command Injection
- Time delays: `; sleep 10` to confirm execution
- Output redirection: writing command output to a web-accessible file
- Out-of-band (OOB): using `nslookup` or `curl` to exfiltrate data via DNS/HTTP to an external server (Burp Collaborator)
