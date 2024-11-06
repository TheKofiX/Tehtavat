## h2 Infra-as-code:
### x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva. Ei siis vaadita pitkää eikä essee-muotoista tiivistelmää.)
    Karvinen 2023: Run Salt Command Locally

    
    Karvinen 2018: Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux
    Karvinen 2006: Raportin kirjoittaminen
    Saltin asennus edellyttää nykyään (Debian 12 Bookworm) uuden pakettivaraston asentamista, mitä ei käsitellä näissä artikkelissa. Ohjeet pakettivaraston asentamiseen vinkeissä alla.
### a) Hello Vagrant! Osoita jollain komennolla, että Vagrant on asennettu (esim tulostaa vagrantin versionumeron). Jos et ole vielä asentanut niitä, raportoi myös Vagrant ja VirtualBox asennukset. (Jos Vagrant ja VirtualBox on jo asennettu, niiden asennusta ei tarvitse tehdä eikä raportoida uudelleen.)
    Virtualbox oli jo asennettuna, mutta vagrant piti vielä asentaa. 
    Sen asennus toimi kuten muutkin Windows ohjelmat, lataamalla .exe tiedoston ja ajamalla sen.
  <img src="https://i.imgur.com/5zX8hrN.png" alt="Alternate image text" width="400"/>

### b) Linux Vagrant. Tee Vagrantilla uusi Linux-virtuaalikone.
    Vagrant Linux-virtuaalikone asennettiin komennoilla    
    *$ vagrant init debian/bookworm64
     $ vagrant up*
     Joiden jälkeen alla olevan kuvan tapaisesti vagrant ssh sai yhteyden koneeseen.
     Kuvasta näkyy myös *ls_release -a* komento joka osoittaa kyseisen linux asennuksen.
                            
  <img src="https://i.imgur.com/aepesNJ.png" alt="Alternate image text" width="400"/>

### c) Kaksin kaunihimpi. Tee kahden Linux-tietokoneen verkko Vagrantilla. Osoita, että koneet voivat pingata toisiaan.
     Kuten alla olevasta kuvasta huomaa, pystymme pingaamaan toisen vagrant koneen IP-osoitteeseen.
     Olin tässä vaiheessa asentanut myös jo saltin, jonka vuoksi sen pingaus on mukana.
  <img src="https://i.imgur.com/a68avhq.png" alt="Alternate image text" width="400"/>

### d) Herra-orja verkossa. Demonstroi Salt herra-orja arkkitehtuurin toimintaa kahden Linux-koneen verkossa, jonka teit Vagrantilla. Asenna toiselle koneelle salt-master, toiselle salt-minion. Laita orjan /etc/salt/minion -tiedostoon masterin osoite. Hyväksy avain ja osoita, että herra voi komentaa orjakonetta.
      Kuten yllä olevan kohdan c) kuvasta huomaa pystyy minion kone vastaamaan master koneen pingi pyyntöön.
      Komento: sudo salt '*' test.ping

### e) Hei infrakoodi! Kokeile paikallisesti (esim 'sudo salt-call --local') infraa koodina. Kirjota sls-tiedosto, joka tekee esimerkkitiedoston /tmp/ -kansioon.
        srv/salt/hello/init.sls tiedosto pitää sisällään:
        /tmp/testi.txt:
          file.managed:
            - contents: "Testitiedosto slsn käytöstä."
        Ensimmäisessä kuvassa kyseinen sls tiedosto ajetaan enimmäisen kerran.
        Kuvasta 2.ilmenee, että testi.txt tiedosto luotiin onnistuneesti.
  <img src="https://i.imgur.com/IaY15ur.png" alt="Alternate image text" width="400"/>
      Kuva 2
  <img src="https://i.imgur.com/1NXagcG.png" alt="Alternate image text" width="400"/>
  
### f) Aja esimerkki sls-tiedostosi verkon yli orjalla.
    Alla olevan kuvan mukaisesti ajettiin sls tiedosto komennolla:
    $ sudo salt 'minion' state.apply hello
    Jonka jälkeen varmistettiin tiedoston luonti/olemassa olo komennolla:
    $ sudo salt 'minion' cmd.run 'cat /tmp/testi.txt'
  <img src="https://i.imgur.com/tjTR6SS.png" alt="Alternate image text" width="400"/>

### g) Tee sls-tiedosto, joka käyttää vähintään kahta eri tilafunktiota näistä: package, file, service, user. Tarkista eri ohjelmalla, että lopputulos on oikea. Osoita useammalla ajolla, että sls-tiedostosi on idempotentti.
  <img src="https://i.imgur.com/RVzLZx0.png" alt="Alternate image text" width="400"/>
   <img src="https://i.imgur.com/JUG7kPv.png" alt="Alternate image text" width="300"/>
   
### h) Top file. Automatisoi vähintään kahden tilan / modulin ajaminen. Esim. komento 'sudo salt "*" state.apply' tai 'sudo salt-call --local state.apply' ajaa modulit "hello" ja "apache".
  <img src="https://i.imgur.com/fvVl1vN.png" alt="Alternate image text" width="300"/>
  <img src="https://i.imgur.com/JqExShc.png" alt="Alternate image text" width="300"/>
