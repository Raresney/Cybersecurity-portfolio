# Useful Windows CMD Tools

## System Information

| Command | Description |
|---------|-------------|
| `set` | Display environment variables / path from the command line |
| `ver` | Display Windows version |
| `systeminfo` | Display detailed system information |
| `driverquery \| more` | Display a list of installed device drivers |
| `chkdsk` | Check the file system and disk volumes for errors and bad sectors |
| `sfc /scannow` | Scan system files for corruption and repair if needed |

## General Commands

| Command | Description |
|---------|-------------|
| `cls` | Clear the screen |
| `help` | Display help information |
| `/?` | Can be used with most commands to display a help page |
| `more` | Display output one screen at a time |
| `Ctrl + C` | Exit / interrupt a running command |

## Networking

| Command | Description |
|---------|-------------|
| `ipconfig /all` | Display full network configuration |
| `ping target_name` | Send ICMP packets and listen for response (test reachability) |
| `tracert target_name` | Trace the network route traversed to reach the target |
| `nslookup example.com` | Look up a host domain and return its IP address |
| `nslookup example.com 1.1.1.1` | Look up using a specific DNS server |
| `netstat` | Display current network connections and listening ports |
| `netstat -h` | Display netstat help page |
| `netstat -abon` | Display all connections with program names and process IDs |

### Netstat Options

| Option | Description |
|--------|-------------|
| `-a` | Display all connections |
| `-b` | Show the program associated with each listening port and established connection |
| `-o` | Reveal the process ID associated with the connections |
| `-n` | Use numerical form for addresses and port numbers |

## File System Navigation

| Command | Description |
|---------|-------------|
| `cd` | Display or change current directory |
| `dir` | List contents of current directory |
| `dir /a` | Show hidden files |
| `dir /s` | Display files in current directory and all subdirectories |
| `mkdir` | Create a directory |
| `rmdir` | Remove a directory |
| `type` | Display the contents of a file |

## File Operations

| Command | Description |
|---------|-------------|
| `copy` | Copy files |
| `move test.txt ..` | Move a file to the parent directory |
| `erase` / `del` | Delete a file |
| `copy *md C:\Markdown` | Use wildcard to copy all matching files |

## Process Management

| Command | Description |
|---------|-------------|
| `tasklist` | List all running processes |
| `tasklist /?` | Show available tasklist options |
| `tasklist /FI "imagename eq sshd.exe"` | Filter tasks by name |
| `taskkill /PID 4567` | Terminate a process by its PID |

## System Control

| Command | Description |
|---------|-------------|
| `shutdown /s` | Shut down the system |
| `shutdown /r` | Full shutdown and restart |
| `shutdown \| more` | Display shutdown help page |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
