# h3 Aaltoja harjaamassa

## Vastaus tehtävään X

Hubacek

- URH spektri analysoinnilla etsitään taajuus jolla kaukosäädin lähettää, jonka jälkeen lähetys nauhoitetaan ja tallennetaan.

- Modulaatioksi valittiin "ASK" ja "Autodetect parameters" avulla saadan arvioitua signaalin asetukset. -> modulaatio selityksiä (https://en.wikipedia.org/wiki/On%E2%80%93off_keying)

- Automaattinen tunnistus ei ole aina täysin tarkka, antaa vain apuja ja suunnan joten tarkistetaan käsin parametrit jotta voidaan saada tarkkoja loppu tuloksia.

Cornelius

- Tutkitaan langattoman sää aseman lämpötila ja kosteustietoja.

- rtl_433 softa tunnistaa laitteen nimellä Nexus-TH ja purkaa mitatut arvot automaattisesti.

- URH avulla tutkitaan sama signaali käsin. Lähetin kytkee radiosignaalin päälle ja pois joka viittaa OOK-modulaatiota. -> https://en.wikipedia.org/wiki/On%E2%80%93off_keying

Vapaaehtoinen Lohner

En Vastannut

     x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva.)
    Hubacek 2019: Universal Radio Hacker SDR Tutorial on 433 MHz radio plugs (Video, alkaen 3:19 ja päättyen 7:40. Yhteensä noin 4 min.)
    Cornelius 2022: Decode 433.92 MHz weather station data
    Vapaaehtoinen, vaikeahko: Lohner 2019: Decoding ASK/OOK_PPM Signals with URH and rtl_433


## Vastaus tehtävään b

Komennolla **"rtl_433 -V"** tulostaa rtl_433 versio tiedot.
<img width="608" height="67" alt="image" src="https://github.com/user-attachments/assets/919439d7-9e4d-40cd-9d2f-e80de4cddcc3" />

rtl_433 github sivun https://github.com/merbanan/rtl_433 ensimmäinen komento modifier on **"-V"**
<img width="326" height="44" alt="image" src="https://github.com/user-attachments/assets/e682e64a-bfad-4414-900b-03afa4a5567d" />


    b) rtl_433. Asenna rtl_433 automaattista analyysia varten. Kokeile, että voit ajaa sitä. './rtl_433' vastaa "rtl_433 version 25.02 branch..."

## Vastaus tehtävään c

https://github.com/merbanan/rtl_433 <- sivulta löytyy komentoja rtl_433:n käyttöön. (MAN sivut ovat myös olemassa.)

**"wget https://terokarvinen.com/verkkoon-tunkeutuminen-ja-tiedustelu/samples/Converted_433.92M_2000k.cs8"** komennon avulla saat ladattua rtl_433 tiedoston suoraan terokarvinen.com sivulta (MAN sivut myös olemassa "wget" komennolle. / Käytin Kali distroa, tässä Kalin wget sivu https://www.kali.org/tools/wget/)

<img width="694" height="350" alt="image" src="https://github.com/user-attachments/assets/e8ddcc0e-edae-42f1-84b2-79fc0c3015ea" />

**"rtl_433 -r Converted_433.92M_2000k.cs8 -F json"** <- Komennolla käytät rtl_433 softaa ja saat luettua "-r" tiedoston Converted_433.92M_2000k.cs8 sitten "-F json" tulostaa json tiedoston jota voit selko kielellä lukea ja päätellä tiedostosta tietoa. 

<img width="1011" height="475" alt="image" src="https://github.com/user-attachments/assets/6a4006e2-e5bb-4c90-a4de-ea8ae9597d4b" />

"Mitä ihmettä näytteessä sitten näkyy"
Näytteessä näkyy että joku laite yrittää lähettää OFF komentoja, eli käskyä sammuttaa signaalia vastaanottava laite <img width="60" height="37" alt="image" src="https://github.com/user-attachments/assets/750aebc3-6447-4571-adcd-e362c9b45f45" />

Kaikilla eri protokollilla "proove, Nexa ja Klik.." on sama tunniste/id 8785315 joten kyseessä ei ole monta eri laitetta vaan yksi laite joka käyttää monta protokollaa. <img width="124" height="31" alt="image" src="https://github.com/user-attachments/assets/6a94357a-13a1-4e02-8c4e-fb4e1b66fe98" />

    c) Automaattinen analyysi. Mitä tässä näytteessä tapahtuu? Mitä tunnisteita (id yms) löydät? Converted_433.92M_2000k.cs8. Analysoi näyte 'rtl_433' ohjelmalla.

