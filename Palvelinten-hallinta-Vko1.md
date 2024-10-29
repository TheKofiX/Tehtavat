 x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva. Ei siis vaadita pitkää eikä essee-muotoista tiivistelmää.)

### a) Asenna Debian 12-Bookworm virtuaalikoneeseen. (Poikkeuksellisesti tätä alakohtaa ei tarvitse raportoida, jos siinä ei ole mitään ongelmia. Mutta jos on ongelmia, sitten täsmällinen raportti, jotta voidaan ratkoa niitä yhdessä.)
  
  - Ei ongelmia asennuksessa

### b) Asenna Salt (salt-minion) Linuxille (uuteen virtuaalikoneeseesi).

  -

### c) Viisi tärkeintä. Näytä Linuxissa esimerkit viidestä tärkeimmästä Saltin tilafunktiosta: pkg, file, service, user, cmd. Analysoi ja selitä tulokset.

### d) Idempotentti. Anna esimerkki idempotenssista. Aja 'salt-call --local' komentoja, analysoi tulokset, selitä miten idempotenssi ilmenee.

Alla olevista kuvista huomaa kun komento "sudo salt '*' state.apply install_htop" Ajetaan ensimmäisen kerran tapahtuu muutos, mutta kun se ajetaan uudelleen ei muutosta tapahdu.

<img src="https://i.imgur.com/2i7SmC9.png" alt="Alternate image text" width="300"/>
<img src="https://i.imgur.com/u5CdbTp.png" alt="Alternate image text" width="300"/>

### e) Herra-orja. Kokeile herra-orja arkkitehtuuria niin, että herra ja orja ovat samalla koneella.
