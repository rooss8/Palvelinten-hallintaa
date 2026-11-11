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

- Aloitin debianissa terminalissa laittaamalla komennon sudo apt-get install apache2. Luki, että on jo apache 2 uusin versio on ladattu. Avasin sitten tiedoston tekstieditorissa komennolla sudoedit /etc/apache2/... ja muokkasin sitä. Sit laitoin komennon sudo systemctl restart apache2

- <img width="366" height="221" alt="image" src="https://github.com/user-attachments/assets/2122805f-6d7d-46ed-a83f-ccd6b0e60239" />

Seuraavaksi handler:

<img width="265" height="70" alt="image" src="https://github.com/user-attachments/assets/c2dfc620-ff3f-4368-9012-1aeead65e03c" />


<img width="290" height="83" alt="image" src="https://github.com/user-attachments/assets/8a58b124-f343-4df5-8004-5727b35ec9e6" />


## b) Moottorix. Asenna Nginx käsin. Weppisivun tulee näkyä palvelimen etusivulla. Sivun tulee olla tavallisen käyttäjän muokattavissa, ilman root- tai sudo-oikeuksia. (Muista sammuttaa Apache ensin.)

- Sammutin apachen komennoilla sudo systemctl stop apache2 ja sudo systemctl disable apache2
- Asennuksess oli jotain ongelmaa
  

# Lähteet

Karvinen 2026. Apache installed with Ansible - quick notes. Haettu osoitteesta: https://terokarvinen.com/apache-ansible/