## Vastaus tehtävään d

**"wget https://terokarvinen.com/verkkoon-tunkeutuminen-ja-tiedustelu/samples/Recorded-HackRF-20250411_183354-433_92MHz-2MSps-2MHz.complex16s"** <- Taas lähetään tällä wget komennolla alkuun että saadaan tiedosto/näyte tietokoneelle.

<img width="1096" height="266" alt="image" src="https://github.com/user-attachments/assets/3f3687f9-ad5a-4b80-bbf9-898ada3ee144" />

Tehtävässä sanotaan **"Muunna näyte rtl_433-yhteensopivaan muotoon ja analysoi se"** ongelmana tässä on se että rtl_433 osaa lukea jo tiedoston ilman mitään muunnoksia, joten tiedostoa ei tarvitse muuntaa.

<img width="1099" height="338" alt="image" src="https://github.com/user-attachments/assets/c262b5ba-302b-42a1-9982-442f1943e794" />

https://github.com/merbanan/rtl_433/blob/master/docs/IQ_FORMATS.md alhaalla näkyy rtl_433 github sivun manuaalista että rtl_433 hyväksyy complex16s tiedostot heti.

<img width="567" height="414" alt="image" src="https://github.com/user-attachments/assets/758ffa93-7e2f-47e1-b247-e9acaa14251e" />


    d) Too compex 16? Olet nauhoittanut näytteen 'urh' -ohjelmalla .complex16s-muodossa. Muunna näyte rtl_433-yhteensopivaan muotoon ja analysoi se. Näyte Recorded-HackRF-20250411_183354-433_92MHz-2MSps-2MHz.complex16s

## Vastaus tehtävään e

URH (Ultimate Radio Hacker) lataus ohjeet ja käyttö ohjeet löytyy sen github sivulta https://github.com/jopohl/urh

Komennolla ***pipx install urh"** saa URH sovelluksen ladattua mutta pipx viittaa python kieleen joten jos URH ei asennu aikaisemmalla kommennolla pitää ladata ensimmäiseksi pipx -> **"sudo apt install pipx"**

<img width="461" height="93" alt="image" src="https://github.com/user-attachments/assets/406feec0-9dca-4f48-9b41-9749049c1aad" />

<img width="641" height="188" alt="image" src="https://github.com/user-attachments/assets/3b9fcdd9-4cc1-4fe2-b6ee-35c5cd1202d6" />

URH sovellus tuli ladattua jo tunnilla Kaliin joten näytin Ubuntu versiossa terminaali virhe ilmoitukset.

URH sovelluksen saa auki helpolla komennolla **"urh"**

<img width="1035" height="615" alt="image" src="https://github.com/user-attachments/assets/7353542d-0fe0-4d92-a7ff-45683359d421" />

Ladataan 1-on-on-on-HackRF... tiedosto koneelle wget avulla.

<img width="744" height="265" alt="image" src="https://github.com/user-attachments/assets/7047fe78-1c1e-447a-becc-e540b0fb1c5b" />

URH sovelluksen vasemmasta yläkulmasta löytyy nappi **"File"** sitten avautuvasta valikosta **"Open"** ja etsitään juuri ladattu tiedosto.

<img width="321" height="117" alt="image" src="https://github.com/user-attachments/assets/0a8ad93d-3cc2-471a-a09a-b094149d48e7" />

<img width="965" height="641" alt="image" src="https://github.com/user-attachments/assets/cbcc18fa-ad8e-4727-9b4c-cf802045f178" />

Tiedosto avattu URH sovelluksessa

