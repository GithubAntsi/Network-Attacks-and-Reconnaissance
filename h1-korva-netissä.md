# h1 Korva netissä

    x) Spektrini. Piirrä oma sähkömagneettinen spektri. Eli jana, jossa taajuus kasvaa. Ja 3-10 itseäsi kiinnostavaa sovellusta. Saavat olla aivan tavanomaisia. Merkitse nuolilla, mihin suuntaa kasvavat: aallonpituus, antennin koko, läpäisevyys, kyky siirtää tietoa. Tämä alakohta ei edellytä testejä tietokoneella.

## Vastaus tehtävään X
- Alhaalla oma piirtämä spektri, rehellisesti ihan kauheaa katsottavaa mutta en nyt saanut oikeastaan parempaa läppärin trackpädillä ::)
- lähde joka auttoi vähän spektrin ja radio aaltojen ymmärtämisessä: https://fi.wikipedia.org/wiki/S%C3%A4hk%C3%B6magneettinen_spektri

<img width="943" height="563" alt="scuffed-spektri" src="https://github.com/user-attachments/assets/c596077b-7083-4d2b-88d2-a2d41045450a" />

    a) WebSDR. Etäkäytä WebSDR-ohjelmaradiota, joka on kaukana sinusta ja kuuntele radioliikennettä. Radioliikenne tulee siepata niin, että radiovastaanotin on joko eri maassa tai vähintään 400 km paikasta, jossa teet tätä tehtävää. Käytä esimerkkinä julkista, suurelle yleisölle tarkoitettua viestiä, esimerkiksi yleisradiolähetystä. Kerro löytämäsi taajuus, aallonpituus ja modulaatio. Kuvaile askeleet ja ota ruutukaappaus. (Tehtävässä ei saa ilmaista sellaisen viestin sisältöä tai olemassaoloa, joka ei ole tarkoitettu julkiseksi. Voit sen sijaan kuvailla, miten sait julkisen radiolähetyksen kuulumaan kaiuttimistasi. Julkisten, esimerkiksi yleisradiolähetysten sisältöä saa tietysti kuvailla.)

## Vastaus tehtävään A
- WebSDR sivun kautta löysin radio lähettimen jota ylläpidetään washington DC alueella mutta ei ole ekluusivisesti amerikkalaisa lähetyksiä. http://na5b.com:8901/
- Aallon pituus laskuisaa käytin netissä toimivaa laskinta -> https://www.omnicalculator.com/physics/wavelength

- Kanavan tiedot jota kuuntelin -> Taajuus: 730 kHz, Aallonpituus 410,675 m ≈ 411 m, Modulaatio oli AM. (Taajuusalue joka oli päällä oli MW-160) Kanava jota kuuntelin soitti musiikkia sillä hetkellä ja vaikutti siltä että kanava soittaa pelkästään musiikkia (mainoksia välillä), radio lähetys kuitenkin on alkuperäisin alexandria egypti.

<img width="945" height="591" alt="image" src="https://github.com/user-attachments/assets/710e667d-3179-41a1-ab4d-1d778e762abe" />

    b) Moduwhat? Kuuntele kanavaa, joka käyttää eri modulaatiota (AM, FM...) kuin edellisessä kohdassa käyttämäsi kanava.

## Vastaus tehtävään B  
- Seuraava kanava jota kuuntelin oli samalla sivulla mutta eri asetuksilla toimiva. Taajuus: 3838 kHz, Aallonpituus 78,1116 ≈ 78 m, Modulaatio oli LSB (Taajuusalue oli 80m) kanava kuulosti joltain radio puhe showilta missä on kaksi juontajaa ja  keskustelevat ihmisten kanssa ketkä soittavat radio kanavaan tai juttelevat keskenään.

<img width="946" height="704" alt="image" src="https://github.com/user-attachments/assets/b185bb39-b8f5-488b-b886-7531c7ccdac7" />
  
    c) ADS-B. Etsi jokin sinua kiinnnostava lentokone ADS-B Exchange -palvelusta. Kuvaile konetta ja sen lentoa. Selitä, miten tiedot on saatu.

## Vastaus tehtävään C
- Callsign JAL934 (hex ID: 862D94), Airline: Japan Airlines
- Type: B763 (BOEING 767-300)
- Lentokone kooltaan ei ole suurin kone, itse asiassa suomessa on suurempia lentokoneita kuten airbus mallin koneet. Suurin syy itse asiassa valintaan oli se että olen itse ollut samanlaisessa koneessa kun lensin japanin sisällä nagoyasta - tokioon.
- Reitti jonka näin ADS-B exchange sivulla klo 15:19 24.10.2026 oli japanin sisäinen lento, tokiosta - okinawaan ja sitten takaisin okinawasta - tokioon.
- Tietojen saanti tapa ADS-B Exchange sivulle on itse asiassa kiinnostava tapa, ADS-B Exchange sivun about osiosta 
https://www.adsbexchange.com/about/
voit osallistua itse olemaan "Feeder" eli autat vastaanottamaan lähi lentokoneista lähetettäviä sijaintia, korkeus, tunnistetiedot ja muuta dataa ja välität tiedot ADS-B exchange sivulle, jotta sivulla saadaan tarkka sijanti kartta suurimmasta osasta ilmassa olevista koneista.

## En tehnyt
    d) Vapaaehtoinen Atalaya. Asenna F-Droid ja sillä Atalaya. Käytä ohjelmaa ja selitä tulokset.
    e) Vapaaehtoinen WifiAnalyzer. Asenna F-Droid ja sillä WifiAnalyzer. Käytä ohjelmaa ja selitä tulokset.
    f) Vapaaehtoinen GPSTest. Asenna F-Droid ja sillä GPSTest. Käytä ohjelmaa ja selitä tulokset.
