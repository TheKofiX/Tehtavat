# x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva. Ei siis vaadita pitkää eikä essee-muotoista tiivistelmää.)

a) Asenna Debian 12-Bookworm virtuaalikoneeseen. (Poikkeuksellisesti tätä alakohtaa ei tarvitse raportoida, jos siinä ei ole mitään ongelmia. Mutta jos on ongelmia, sitten täsmällinen raportti, jotta voidaan ratkoa niitä yhdessä.)
  
  - Ei ongelmia asennuksessa

b) Asenna Salt (salt-minion) Linuxille (uuteen virtuaalikoneeseesi).

  -

c) Viisi tärkeintä. Näytä Linuxissa esimerkit viidestä tärkeimmästä Saltin tilafunktiosta: pkg, file, service, user, cmd. Analysoi ja selitä tulokset.
d) Idempotentti. Anna esimerkki idempotenssista. Aja 'salt-call --local' komentoja, analysoi tulokset, selitä miten idempotenssi ilmenee.
# Ajamalla komennon ensimmäisen kerran saat tulokseksi tämän. Kiinnitä huomio kohtaan (changed=1)
Changes:
----------
          htop:
              ----------
              new:
                  3.2.2-2
              old:

Summary for janne-virtualbox
------------
Succeeded: 1 (changed=1)
Failed:    0
------------
Total states run:     1
Total run time:   2.269 s

# Ajamalla komennon toisen kerran muuttuu summary seuraavan laiseksi: 
Summary for janne-virtualbox
------------
Succeeded: 1
Failed:    0
------------
Total states run:     1
Total run time:  43.600 ms
janne@janne-virtualbox:~$
e) Herra-orja. Kokeile herra-orja arkkitehtuuria niin, että herra ja orja ovat samalla koneella.
