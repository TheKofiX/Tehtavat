### a) Hello Vagrant! Osoita jollain komennolla, että Vagrant on asennettu (esim tulostaa vagrantin versionumeron). Jos et ole vielä asentanut niitä, raportoi myös Vagrant ja VirtualBox asennukset. (Jos Vagrant ja VirtualBox on jo asennettu, niiden asennusta ei tarvitse tehdä eikä raportoida uudelleen.)
  <img src="blob:https://imgur.com/171d7e8a-e0df-4314-b6e8-d604413cd135" alt="Alternate image text" width="300"/>

### b) Linux Vagrant. Tee Vagrantilla uusi Linux-virtuaalikone.
  <img src="" alt="Alternate image text" width="300"/>

### c) Kaksin kaunihimpi. Tee kahden Linux-tietokoneen verkko Vagrantilla. Osoita, että koneet voivat pingata toisiaan.
  <img src="" alt="Alternate image text" width="300"/>

### d) Herra-orja verkossa. Demonstroi Salt herra-orja arkkitehtuurin toimintaa kahden Linux-koneen verkossa, jonka teit Vagrantilla. Asenna toiselle koneelle salt-master, toiselle salt-minion. Laita orjan /etc/salt/minion -tiedostoon masterin osoite. Hyväksy avain ja osoita, että herra voi komentaa orjakonetta.
  <img src="" alt="Alternate image text" width="300"/>

### e) Hei infrakoodi! Kokeile paikallisesti (esim 'sudo salt-call --local') infraa koodina. Kirjota sls-tiedosto, joka tekee esimerkkitiedoston /tmp/ -kansioon.
  <img src="" alt="Alternate image text" width="300"/>

### f) Aja esimerkki sls-tiedostosi verkon yli orjalla.
  <img src="" alt="Alternate image text" width="300"/>

### g) Tee sls-tiedosto, joka käyttää vähintään kahta eri tilafunktiota näistä: package, file, service, user. Tarkista eri ohjelmalla, että lopputulos on oikea. Osoita useammalla ajolla, että sls-tiedostosi on idempotentti.
  <img src="" alt="Alternate image text" width="300"/>

### h) Top file. Automatisoi vähintään kahden tilan / modulin ajaminen. Esim. komento 'sudo salt "*" state.apply' tai 'sudo salt-call --local state.apply' ajaa modulit "hello" ja "apache".
  <img src="" alt="Alternate image text" width="300"/>

### i) Vapaaehtoinen, haastavahko tässä vaiheessa: Asenna ja konfiguroi Apache. Sen tulee näyttää palvelimen etusivulla weppisivua. Weppisivun tulee olla muokattavissa käyttäjän oikeuksin, ilman sudoa.
