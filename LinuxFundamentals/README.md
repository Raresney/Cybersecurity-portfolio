# Linux Commands Reference

Quick reference for essential Linux commands used in cybersecurity and system administration.

---

## Navigation & Files

| Command | Description |
| ------- | ----------- |
| `pwd` | Print current working directory |
| `ls -la` | List all files including hidden, permissions, sizes |
| `cd /path` | Change working directory |
| `mkdir -p dir/sub` | Create directories including nested ones |
| `cp -r src dest` | Copy files/directories recursively |
| `mv src dest` | Move or rename files |
| `rm -rf target` | Force delete files/directories (no confirmation!) |
| `find / -name "*.log"` | Search files by name, type, date, etc. |
| `locate filename` | Quick search from index (faster than find) |
| `tree` | Display directory structure visually |

## Reading & Editing Files

| Command | Description |
| ------- | ----------- |
| `cat file` | Display full file contents |
| `less file` | Navigate through a file (scroll up/down) |
| `head -n 20 file` | First N lines of a file |
| `tail -f file` | Follow the end of a file live (logs) |
| `nano file` | Simple, fast, intuitive editor |
| `vim file` | Advanced editor (steep learning curve, but powerful) |
| `grep -r "text" /path` | Search text recursively in files |
| `wc -l file` | Count lines in a file |
| `diff file1 file2` | Show differences between two files |

## Permissions & Ownership

| Command | Description |
| ------- | ----------- |
| `chmod 755 file` | Set permissions (rwx r-x r-x) |
| `chown user:group file` | Change file owner |
| `sudo command` | Run command as root (superuser) |

## Processes & System

| Command | Description |
| ------- | ----------- |
| `ps aux` | List all active processes |
| `top` / `htop` | Live CPU, RAM, process monitor |
| `kill -9 PID` | Force kill a process by PID |
| `systemctl start/stop svc` | Start/stop a systemd service |
| `systemctl status svc` | Check service status |
| `df -h` | Free disk space (human-readable) |
| `du -sh *` | Size of each directory/file |
| `free -h` | RAM: total, used, free |
| `uptime` | System uptime + load average |

## Networking

| Command | Description |
| ------- | ----------- |
| `ip a` / `ifconfig` | Display interface IP addresses |
| `ping host` | Test connectivity to a host |
| `curl URL` | Make HTTP request (API testing, download) |
| `wget URL` | Download files from the web |
| `ss -tulnp` | Open ports and listening services |
| `ssh user@host` | Secure remote connection |
| `scp file user@host:/p` | Copy files between machines via SSH |

## Piping & Redirection

| Command | Description |
| ------- | ----------- |
| `cmd1 \| cmd2` | Pipe output of cmd1 as input to cmd2 |
| `cmd > file` | Write output to file (overwrite) |
| `cmd >> file` | Append output to end of file |
| `cmd 2>&1` | Redirect errors together with output |

## Archives & Packages

| Command | Description |
| ------- | ----------- |
| `tar -czf a.tar.gz dir/` | Compress a directory into .tar.gz archive |
| `tar -xzf a.tar.gz` | Extract a .tar.gz archive |
| `apt update && upgrade` | Update package list + upgrade |
| `apt install package` | Install a package (Debian/Ubuntu) |
| `dnf install package` | Install a package (Fedora/RHEL) |

## Useful Combos

| Command | Description |
| ------- | ----------- |
| `history \| grep "x"` | Search previously run commands |
| `xargs` | Transform output into arguments for another command |
| `sed 's/old/new/g' file` | Replace text in files (find & replace) |
| `awk '{print $2}' file` | Extract specific columns from text |
| `crontab -e` | Edit scheduled tasks (cron jobs) |
| `ln -s target link` | Create a symlink (shortcut) |
