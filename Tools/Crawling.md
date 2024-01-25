cat subs.txt | httpx -title -status-code

#KATANA

**katana -u https://www.temu.com/?fcbz=1 -rd 2  --proxy http://127.0.0.1:8080 -o katana_results.txt**

Katana is a CRAWLER(get that, a CRAWLER!). This command crawls fo rvarious endpoints from the above link with a basic delay of 2 seconds using the Burp proxy and outputs the results in the above txt file.

**while read sub; do echo "$sub" | timeout 300s katana -j -or -ob -hl -xhr | jq '.response.xhr_requests[] | select(.method == "GET") | .endpoint' | tee -a foundXHRGets.txt; done<subs.txt**

Combines bash scripting with KATANA. It reads for JS files and their XHR requests thus checking for hidden endpoints.
**-hl** is for crawling head-lessly(for dynamic web applications)

**katana -cos /logout /sendMoneyTo**
Prevents crawling to endpoints that may lose functionality of the account

**while read sub; do echo "$sub" | timeout 300s katana -kf sitemapxml -s breadth-first -iqp -hl -ef png,jpg,jpeg,css,js,svg -c 30 -do -jsonl | jq -r '.request | select(.attribute == "href") | select(.endpoint | contains("twitter") or contains("github")) | .endpoint' done<subs.txt | tee -a foundTwitterAndGitHub.txt**
Goes and checks for out of scope targets. Helps find P4 roken links and path traversals among others.

#HAKRAWLER
**hakrawler -domain https://url.com/**



