# h3 Aaltoja harjaamassa

## Vastaus tehtävään X

Hubacek
bläh

Cornelius
bläh

Vapaaehtoinen Lohner
bläh

     x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva.)
    Hubacek 2019: Universal Radio Hacker SDR Tutorial on 433 MHz radio plugs (Video, alkaen 3:19 ja päättyen 7:40. Yhteensä noin 4 min.)
    Cornelius 2022: Decode 433.92 MHz weather station data
    Vapaaehtoinen, vaikeahko: Lohner 2019: Decoding ASK/OOK_PPM Signals with URH and rtl_433


## Vastaus tehtävään b

Komennolla **"rtl_433 -V"** tulostaa rtl_433 versio tiedot.
<img width="608" height="67" alt="image" src="https://github.com/user-attachments/assets/919439d7-9e4d-40cd-9d2f-e80de4cddcc3" />

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

**"wget https://terokarvinen.com/verkkoon-tunkeutuminen-ja-tiedustelu/samples/Recorded HackRF-20250411_183354-433_92MHz-2MSps-2MHz.complex16s"** <- Taas lähetään tällä wget komennolla alkuun että saadaan tiedosto/näyte tietokoneelle.

<img width="1096" height="266" alt="image" src="https://github.com/user-attachments/assets/3f3687f9-ad5a-4b80-bbf9-898ada3ee144" />

Tehtävässä sanotaan **"Muunna näyte rtl_433-yhteensopivaan muotoon ja analysoi se"** ongelmana tässä on se että rtl_433 osaa lukea jo tiedoston ilman mitään muunnoksia, joten tiedostoa ei tarvitse muuntaa.

<img width="1099" height="338" alt="image" src="https://github.com/user-attachments/assets/c262b5ba-302b-42a1-9982-442f1943e794" />

https://github.com/merbanan/rtl_433/blob/master/docs/IQ_FORMATS.md alhaalla näkyy rtl_433 github sivun manuaalista että rtl_433 hyväksyy complex16s tiedostot heti.

<img width="567" height="414" alt="image" src="https://github.com/user-attachments/assets/758ffa93-7e2f-47e1-b247-e9acaa14251e" />


    d) Too compex 16? Olet nauhoittanut näytteen 'urh' -ohjelmalla .complex16s-muodossa. Muunna näyte rtl_433-yhteensopivaan muotoon ja analysoi se. Näyte Recorded-HackRF-20250411_183354-433_92MHz-2MSps-2MHz.complex16s

## Vastaus tehtävään e
    
    e) Ultimate. Asenna URH, the Ultimate Radio Hacker.
    Tarkastele näytettä 1-on-on-on-HackRF-20250412_113805-433_912MHz-2MSps-2MHz.complex16s. Siinä Nexan pistorasian kaukosäätimen valon 1 ON -nappia on painettu kolmesti. Käytä Ultimate Radio Hacker 'urh' -ohjelmaa.
        f) Yleiskuva. Kuvaile näytettä yleisesti: kuinka pitkä, millä taajuudella, milloin nauhoitettu? Miltä näyte silmämääräisesti näyttää?
        g) Bittistä. Demoduloi signaali niin, että saat raakabittejä. Mikä on oikea modulaatio? Miten pitkä yksi raakabitti on ajassa? Kuvaile tätä aikaa vertaamalla sitä johonkin. (Monissa singaaleissa on line encoding, eli lopullisia bittejä varten näitä "raakabittejä" on vielä käsiteltävä)
    h) Vapaaehtoinen: Sdr++. Kokeile sdr++ -sovellusta ja esittele sillä jokin "hei maailma" -tyyppinen esimerkki.
    i) Vapaaehtoinen, vaikeahko: GNU Radio. Asenne GNU Radio ja tee sillä yksinkertainen "Hei maailma".

Vinkit

    WebSDR
        Löydät asemia hakukoneilla. Niitä voi käyttää selaimella.
        Valitse taajuus ja modulaatio. Säätele, kunnes radiolähetys kuuluu kaiuttimista.
    rtl_433
        Purkaa automaattisesti lukuisia protokollia
        Tukee muitakin taajuuksia kuin 433 MHz
        Kalissa 'sudo apt-get install rtl_433' (ja Sid:ssä)
        Debianissa ja muissa
            Projektin Github-sivulta merbanan/rtl_433
            Releases-sivulta tuorein versio, jossa on:
                Linux
                amd64
                SoapySDR (ei vaikuta tähän harjoitukseen, mutta vaaditaan esim HackRF-tukeen)
                Omaan järjestelmään sopiva OpenSSL versio, Debian 12-Bookworm kanssa 3
            $ sudo apt-get -y install atool wget libssl-dev libtool libusb-1.0-0-dev librtlsdr-dev rtl-sdr libsoapysdr-dev
            $ wget https://github.com/merbanan/rtl_433/releases/download/25.02/rtl_433-soapysdr-openssl3-Linux-amd64-25.02.zip
            $ aunpack rtl*.zip
        Voi lukea suoraan radiolta (oletus) tai tiedostosta
            $ rtl_433 -r foo_433.92M_1000k.cs8
            $ man rtl_433
        Tiedostomuodon muuttaminen 'urh' complex16s -> 'rtl_433' cs8
            Vain tiedoston nimi muuttuu
            Tiedoston nimessä pitää olla oikea taajuus (center frequency) ja näytteenottotaajuus (sample rate)
            Erottimena alaviiva
            foo_433.92M_1000k.cs8
            File name meta data
    Ultimate Radio Hacker 'urh'
        URH avulla voi analysoida lähetteitä
        Tässä kokeilemme analyysin alkuvaiheita, joissa saadut bitit eivät vielä ole niitä lopullisia bittejä
        Helppo asennus, sopii valmiiksi kaapattujen signaalien analyysiin
            $ sudo apt-get update
            $ sudo apt-get -y install pipx
            $ pipx install urh
            $ pipx ensurepath
            sulje ja avaa terminaali
            $ urh
            URH graafinen käyttöliittymä aukeaa
        Signaalien sieppaamiseen tarvitaan laitetuki omalle softaradiolle. Tätä varten jouduin itse kääntämään sorsista ja säätelemään. Tässä tehtävässä et tarvitse laitetukea softaradiolle.
        Voit leikata (crop) signaalia valitsemalla sen aallosta. Crop löytyy kontekstivalikosta, joka aukeaa hiiren oikealla napilla.
    Gqrx löytyy Debianin paketinhallinnasta
    Läpikävely (walktrough / spoiler): Nurminen 2025: h3 Aaltoja harjaamassa
