Try:
naabu -host <ip> -p - -Pn -o portscan | httpx -sc -td -server

Nuclei for weak FTP:
cat port-scanned-hosts.txt | grep -E ':21$' | awk -F: '{print $1}' | nuclei -nh -id ftp-anonymous-login,ftp-weak-credentials

Nuclei for weak/anonymous LDAP
cat port-scanned-hosts.txt | grep -E ':389$' | awk -F: '{print $1}' | nuclei -nh -id ldap-anonymous-login

**Shodan favicon hash**:
One-liner of favicon hash for shodan: python3 -c "import mmh3,requests,codecs;print(mmh3.hash(codecs.encode(requests.get('[URL]',verify=False).content,'base64')))" Replace URL with [http://target.com/favicon.ico](https://t.co/j1P2Dv0XlG) and use http.favicon.hash:<HASH>


Reading sensitive pdf files:
(httpx, gau and pdftotext have to be installed)
for i in `cat apex-domains.txt | gau --subs --threads 16 | grep -Ea '\.pdf' | httpx -silent -mc 200`; do if curl -s "$i" | pdftotext -q - - | grep -Eaiq 'internal use|classified'; then echo [$i](https://twitter.com/search?q=%24i&src=cashtag_click); fi; done

For LFI:
paramspider -d target.com -o urls.txt | \
  while read -r URL; do
    ffuf -u "${URL}" -c -w /root/FUZZDB/Seclists/Fuzzing/LFI/LFI-JHaddix.txt -ac
  done

For Open redirect:
gau target.com | grep -a -i '=https' | \
  qsreplace 'http://evil.com' | \
  while read -r host; do
    if curl -s -L "$host" -I | grep -q "evil.com"; then
      echo -e "$host \033[0;31mVulnerable\n"
    fi
  done
