# Linux Commands Reference

Quick reference for essential Linux commands used in cybersecurity and system administration.

---

## Navigare & fisiere

| Comanda | Descriere |
| ------- | --------- |
| `pwd` | Afiseaza directorul curent |
| `ls -la` | Listeaza tot: fisiere ascunse, permisiuni, dimensiuni |
| `cd /path` | Schimba directorul de lucru |
| `mkdir -p dir/sub` | Creeaza directoare inclusiv nested |
| `cp -r src dest` | Copiaza fisiere/directoare recursiv |
| `mv src dest` | Muta sau redenumeste fisiere |
| `rm -rf target` | Sterge fortat fisiere/directoare (fara confirmare!) |
| `find / -name "*.log"` | Cauta fisiere dupa nume, tip, data etc. |
| `locate filename` | Cauta rapid din index (mai rapid ca find) |
| `tree` | Afiseaza structura de directoare vizual |

## Citit & editat fisiere

| Comanda | Descriere |
| ------- | --------- |
| `cat file` | Afiseaza continutul complet al fisierului |
| `less file` | Navigheaza prin fisier (scroll sus/jos) |
| `head -n 20 file` | Primele N linii din fisier |
| `tail -f file` | Urmareste live sfarsitul fisierului (logs) |
| `nano file` | Editor simplu, rapid, intuitiv |
| `vim file` | Editor avansat (curba de invatare, dar puternic) |
| `grep -r "text" /path` | Cauta text recursiv in fisiere |
| `wc -l file` | Numara liniile dintr-un fisier |
| `diff file1 file2` | Arata diferentele intre doua fisiere |

## Permisiuni & ownership

| Comanda | Descriere |
| ------- | --------- |
| `chmod 755 file` | Seteaza permisiuni (rwx r-x r-x) |
| `chown user:group file` | Schimba proprietarul fisierului |
| `sudo command` | Ruleaza comanda ca root (superuser) |

## Procese & sistem

| Comanda | Descriere |
| ------- | --------- |
| `ps aux` | Listeaza toate procesele active |
| `top` / `htop` | Monitor live CPU, RAM, procese |
| `kill -9 PID` | Omoara fortat un proces dupa PID |
| `systemctl start/stop svc` | Porneste/opreste un serviciu systemd |
| `systemctl status svc` | Verifica starea unui serviciu |
| `df -h` | Spatiu liber pe disk (human-readable) |
| `du -sh *` | Dimensiunea fiecarui director/fisier |
| `free -h` | Memorie RAM: totala, folosita, libera |
| `uptime` | De cat timp e pornit sistemul + load |

## Retea

| Comanda | Descriere |
| ------- | --------- |
| `ip a` / `ifconfig` | Afiseaza adresele IP ale interfetelor |
| `ping host` | Testeaza conectivitatea la un host |
| `curl URL` | Face request HTTP (testare API, download) |
| `wget URL` | Descarca fisiere de pe web |
| `ss -tulnp` | Porturi deschise si ce le asculta |
| `ssh user@host` | Conectare remota securizata |
| `scp file user@host:/p` | Copiaza fisiere intre masini via SSH |

## Piping & redirectare

| Comanda | Descriere |
| ------- | --------- |
| `cmd1 \| cmd2` | Trimite output-ul lui cmd1 ca input la cmd2 |
| `cmd > file` | Scrie output in fisier (suprascrie) |
| `cmd >> file` | Adauga output la sfarsitul fisierului |
| `cmd 2>&1` | Redirectioneaza si erorile impreuna cu output |

## Arhive & pachete

| Comanda | Descriere |
| ------- | --------- |
| `tar -czf a.tar.gz dir/` | Comprima un director in arhiva .tar.gz |
| `tar -xzf a.tar.gz` | Extrage o arhiva .tar.gz |
| `apt update && upgrade` | Actualizeaza lista de pachete + upgrade |
| `apt install pachet` | Instaleaza un pachet (Debian/Ubuntu) |
| `dnf install pachet` | Instaleaza un pachet (Fedora/RHEL) |

## Combo-uri utile

| Comanda | Descriere |
| ------- | --------- |
| `history \| grep "x"` | Cauta in comenzile rulate anterior |
| `xargs` | Transforma output in argumente pt alta comanda |
| `sed 's/old/new/g' file` | Inlocuieste text in fisiere (find & replace) |
| `awk '{print $2}' file` | Extrage coloane specifice din text |
| `crontab -e` | Editeaza taskuri programate (cron jobs) |
| `ln -s target link` | Creeaza un symlink (scurtatura) |
