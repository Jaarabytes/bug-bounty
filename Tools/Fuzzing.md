#Ffuf

**ffuf -w wordlist -u target/FUZZ -mc 200,403 -c -v -recursion**
Scans recursively and Matches for 200 Ok and 403 unathorized status codes with verbose and colorized output

**gobuster dir -u target -w wordlist --delay 2000**
The delay is necessary since most programs hate traffic

subfinder -d soundtrackyourbrand.com -all -silent -o subfinder.txt