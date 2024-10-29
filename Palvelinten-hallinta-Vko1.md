### x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva. Ei siis vaadita pitkää eikä essee-muotoista tiivistelmää.)

      Raportin kirjoitus:
      - Raportin avulla tulee voida toistaa kokeilu samanlaisessa ympäristössä.
      - Älä sepitä, plagioi tai käytä kuvia luvatta.
      - Muista lähteet, sekä ota huomioon hyvä luettavuus.

      Salt komennot:
      - Saltin avullla hallitaan monia koneita paikallisesti tai verkon yli.
      - Tärkeimmät toiminnot on: pkg,file,service,user ja cmd

      Salt quickstart: 
      - Käydään läpi yleisiä komentoja ja tietoa masterin sekä minionin välillä.
      
### a) Asenna Debian 12-Bookworm virtuaalikoneeseen. (Poikkeuksellisesti tätä alakohtaa ei tarvitse raportoida, jos siinä ei ole mitään ongelmia. Mutta jos on ongelmia, sitten täsmällinen raportti, jotta voidaan ratkoa niitä yhdessä.)
  
  - Ei ongelmia asennuksessa

### b) Asenna Salt (salt-minion) Linuxille (uuteen virtuaalikoneeseesi).

 - Alla olevista kuvista näkyy salt-minionin asennus komentoja sekä avaimen hyväksyminen.
   
<img src="https://i.imgur.com/eIQhszg.png" alt="Alternate image text" width="300"/>
<img src="https://i.imgur.com/IzKOUb3.png" alt="Alternate image text" width="300"/>
<img src="https://i.imgur.com/dxIIoM8.png" alt="Alternate image text" width="300"/>

### c) Viisi tärkeintä. pkg, file, service, user, cmd. Analysoi ja selitä tulokset.
      -pkg mahdollistaa pakettien asentamisen, päivittämisen ja poistamisen. Esimerkki: (Varmistaa Vim asennuksen)
      vim:
      pkg.installed
      
      - file hallinnoi tiedostoja, sekä kansioita. Esimerkki: (Luo tiedoston)
       /tmp/testfile.txt:
       file.managed
       
      -Service mahdollistaa palveluiden käynnistämisen, pysäyttämisen ja niiden uudelleenkäynnistyksen. (Esimerkki varmistaa että ohjelma on käynnissä)
      apache2:
      service.running
      
      -user Hallinnoi käyttäjätilejä. Se mahdollistaa käyttäjien luonnin, poiston sekä muokkaamisen.
      
      -cmd suorittaa komentokehotetoimintoja. Esimerkki: suorittaa päivityksen
      update-system:
       cmd.run:
       name: apt-get update && apt-get upgrade -y

### d) Idempotentti. Anna esimerkki idempotenssista. Analysoi tulokset, selitä miten idempotenssi ilmenee.

Alla olevista kuvista huomaa kun komento "sudo salt '*' state.apply install_htop" Ajetaan ensimmäisen kerran tapahtuu muutos, mutta kun se ajetaan uudelleen ei muutosta tapahdu.

<img src="https://i.imgur.com/2i7SmC9.png" alt="Alternate image text" width="300"/>
<img src="https://i.imgur.com/u5CdbTp.png" alt="Alternate image text" width="300"/>

### e) Herra-orja. Kokeile herra-orja arkkitehtuuria niin, että herra ja orja ovat samalla koneella.

<img src="https://i.imgur.com/Y0P9JHl.png" alt="Alternate image text" width="300"/>
