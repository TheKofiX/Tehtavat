x) Lue/katso/kuuntele ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva.)

        OWASP: OWASP Top 10: A01 Broken Access Control
          - Broken Access Control eli "Rikkoutunut käyttöoikeuksien hallinta"
          - Tärkeää varmistaa että käyttäjät eivät pysty toimia oikeuksien ulkopuolella.
          - Varmista että tekijöillä on vain tehtävään tarvittavat oikeudet.
          - Tärkeää pitää lokia, jossa kirjautumiset ja avatut tiedostot sisältyvät. 
          
        Karvinen 2023: Find Hidden Web Directories - Fuzz URLs with ffuf
          - Auttaa esim. löytämään piilotettuja hakemistoja.
          - Sisältää asennus ohjeet, sekä esimerkki tehtävän, tämän jälkeen aika haasteeseen.
          
        PortSwigger: Access control vulnerabilities and privilege escalation
          - Ohjeita, sekä suojaus keinoja pääsynhallinan virheiden minimoimiseen. Näitä on mm.
          - Muista vahvistaa käyttäjän identiteetti.
          - Sovitut yhteiset käytännöt.
          - Yleissääntönä kielto kaikkiin resursseihin, ellei toisin määritellä.
          
        Karvinen 2006: Raportin kirjoittaminen
          - Muista lähdeviittaukset raportteihin.
          - Pahoja mogia on sepittäminen, plagiointi sekä kuvien luvaton kopiointi.
          - Tee tekstistä helppo lukuista.
          - Ole täsmällinen sekä tee raporteista toistettavia, jotta muut oppilaat pystyvät ratkaisemaan.
          
a) Murtaudu 010-staff-only. Ks. Karvinen 2024: Hack'n Fix
    Murtautumisessa käytin tehtävään vinkkejä sekä kysyin ChatGPT:ltä neuvoa.
    Vaihe 1. Ensimmäinen kysymykseni oli, mihin voin kirjoittaa SQL injectiota varten tarvittavan SQL lauseen. Annettu teksti kenttä oli vain numeroille, eikä URL kenttäkään antanut apua. 
    Tähän kysyin vinkkiä ChatGPT:ltä. Kysymykseni oli: "I have a field thats numbers only and a website address of 127.0.0.1:5000 can either of these be used to pass sql commands." Tähän sain neuvoksi "Bypass Frontend Validation" sekä html koodi snipetin sisältäen type="text".
<img src="https://i.imgur.com/WaPt33W.png" alt="Alternate image text" width="300"/>
    
    Ymmärsin tämän jälkeen, että pystyn käyttämään Inspect Element(f12) Toimintoa muuttamaan tekstikentän tyypin "text" pohjaksi.
    Vaihe 2.Tämän jälkeen pääsin syöttämään SQL komennon  "123 UNION SELECT pin FROM pins -- ", joka antoi sivulle tekstin "Your password is 11112222333" 

<img src="https://i.imgur.com/p5PTXMt.png" alt="Alternate image text" width="300"/>
    
    Vaihe 3.Tämän pinin syötettyä sai näkyviin tehtävän vastauksen.
<img src="https://i.imgur.com/kHjPLuy.png" alt="Alternate image text" width="300"/>
  
 
b) Korjaa 010-staff-only haavoittuvuus lähdekoodista. Osoita testillä, että ratkaisusi toimii.
c) Ratkaise dirfuzt-1 artikkelista Karvinen 2023: Find Hidden Web Directories - Fuzz URLs with ffuf. Tämä auttaa 020-your-eyes-only ratkaisemisessa.
d) Murtaudu 020-your-eyes-only. Ks. Karvinen 2024: Hack'n Fix
e) Korjaa 020-your-eyes-only haavoittuvuus. Osoita testillä, että ratkaisusi toimii.
