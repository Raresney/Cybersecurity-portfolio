# Linux Shells

## Essential Commands

| Command | Description |
|---------|-------------|
| `pwd` | Check current working directory |
| `cd` | Change directory |
| `ls` | List directory contents |
| `cat` | Display file contents |
| `grep` | Search for a word in a file |
| `echo $SHELL` | Show current shell |
| `cat /etc/shells` | List available shells |
| `zsh` | Switch to zsh shell |
| `history` | Show previous commands |
| `nano` | Create/edit a script file |
| `sudo su` | Become root user |

## Writing a Bash Script

### Defining the Interpreter

```bash
#!/bin/bash
echo "Hey, what's your name?"
read name
echo "Welcome, $name"
```

Save the script by pressing `CTRL+X`. Confirm by pressing `Y` and then `ENTER`.

### Running the Script

```bash
./first_script.sh
```

### Setting Execution Permission

```bash
chmod +x first_script.sh
```

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
