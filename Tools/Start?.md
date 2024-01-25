#Extensions
Wappalyzer, whatruns, editThisCookie, xnlReveal, FoxyProxy
Shodan, dot git, open all urls, whatsweb, webanalyze

#Recon
look for :
/crossdomain.xml
/clientaccesspolicy.xml
/sitemap.xml
/.well-known/

wafW00f
whatwaf

githound
git-search

gau, waybackurls, waymore,hakrawler
gf-patterns
paramspider
dalfox(XSS), bfac(backup),blc(broken link hijacking)
js files(subjs, linkfinder)
secretfinder(Secrets in js file)
Js analysis(Jsparser, jsfscan,jsscanner,jshole)
CORS(CORScanner, corsy)
bbot, arjun, ffuf, webcopilot,

Regex for parameters:
grep -Eo '(var|let) ([A-Za-z0-9_]+){2,}' -R js-files | cut -d' ' -f2

