# Sauvegarde DNS clairstart.com — avant bascule vers GitHub Pages
# Prise le 2026-08-12 depuis IONOS + DNS public (8.8.8.8)

## Enregistrements que IONOS va DESACTIVER (a re-creer apres la bascule)
NS    notify           ns3.lovable.cloud
NS    notify           ns4.lovable.cloud
TXT   _dmarc           "v=DMARC1; p=none; pct=100; rua=mailto:dmarcreports@lovable.dev"
TXT   _lovable-email   "lovable_email_verify=9ec4e413162f906acffde53c419b98d7c6eaa6e220d3b462af8af48d915fd147"

## Autres enregistrements Lovable (non listes comme desactives)
TXT   _lovable         "lovable_verify=bf617f692d2d5519612b0521bd6bb60142f53b64f1309b2619d9e48484e503d4"
TXT   _lovable.www     "lovable_verify=e490dc781155505848105b70f8a179639cff44099fcf95935568ec73027827cd"

## Email IONOS — NE PAS TOUCHER
MX    @                mx00.ionos.fr (10) / mx01.ionos.fr (10)
TXT   @                "v=spf1 include:_spf-eu.ionos.com ~all"
CNAME s1-ionos._domainkey  s1.dkim.ionos.com
CNAME s2-ionos._domainkey  s2.dkim.ionos.com
CNAME autodiscover     adsredir.ionos.info
CNAME _domainconnect   _domainconnect.ionos.com

## Avant / apres
A @   185.158.133.1 (parking IONOS)  ->  185.199.108.153 (GitHub Pages)
A www 185.158.133.1                 ->  185.199.108.153 (mis a jour par le meme formulaire)
