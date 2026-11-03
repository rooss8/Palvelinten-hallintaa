# H2 Voileipä

## x) Lue ja tiivistä

## Karvinen 2026a: Sudo without password

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


## Munroe 2006: xkcd 149: Sandwitch

-Sivusto kertookin webkomiikkaa romanssista, sarkasmista, matikasta ja kielestä
-Sandwitch vitsi kertoo sudo komennosta, ihminen ei tee voileipää, sudo tekee


## Karvinen 2026: Passwordless Sudo with Ansible

Ansiblen sisäänrakennettu dokumentaatio ansible-doc -kommennolla.
Kustakin vain
Johdantokappale (Usein MODULE alla, päättyy OPTIONS alkuun)
Nimetyt optiot selityksineen
Esimerkeistä (EXAMPLES) jokin helppo ja keskeinen esimerkki
'ansible-doc copy': content, dest, src; owner, group, mode;
'ansible-doc apt': name, state, update_cache.
'ansible-doc file': path, recurse, src, state. owner, group, mode;
'ansible-doc user': name; create_home, comment, groups, shell, state, system.
'ansible-doc authorized_key': user, key.

