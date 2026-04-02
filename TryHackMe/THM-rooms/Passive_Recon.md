Purpose	Commandline 				    Example
Lookup WHOIS record			            whois tryhackme.com
Lookup DNS A records			        nslookup -type=A tryhackme.com
Lookup DNS MX records at DNS server	    nslookup -type=MX tryhackme.com 1.1.1.1
Lookup DNS TXT records			        nslookup -type=TXT tryhackme.com
Lookup DNS A records			        dig tryhackme.com A
Lookup DNS MX records at DNS server	    dig @1.1.1.1 tryhackme.com MX
Lookup DNS TXT records			        dig tryhackme.com TXT
