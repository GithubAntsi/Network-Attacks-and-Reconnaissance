# h3 Aaltoja harjaamassa

Vastaus tehtävään X

Hubacek
-

Cornelius
-

Vapaaehtoinen Lohner
(En tehnyt)

    x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva.)
        - Hubacek 2019: Universal Radio Hacker SDR Tutorial on 433 MHz radio plugs (Video, alkaen 3:19 ja päättyen 7:40. Yhteensä noin 4 min.)
        - Cornelius 2022: Decode 433.92 MHz weather station data
        - Vapaaehtoinen, vaikeahko: Lohner 2019: Decoding ASK/OOK_PPM Signals with URH and rtl_433
    b) rtl_433. Asenna rtl_433 automaattista analyysia varten. Kokeile, että voit ajaa sitä. './rtl_433' vastaa "rtl_433 version 25.02 branch..."
    c) Automaattinen analyysi. Mitä tässä näytteessä tapahtuu? Mitä tunnisteita (id yms) löydät? Converted_433.92M_2000k.cs8. Analysoi näyte 'rtl_433' ohjelmalla.
    d) Too compex 16? Olet nauhoittanut näytteen 'urh' -ohjelmalla .complex16s-muodossa. Muunna näyte rtl_433-yhteensopivaan muotoon ja analysoi se. Näyte Recorded-HackRF-20250411_183354-433_92MHz-2MSps-2MHz.complex16s
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
