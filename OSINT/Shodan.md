Searching for CVE's:
( Test case Jenkins)
product: Jenkins -"2.442"-"2.426.3"



Interesting IP's from shodan:
cat ips.txt | httpx > live-ips.txt
cat live-ips.txt | dirsearch --stdin

#Searches
Use the last modifed and content length headers to get original IP(Thus bypass waf)

\*ssl.cert.fingerprint:”${target}”\*
\*ssl:”${target}”*
\*org:”${target}”*
\*hostname:”${target}”* 
\*[http://ssl.cert.issuer.cn(https://t.co/7FaohrNnvA):”${target}”*
“log in with” ssl:”${target}”
“log in with” hostname:”\*.${target}”
http.status:”302" sso [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
http.status:”302" sso ssl:”${target}” http.status:”302" sso hostname:”*.${target}”http.status:”302" oauth hostname:”\*.${target}”
http.title:”log in with” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
http.title:”log in with” ssl:”${target}”
http.title:”log in with” hostname:”\*.${target}”
“log in with” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
http.status:”302" oauth ssl:”${target}”
http.status:”302" oauth [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
“LogIn” hostname:”\*.${target}”
“LogIn” ssl:”${target}”
LogIn” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
http.title:”LogIn” hostname:”\*.${target}”
http.title:”LogIn” ssl:”${target}”
http.title:”LogIn” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
“sign up” hostname:”\*.${target}”
“sign up” ssl:”${target}”
title:”Login — Adminer” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
http.title:”sign up” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
http.title:”sign up” ssl:”${target}”
http.title:”sign up” hostname:”\*.${target}”
“sign up” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
title:”Login — Adminer” hostname:”\*.${target}”
“Authentication: disabled” port:445 product:”Samba” hostname:”\*.${target}”
ftp port:”10000" [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”
ftp port:”10000" hostname:”\*.${target}”
\*http.title:”Index of /” [http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”\*
\*http.title:”Index of /” hostname:”\*.${target}”*
\*ssl.cert.subject.commonName:”.${target}”\*
\*ssl.cert.expired:true hostname:”.${target}”\*
\*[http://ssl.cert.subject.cn](https://t.co/NraBmIC8nH):”${target}”\*

ssl.cert.subject.CN:"gevme.com*" 200
ssl.cert.subject.CN:"*.target.com" "230 login successful" port:"21"
ssl.cert.subject.CN:"*.target.com"+200 http.title:"Admin"
Set-Cookie:"mongo-express=" "200 OK"
ssl:"invisionapp.com" http.title:"index of / "
ssl:"arubenetworks.com" 200 http.title:"dahsboard"
net:192.168.43/24, 192.168.40/24

AEM login apnel :- git clone https://github.com/0ang3el/aem-hacker.git
User:anonymous Pass:anonymous

Finding index files:
ssl.cert.subject.CN:"target.com" http.title:"index of/"

Finding admin panel:
ssl.cert.subject.CN:"\*.target.com" "230 login successful" port:"21"

Exposed API key:
http.html:"xoxb-"

Finding Jenkins server via Favicon:
ssl."\*\.hydroshare.org" http.favicon.hash:81586312

Multiple services for favicon hashsh:
https://github.com/sansatart/scrapts/blob/master/shodan-favicon-hashes.csv

Finding Graphana Dashboard:
http.title:"Graphana"

Search for a particular CVE:
vuln:CVE-2014-0160

Search particular Prts and Services:
ssh -port:22

Airbyte panel bypass:
http.title:"Airbyte":200

XSS Vuln via Citrix Gateway:
ssl:"domain.com" 200 http.title:"citrix gateway"