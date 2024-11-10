## h3 No strings attached

### a) Strings. Lataa ezbin-challenges.zip Aja 'passtr'. Selvitä oikea salasana 'strings' avulla. Selvitä myös lippu. (Ensisijaisesti katsomatta sorsia, jos osaat.)

      - En ollut ennen käyttänyt C kieltä tai esim. strings komentoa ennen, aloitin tämän takia opettelmalla ja tutkimalla kuinka se toimii.
      - Tämän jälkeen aloitin tutkimaan kuinka näitä komentoja voisi käyttää salasanan saamiseen.
      - Ensimmäinen kokeilemani komento oli strings | grep -i "password", joka palautti sattumalta tehtävän lipun, huomasin kuitenkin että tämä ei ollut pyydetty   salasana.
<img src="https://i.imgur.com/5p6s0c9.png" alt="Alternate image text" width="400"/>

Seuraava komento jota yritin oli strings passtr, joka vain hakee kaikki strings tiedot ohjelmasta.
Näiden avulla löysinkin jo salasanan.
<img src="https://i.imgur.com/tvcteaA.png" alt="Alternate image text" width="400"/>

Lopullinen lippu.
<img src="https://i.imgur.com/FEQRO1p.png" alt="Alternate image text" width="400"/>

### b) Tee passtr.c -ohjelmasta uusi versio, jossa salasana ei näy suoraan sellaisenaan binääristä. Osoita testillä, että salasana ei näy. (Obfuskointi riittää.)

- Itselläni ei ollut ideaa kuinka lähestyisin salasanan obfuskointia.
- Ensimmäinen löytämäni neuvo oli tehdä for looppi joka yhdistää salasanan yhtenäiseksi, useasta eri stringistä.
- Kokeilin kyseistä ohjelmaa, mutta päädyin kuitenkin seuraavan tehtävän pohjalta käyttämään UPX ohjelmaa, joka pakkaa tiedoston, ja hajauttaa näin strings osat.
<img src="https://i.imgur.com/UBw900c.png" alt="Alternate image text" width="400"/>
  strings passtr, ei enää anna selkokielellä koko salasanaa tai lippua.
<img src="https://i.imgur.com/wI9eXK4.png" alt="Alternate image text" width="400"/>
  - Myöskään strings grep toiminto, ei tuota oikeaa salasanaa.
<img src="https://i.imgur.com/DJbtuBT.png" alt="Alternate image text" width="400"/>

### c) Packd. Aja 'packd' paketista ezbin-challenges.zip. Mikä on salasana? Mikä on lippu? (Tämä tehtävä on hieman haastavampi. Kirjaa ylös kokeilemasi lähestymistavat ja keksimäsi hypoteesit. 

    Lähestyin tehtävää samalla tavalla kuin tehtävää a). Huomasin kuitenkin että tekstit olivat outoja aivan kuin ne olivat jaettu usealle riville.
    - Huomasin myös paljon tekstiä UPX, jonka googlettamisen jälkeen ymmärsin sen olevan pakkausohjelma.
    - Kysyin tässä vaiheessa ChatGPT:ltä kuinka tämän saisi helpoiten purettua, joka ohjasi upx:n asennukseen sekä komentoon 
     -*upx -d pacckd* joka peruu tiedoston pakkauksen.
<img src="https://i.imgur.com/DjO0pb9.png" alt="Alternate image text" width="400"/>
<img src="https://i.imgur.com/89svmhd.png" alt="Alternate image text" width="400"/>
<img src="https://i.imgur.com/Cya5Kgp.png" alt="Alternate image text" width="400"/>
