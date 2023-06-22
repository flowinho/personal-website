---
layout: post
title: tbd
---

notes

- brauchst github account (pro wenn seite public aber repo private sein soll)
- brauchst domain
- repo anlegen
- braucht inhalt (readme reicht)

ablauf

- content anlegen (readme reicht)
- github pages aktivieren (zB. main branch)
- custom domain konfigurieren
- in gandi:

https://docs.github.com/de/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain

A

185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153

AAAA

2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153


prüfen:


dig sagneinzudadjokes.de +noall +answer -t A                                                                                                           ─╯

; <<>> DiG 9.10.6 <<>> sagneinzudadjokes.de +noall +answer -t A
;; global options: +cmd
sagneinzudadjokes.de.	10800	IN	A	185.199.110.153
sagneinzudadjokes.de.	10800	IN	A	185.199.108.153
sagneinzudadjokes.de.	10800	IN	A	185.199.111.153
sagneinzudadjokes.de.	10800	IN	A	185.199.109.153

╰─ dig sagneinzudadjokes.de +noall +answer -t AAAA                                                                                                        ─╯

; <<>> DiG 9.10.6 <<>> sagneinzudadjokes.de +noall +answer -t AAAA
;; global options: +cmd
sagneinzudadjokes.de.	10800	IN	AAAA	2606:50c0:8000::153
sagneinzudadjokes.de.	10800	IN	AAAA	2606:50c0:8001::153
sagneinzudadjokes.de.	10800	IN	AAAA	2606:50c0:8003::153
sagneinzudadjokes.de.	10800	IN	AAAA	2606:50c0:8002::153


─ dig www.sagneinzudadjokes.de +nostats +nocomments +nocmd                                                                                               ─╯

; <<>> DiG 9.10.6 <<>> www.sagneinzudadjokes.de +nostats +nocomments +nocmd
;; global options: +cmd
;www.sagneinzudadjokes.de.	IN	A
www.sagneinzudadjokes.de. 10800	IN	CNAME	flowinho.github.io.
flowinho.github.io.	3600	IN	A	185.199.111.153
flowinho.github.io.	3600	IN	A	185.199.109.153
flowinho.github.io.	3600	IN	A	185.199.108.153
flowinho.github.io.	3600	IN	A	185.199.110.1


GitHub Pages aktivieren
custom domain eintragen wenn überprüfung erfolgreich ist.
Warten bis das Zertifikat ausgestellt wurde.
"Enforce https" aktivieren.

Profit.
