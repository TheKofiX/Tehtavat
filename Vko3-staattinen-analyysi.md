## h3 No strings attached

### a) Strings. Lataa ezbin-challenges.zip Aja 'passtr'. Selvitä oikea salasana 'strings' avulla. Selvitä myös lippu. (Ensisijaisesti katsomatta sorsia, jos osaat.)

- En ollut ennen käyttänyt C kieltä tai esim. strings komentoa ennen, aloitin tämän takia opettelmalla ja tutkimalla kuinka se toimii.
- Tämän jälkeen aloitin tutkimaan kuinka näitä komentoja voisi käyttää salasanan saamiseen.
- Ensimmäinen kokeilemani komento oli *strings | grep -i "password"*, joka palautti sattumalta tehtävän lipun, huomasin kuitenkin että tämä ei ollut pyydetty   salasana.
<img src="https://i.imgur.com/5p6s0c9.png" alt="Alternate image text" width="400"/>

- Seuraava komento jota yritin oli *strings passtr*, joka vain hakee kaikki strings tiedot ohjelmasta.
Näiden avulla löysinkin jo salasanan.

<img src="https://i.imgur.com/tvcteaA.png" alt="Alternate image text" width="400"/>

- Lopullinen lippu.

<img src="https://i.imgur.com/FEQRO1p.png" alt="Alternate image text" width="400"/>

### b) Tee passtr.c -ohjelmasta uusi versio, jossa salasana ei näy suoraan sellaisenaan binääristä. Osoita testillä, että salasana ei näy. (Obfuskointi riittää.)

- Itselläni ei ollut ideaa kuinka lähestyisin salasanan obfuskointia.
- Ensimmäinen löytämäni neuvo oli jakaa salasana useaan eri strings osioon, jonka jälkeen for looppi yhdistäisi salasanan osat. Kokeilin kyseistä ohjelmaa, mutta sain kuitenkin seuraavan tehtävän pohjalta idean käyttää UPX ohjelmaa, joka pakkaa tiedoston, ja hajauttaa näin strings osat.
  
<img src="https://i.imgur.com/UBw900c.png" alt="Alternate image text" width="400"/>

- *strings passtr*, ei enää anna selkokielellä koko salasanaa tai lippua.
  
<img src="https://i.imgur.com/wI9eXK4.png" alt="Alternate image text" width="400"/>

- Myöskään *strings passtr | grep -i "sala"* toiminto, ei tuota oikeaa salasanaa.
  
<img src="https://i.imgur.com/DJbtuBT.png" alt="Alternate image text" width="400"/>

### c) Packd. Aja 'packd' paketista ezbin-challenges.zip. Mikä on salasana? Mikä on lippu? (Tämä tehtävä on hieman haastavampi. Kirjaa ylös kokeilemasi lähestymistavat ja keksimäsi hypoteesit. 

- Lähestyin tehtävää samalla tavalla kuin tehtävää a). Huomasin kuitenkin että tekstit olivat outoja aivan kuin ne olivat jaettu usealle riville.
- Huomasin myös paljon tekstiä, jossa luki "UPX", niin strings tiedoista, kuin myös lähdekoodin avatessa. Tämän googlettamisen jälkeen ymmärsin sen olevan pakkausohjelma.
- Kysyin tässä vaiheessa ChatGPT:ltä kuinka tämän saisi helpoiten peruttua, joka ohjasi upx:n asennukseen sekä komentoon 
 *upx -d pacckd* joka peruu tiedoston pakkauksen.
<img src="https://i.imgur.com/DjO0pb9.png" alt="Alternate image text" width="400"/>

- Kun UPX pakkaus oli saatu purettua, toimi samat komennot kuin tehtävässä a.
 
<img src="https://i.imgur.com/89svmhd.png" alt="Alternate image text" width="400"/>

- Lopullinen lippu ja salasana.

<img src="https://i.imgur.com/Cya5Kgp.png" alt="Alternate image text" width="400"/>

### Lähteet/neuvot

  ChatGPT:ltä kysyin:
  "kuinka puran upx lähdekoodi ohjelman linuxilla". Kysyin myös yleisesti kuinka strings toimintoa voi käyttää.
        
  Yleistä opiskelua strings toiminnoista:
  https://www.geeksforgeeks.org/strings-in-c/
  https://www.howtogeek.com/427805/how-to-use-the-strings-command-on-linux/
  https://phoenixnap.com/kb/grep-command-linux-unix-examples
