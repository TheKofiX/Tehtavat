## h2 Infra-as-code:
### x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva. Ei siis vaadita pitkää eikä essee-muotoista tiivistelmää.)
    Karvinen 2023: Run Salt Command Locally

    
    Karvinen 2018: Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux
    Karvinen 2006: Raportin kirjoittaminen
    Saltin asennus edellyttää nykyään (Debian 12 Bookworm) uuden pakettivaraston asentamista, mitä ei käsitellä näissä artikkelissa. Ohjeet pakettivaraston asentamiseen vinkeissä alla.
### a) Hello Vagrant! Osoita jollain komennolla, että Vagrant on asennettu (esim tulostaa vagrantin versionumeron). Jos et ole vielä asentanut niitä, raportoi myös Vagrant ja VirtualBox asennukset. (Jos Vagrant ja VirtualBox on jo asennettu, niiden asennusta ei tarvitse tehdä eikä raportoida uudelleen.)

  <img src="https://i.imgur.com/5zX8hrN.png" alt="Alternate image text" width="300"/>

### b) Linux Vagrant. Tee Vagrantilla uusi Linux-virtuaalikone.
  <img src="https://i.imgur.com/aepesNJ.png" alt="Alternate image text" width="300"/>

### c) Kaksin kaunihimpi. Tee kahden Linux-tietokoneen verkko Vagrantilla. Osoita, että koneet voivat pingata toisiaan.
  <img src="https://i.imgur.com/a68avhq.png" alt="Alternate image text" width="300"/>

### d) Herra-orja verkossa. Demonstroi Salt herra-orja arkkitehtuurin toimintaa kahden Linux-koneen verkossa, jonka teit Vagrantilla. Asenna toiselle koneelle salt-master, toiselle salt-minion. Laita orjan /etc/salt/minion -tiedostoon masterin osoite. Hyväksy avain ja osoita, että herra voi komentaa orjakonetta.
  <img src="" alt="Alternate image text" width="300"/>

### e) Hei infrakoodi! Kokeile paikallisesti (esim 'sudo salt-call --local') infraa koodina. Kirjota sls-tiedosto, joka tekee esimerkkitiedoston /tmp/ -kansioon.
  <img src="https://i.imgur.com/IaY15ur.png" alt="Alternate image text" width="300"/>
  <img src="https://i.imgur.com/1NXagcG.png" alt="Alternate image text" width="300"/>
### f) Aja esimerkki sls-tiedostosi verkon yli orjalla.
  <img src="https://i.imgur.com/tjTR6SS.png" alt="Alternate image text" width="300"/>

### g) Tee sls-tiedosto, joka käyttää vähintään kahta eri tilafunktiota näistä: package, file, service, user. Tarkista eri ohjelmalla, että lopputulos on oikea. Osoita useammalla ajolla, että sls-tiedostosi on idempotentti.
  <img src="https://i.imgur.com/RVzLZx0.png" alt="Alternate image text" width="300"/>
   <img src="https://i.imgur.com/JUG7kPv.png" alt="Alternate image text" width="300"/>
   
### h) Top file. Automatisoi vähintään kahden tilan / modulin ajaminen. Esim. komento 'sudo salt "*" state.apply' tai 'sudo salt-call --local state.apply' ajaa modulit "hello" ja "apache".
  <img src="https://i.imgur.com/fvVl1vN.png" alt="Alternate image text" width="300"/>
  <img src="https://i.imgur.com/JqExShc.png" alt="Alternate image text" width="300"/>
