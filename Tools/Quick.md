#Quick_tips
Simple Low-Hanging Bug: Cache purge requests are not authenticated. → curl -X PURGE https://target[.]evil[.]com → curl -s -D - https://target[.]evil[.]com -o /dev/null

Header based SQLI(use HBSQLi tool)
