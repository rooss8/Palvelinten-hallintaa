
H1 Hei ansiblen maailma
a) Latasin debianin aiemmalla kurssilla. H0 Oikeasti netissä.docx
b) Tein tehtävät Linuxilla virtuaaliboxissa.
 <img width="748" height="419" alt="image" src="https://github.com/user-attachments/assets/616e3a5c-508b-49ab-80cb-3725da804acb" />
SSH toimii niin kuin pitääkin localhostilla.


c)
 <img width="709" height="270" alt="image" src="https://github.com/user-attachments/assets/0554ffa4-48b4-44d5-9de4-793916e11990" />
Tein SSH avaimen. SSH avain löytyy, kun sitä kutsuu.

d) Tein hei maailman ansiblella.
 


 
Jossain vaiheessa eksyin tehtävässä väärään kohtaan ja tuli sen vuoksi error. Sen myötä lisäsin myöhemmässä kohdassa olevan defaultsin jo vähän edeltä. Lisäsin
[defaults]
inventory = hosts.ini
, jotta ei tarvitse joka kerta ansibleen kirjoittaa "-i hosts.ini" (TeroKarvinen.com s.a.).
Löysin oikean kohdan ja pääsin jatkamaan siitä.
 
 
Siinä on tehtävän lopputulos.



Lähteet:
TeroKarvinen.com s.a. Hello Ansible. Luettavissa: https://terokarvinen.com/hello-ansible/ Luettu: 27.10.2026.
TeroKarvinen.com s.a. SSH public key - Login without password. Luettavissa: https://terokarvinen.com/ssh-public-key-login-without-password/#automatic-login-with-ssh-public-key Luettu: 27.10.2026.