<img width="1105" height="645" alt="image" src="https://github.com/user-attachments/assets/535c4a19-7d4c-4e24-94a2-b59e854183bb" />

    e) Ultimate. Asenna URH, the Ultimate Radio Hacker.
    Tarkastele näytettä 1-on-on-on-HackRF-20250412_113805-433_912MHz-2MSps-2MHz.complex16s. Siinä Nexan pistorasian kaukosäätimen valon 1 ON -nappia on painettu kolmesti. Käytä Ultimate Radio Hacker 'urh' -ohjelmaa.

## Vastaus tehtävään f

Painamalla info nappia  <img width="97" height="36" alt="image" src="https://github.com/user-attachments/assets/54101e4b-a5d8-4660-b049-387180902d0f" />
 URH sovelluksessa kun näyte on auki saadaan pientä infoa ilman erikoista tutkimista.

<img width="771" height="227" alt="image" src="https://github.com/user-attachments/assets/f2c20167-f1a9-44e2-b485-1bffd3c60e6f" />

Info ikkunasta saadaan selville nämä asiat.
- Näytteen otto taajuus = 2 MSps (Löytyy tiedoston nimestä, laitetaan se itse kohtaan sample rate)
- Näytteen kesto = 2,75 sekuntia (Info ikkunassa aika perustuu näytteen otto taajuuteen)
- Näyteteen teko aika saadaan nimestä 12.04.2025 (tiedoston nimessä merkattu tyylillä -> 20250412)

      f) Yleiskuva. Kuvaile näytettä yleisesti: kuinka pitkä, millä taajuudella, milloin nauhoitettu? Miltä näyte silmämääräisesti näyttää?

## Vastaus tehtävään g

Tässä maalasin kokonaisen "on" kommenon osuuden enne pientä stoppia, vaikka on monta on komentoa nopeassa rivissä niin meinaa vain että yksi painallus laitteessa lähettää monta kertaa käskyn jotta se menee varmasti perille.

<img width="1081" height="711" alt="image" src="https://github.com/user-attachments/assets/40d9a92e-464b-4eee-9408-b7d29fc336e3" />

Nyt on niin zoomattu kuva että näkee yksittäisen pulssin eli 1 tai 0 maalasin 3 bittiä 101 ja kuvaavassa ikkunassa näkyy miten on, off, on bitti maalattu. erittäin zoomattu versio ylemmästä kuvasta, yksi iso "on" pulssi perustuu moneen pieneen bittiin. Modulaation selvittäminen helpottui kun painoi auto detect ja sitten softa antoi ASK modulaation.

<img width="759" height="483" alt="image" src="https://github.com/user-attachments/assets/e741a446-999e-4228-98a3-5af1b1b53cb2" />

Maalasin yhden bitin ja huomaa että yksi bitti on 526 samples kooltaan, huomasin että ei kaikki mutta suurin osa tippuu tuohon 500 jotain luokkaan. voi muokata omaa samples/symbol sen mukaan. yksi bitti on myös ajallisesti 263 μs eli 263 mikrosekuntia pitkä https://fi.wikipedia.org/wiki/Sekunti

<img width="638" height="400" alt="image" src="https://github.com/user-attachments/assets/d6767a35-fd84-493e-a0ab-0ad6f43c48ed" />

Vähän apuja antava youtube video https://www.youtube.com/watch?v=MTzFFOBYyZA mutta loppujen lopuksi user guide auttaa myös https://www.oldergeeks.com/downloads/files/userguide.pdf

    g) Bittistä. Demoduloi signaali niin, että saat raakabittejä. Mikä on oikea modulaatio? Miten pitkä yksi raakabitti on ajassa? Kuvaile tätä aikaa vertaamalla sitä johonkin. (Monissa singaaleissa on line encoding, eli lopullisia bittejä varten näitä "raakabittejä" on vielä käsiteltävä)

## En vastannut h  + i 

    h) Vapaaehtoinen: Sdr++. Kokeile sdr++ -sovellusta ja esittele sillä jokin "hei maailma" -tyyppinen esimerkki.
    i) Vapaaehtoinen, vaikeahko: GNU Radio. Asenne GNU Radio ja tee sillä yksinkertainen "Hei maailma".
