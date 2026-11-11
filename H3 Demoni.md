# H3 Demoni

## x)Lue ja tiivistä.
## Apache installed with Ansible - quick notes

- Tekstissä opetetaan asentamaan Apache 2 -verkkopalvelin automaattisesti. Palvelin tarjoaa verkkosivuston osoitteessa http://localhost. Sivuja voi muokata tavallisena käyttäjänä – ilman root- tai sudo-oikeuksia.
- Asenna taustaprosessi, muokkaa asetustiedostoja ja käynnistä prosessi.
- Asetustiedostoihin tehdyt muutokset tulevat voimaan vasta, kun taustaprosessi käynnistetään uudelleen.


## Handlers: running operations on change

- Saatat esimerkiksi haluta käynnistää palvelun uudelleen, jos jokin tehtävä päivittää kyseisen palvelun asetukset – mutta et silloin, jos asetukset pysyvät ennallaan. Ansible käyttää tähän tarkoitukseen niin sanottuja käsittelijöitä (handlers). Käsittelijät ovat tehtäviä, jotka suoritetaan ainoastaan, kun tulee muutos.
- Tehtävät voivat `notify`-avainsanan avulla ohjeistaa yhden tai useamman käsittelijän (handler) suoritettavaksi. `notify`-avainsanaa voidaan käyttää tehtävän yhteydessä, ja se ottaa vastaan ​​luettelon käsittelijöiden nimistä; näille käsittelijöille lähetetään ilmoitus, jos tehtävä aiheuttaa muutoksen. Vaihtoehtoisesti voidaan antaa myös merkkijono, joka sisältää yhden käsittelijän nimen.
- Sivulla on esimerkki: Käynnistä memcached uudelleen, Käynnistä apache uudelleen. Käsittelijät suoritetaan siinä järjestyksessä, jossa ne on määritelty käsittelijät-osiossa, ei siinä järjestyksessä, jossa ne on lueteltu notify-lausekkeessa. Saman käsittelijän ilmoittaminen useita kertoja johtaa siihen, että käsittelijä suoritetaan vain kerran riippumatta siitä, kuinka monta tehtävää ilmoittaa siitä. Esimerkiksi, jos useat tehtävät päivittävät määritystiedoston ja ilmoittavat käsittelijälle Apachen uudelleenkäynnistyksestä, Ansible palauttaa Apachen vain kerran tarpeettomien uudelleenkäynnistysten välttämiseksi.


## a) Apassi. Asenna Apache 2 käsin. Weppisivun tulee näkyä palvelimen etusivulla. Sivun tulee olla tavallisen käyttäjän muokattavissa, ilman root- tai sudo-oikeuksia.


## b) Moottorix. Asenna Nginx käsin. Weppisivun tulee näkyä palvelimen etusivulla. Sivun tulee olla tavallisen käyttäjän muokattavissa, ilman root- tai sudo-oikeuksia. (Muista sammuttaa Apache ensin.)


## c) Automoottorix. Automatisoi Nginx asennus Ansiblella. Ylläpitäjän osuus Ansiblella riittää, itse HTML-weppisivut voi tehdä käsin.


## d) Vapaaehtoinen bonus: Osiris-T. Osiris-T asentaa Wazuhin ja tarvittavat virtuaalikoneet. Voit lähettää vihamielistä verkkoliikennettä (tcpreplay), siepata sen (suricata) ja saat tulokset suoraan dashboardille (wazuh). Enemmän alpha kuin se kreikkalainen kirjain. Mutta Oskari, Nico ja Arttu ilahtuvat, jos kokeilet. Häkämies, Saario, Mukkula 2026: Osiris-T. Häkämies etal 2026: How to Install.


# Lähteet
