Starters(
If the webpage sets a 404 not found, chnage the domain name to the website's IP adress
)


My favorite Google dork flow: 
1. Start w/ "site:domain" 
2. Remove stuff "-www" 
3. Keep reading and removing until you get to the fun stuff Example: site:tesla .com -www -shop -share -ir -mfa


**For the goodies:**
site:tesla.com ext:log | ext:txt | ext:conf | ext:cnf | ext:ini | ext:env | ext:sh | ext:bak | ext:backup | ext:swp | ext:old | ext:~ | ext:git | ext:svn | ext:htpasswd | ext:htaccess

site:target[.]com ext:php

site:target[.]com ext:jsp | ext:asp | ext:aspx | ext:pl | ext:cfm | ext:py | ext:rb

site:redcare.it ext:(log | conf | txt | cnf | ini | env | sh | bak | backup | swp | old | ~ | git | svn | htpasswd | htaccess)

**For test environments:**
inurl:demo | inurl:dev | inurl:staging | inurl:stg | inurl:test | inurl:sandbox site:example[.]com

Deep subdomains:
site:\*.\*.\*.target[.]com

Error pages:
intext:"error" | intext:"exception" | intext:"not found" | intext:"failed" site:example[.]com

All TLDs:
site:target.*

Sensitive information:
inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:target[.]com

For XSS:
inurl:q= | inurl:s= | inurl:search= | inurl:query= | inurl:keyword= | inurl:lang= inurl:& site:target[.]com

For Apache:(Look for sensitive information)
site:\*/server-status apache

Inurl:
inurl:config | inurl:env | inurl:setting | inurl:backup | inurl:admin | inurl:php site:example[.]com

XSS and Open redirects:
site:openbugbounty[.]org inurl:reports intext:"target[.]"

inurl:url= | inurl:return= | inurl:next= | inurl:redirect= | inurl:redir= | inurl:ret= | inurl:r2= | inurl:page= inurl:& inurl:http site:target[.]com

SSRF:
inurl:http | inurl:proxy= | inurl:html= | inurl:data= | inurl:resource= inurl:& site:target[.]com

SQLi:
inurl:id= | inurl:pid= | inurl:category= | inurl:cat= | inurl:action= | inurl:sid= | inurl:dir= inurl:& site:example[.]com

Finding everything:

 site:target[.]com 
 Remove noise w/ negative search: -site:www[.]target[.]com -inurl:news -ir 
 Keep going until you find everything

Index.of

RCE:
inurl:cmd | inurl:exec= | inurl:query= | inurl:code= | inurl:do= | inurl:run= | inurl:read= | inurl:ping= inurl:& site:example[.]com

API Docs:
inurl:apidocs | inurl:api-docs | inurl:swagger | inurl:api-explorer site:"example[.]com"

LFI:
inurl:include | inurl:dir | inurl:detail= | inurl:file= | inurl:folder= | inurl:inc= | inurl:locate= | inurl:doc= | inurl:conf= inurl:& site:example
