#nmap
nmap -sC -sV ip
nmap -n -sV --script "ldap* and not brute" mail/smtp.\*.domain/ip
nmap --script vuln ip

#masscan
cat domains.txt | httpx -ip -silent | awk '{print \$2}' | sed -e 's/\\\[//g' -e 's/\\]//g' | tee ips.txt | while read url; do mass=\$(sudo masscan --ports 0-65535 \$url); echo -e "\$url \n \$mass"; done

**prips 93.184.216.0/24 | hakoriginfinder -h example[.]com**
Scans for origin IP addresses even when blocked by WAFs