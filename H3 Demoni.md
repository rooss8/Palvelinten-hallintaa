# H3 Demoni

## x)Lue ja tiivistä.
## Apache installed with Ansible - quick notes

-Tekstissä opetetaan asentamaan Apache 2 -verkkopalvelin automaattisesti. Palvelin tarjoaa verkkosivuston osoitteessa http://localhost.Sivuja voi muokata tavallisena käyttäjänä – ilman root- tai sudo-oikeuksia.
-Asenna taustaprosessi, muokkaa asetustiedostoja ja käynnistä prosessi.
-Asetustiedostoihin tehdyt muutokset tulevat voimaan vasta, kun taustaprosessi käynnistetään uudelleen.


## Handlers: running operations on change


## a) Apassi. Asenna Apache 2 käsin. Weppisivun tulee näkyä palvelimen etusivulla. Sivun tulee olla tavallisen käyttäjän muokattavissa, ilman root- tai sudo-oikeuksia.


## b) Moottorix. Asenna Nginx käsin. Weppisivun tulee näkyä palvelimen etusivulla. Sivun tulee olla tavallisen käyttäjän muokattavissa, ilman root- tai sudo-oikeuksia. (Muista sammuttaa Apache ensin.)


## c) Automoottorix. Automatisoi Nginx asennus Ansiblella. Ylläpitäjän osuus Ansiblella riittää, itse HTML-weppisivut voi tehdä käsin.


## d) Vapaaehtoinen bonus: Osiris-T. Osiris-T asentaa Wazuhin ja tarvittavat virtuaalikoneet. Voit lähettää vihamielistä verkkoliikennettä (tcpreplay), siepata sen (suricata) ja saat tulokset suoraan dashboardille (wazuh). Enemmän alpha kuin se kreikkalainen kirjain. Mutta Oskari, Nico ja Arttu ilahtuvat, jos kokeilet. Häkämies, Saario, Mukkula 2026: Osiris-T. Häkämies etal 2026: How to Install.


# Lähteet
