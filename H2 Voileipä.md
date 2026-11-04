# H2 Voileipä

## x) Lue ja tiivistä

Karvinen 2026a: Sudo without password

-Miten  hyväksyä SUDO ilman salasanaa?

-Luo uusi käyttäjä

<img width="227" height="54" alt="image" src="https://github.com/user-attachments/assets/92e4885b-248d-480a-bd73-35f88929502c" />

Kuva 1 (Karvinen 2026a)

-Rikkinäinnen Sudo vakuutus: avaa uusi ikkuna ssh kohde koneella

-Jos sudo menee rikki sen voi mahdollisesti korjata seuraavalla komennolla
<img width="343" height="28" alt="image" src="https://github.com/user-attachments/assets/f466147d-94ea-4334-a6c9-25e2fc5a6a6d" />


-Uusi sudoaajien sääntö: sääntö, joka mahdollistaa sudoless käyttäjien käyttää sudoa ilman salasanaa 

<img width="319" height="36" alt="image" src="https://github.com/user-attachments/assets/ad3f11c5-f7d0-400c-af70-06cc2e10dcea" />

Kuva 3.

<img width="266" height="34" alt="image" src="https://github.com/user-attachments/assets/cae06ced-7b4e-4fc6-8bf9-b3d28753c9c6" />

Kuva 4.


-Uudet ryhmät toimivat vasta kirjauduttua ulos koneelta ja takaisin


Munroe 2006: xkcd 149: Sandwitch

-Sivusto kertookin webkomiikkaa romanssista, sarkasmista, matikasta ja kielestä
-Sandwitch vitsi kertoo sudo komennosta, ihminen ei tee voileipää pyydettäessä, sudo tekee


Karvinen 2026: Passwordless Sudo with Ansible

- Uusi käyttäjä sudottomaan ryhmään
  
- Edellytyksenä on toimiva Hello Ansible ja sudo without password

- Pitäisi saada toimimaan niin, että ei vaadi sudo salasanaa
  
- Kun saa toimimaan manuaalisesti, voi kopioida muihin tiedostoihin
  
- Mihin kaikkialle se tulee kopioida ja tuleeko jo tässä tehtävässä?


## a) Sudoless password


Tarkistin ensin tree -komennolla muistin virkistykseksi, miltä hakemisto tällä hetkellä näyttää. Sen jälkeen ajoin ensimmäisen komennon roosa@roosavirtualboxilla. Komento oli siis tuo

sudo adduser antero

Muistaakseni noihin name, number yms. kohtiin ei tarvi näissä harjoituksissa mitään kirjoittaa, joten menin enterillä eteenpäin. sit ajoin vielä komennot 

sudo groupadd sudoless

&

sudo adduser antero sudoless

Sitten ajoin toisella terminaalilla roosa@roosavirtualboxissa komennnon sudo -i. Ja siirryin takaisin toiseen terminaaliin. Seuraavaksi avasin tekstieditorin komennolla sudo visudo /etc/sudoers.d/sudoless. Kirjoitin sinne säännön %sudoless ALL = (ALL) NOPASSWD: ALL

<img width="314" height="35" alt="image" src="https://github.com/user-attachments/assets/b5822f55-49aa-4d23-9780-0cbebd055932" />

Tein sen jälkeen testaukset. Luulin, että kun kirjadun anterosta ulos sen ei pidä kysyä salasanaa, mutta se saattoikin tarkoittaa sitä, että kun laitan komennon anterolla, se ei kysy salasanaa.


## b) Sudo without password

<img width="236" height="60" alt="image" src="https://github.com/user-attachments/assets/48b5fc7e-8925-4550-8aca-93d56bf42717" />

Lisäsin site.yml sisältöä.




## Lähteet

Karvinen T 2026a. Sudo without password. Haettu osoitteesta: https://terokarvinen.com/passwordless-sudo/ Luettu: 3.11.2026


Munroe 2026. Sandwitch. Haettu osoitteesta: https://xkcd.com/149/ Luettu 3.11.2026


Karvinen T 2026b. Passwordless Sudo with Ansible. Haettu  osoitteesta: https://terokarvinen.com/passwordless-sudo-with-ansible/ Luettu 3.11.2026

