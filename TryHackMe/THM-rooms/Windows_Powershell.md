# Windows PowerShell

## Cmdlets

PowerShell commands are called **cmdlets** (command-lets). They follow a **Verb-Noun** naming convention.

### Essential Cmdlets

| Cmdlet | Description |
|--------|-------------|
| `Get-Content` | Retrieves (gets) the content of a file and displays it in the console |
| `Set-Location` | Changes (sets) the current working directory |
| `Get-Command` | An essential tool for discovering what commands are available |

### Discovering Commands

```powershell
Get-Command -CommandType "Function"
Find-Module -Name "PowerShell*"
```

## Common Aliases

| Alias | Full Command |
|-------|-------------|
| `ac` | `Add-Content` |
| `asnp` | `Add-PSSnapin` |
| `cat` | `Get-Content` |
| `cd` | `Set-Location` |
| `CFS` | `ConvertFrom-String` |
| `chdir` | `Set-Location` |
| `clc` | `Clear-Content` |
| `clear` | `Clear-Host` |

## Piping

**Piping** is a technique used in command-line environments that allows the output of one command to be used as the input for another. This creates a sequence of operations where data flows from one command to the next. Represented by the `|` symbol.

### Examples

```powershell
Get-ChildItem | Sort-Object Length
Get-ChildItem | Where-Object -Property "Extension" -eq ".txt"
Get-ChildItem | Sort-Object Length -Descending | Select-Object -First 1   # Largest file
```

## Comparison Operators

| Operator | Meaning | Description |
|----------|---------|-------------|
| `-ne` | Not equal | Excludes objects from results based on specified criteria |
| `-gt` | Greater than | Filters only objects which exceed a specified value (strict comparison) |
| `-ge` | Greater than or equal to | Non-strict version of `-gt`; combination of `-gt` and `-eq` |
| `-lt` | Less than | Includes only objects strictly below a certain value (strict comparison) |
| `-le` | Less than or equal to | Non-strict version of `-lt`; combination of `-lt` and `-eq` |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
