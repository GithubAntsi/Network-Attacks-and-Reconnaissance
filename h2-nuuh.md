# h2 Nuuh

## Vastaus Tehtävään X

Wireshark
- Wireshark on erittäin tunnettu ja suosittu tietoverkko snifferi/analysointi softa.
- Liikenteen analysointi on erittäin helppoa Wiresharkin avulla.
- Wireshark antaa hirveästi tietoa, joten analysointia suositellaan pienissä erissä.

Network Interface Names on Linux
- Verkkoliitäntä voi olla fyysinen tai virtuaalinen.
- Prefix nimetys Linuxissa (en = Wired Ethernet, wl = WLAN, wireless local area network, Wifi, lo = Loopback adapter)
- Liitännän loppuosa kertoo MAC osoitteen (numerosarja) tai mihin se on liitetty tietokoneessa.

      x) Lue ja tiivistä. (Tässä x-alakohdassa ei tarvitse tehdä testejä tietokoneella, vain lukeminen tai kuunteleminen ja tiivistelmä riittää. Tiivistämiseen riittää muutama ranskalainen viiva.)
      Karvinen 2025: Wireshark - Getting Started https://terokarvinen.com/wireshark-getting-started/
      Karvinen 2025: Network Interface Names on Linux https://terokarvinen.com/network-interface-linux/


## Vastaus Tehtävään A

Asensin Kalin virtual boxiin, ei mitään ongelmia. Asennus meni helposti ja ei eronnut muista aikaisemmista tehdyistä linux asennuksista.

<img width="1282" height="889" alt="image" src="https://github.com/user-attachments/assets/fe813cc0-50b8-472f-b223-e1fc0bdc8dd7" />

    a) Linux. Asenna Debian tai Kali Linux virtuaalikoneeseen. (Tätä alakohtaa ei poikkeuksellisesti tarvitse raportoida, jos sinulla ei ole mitään ongelmia. Jos on mitään haasteita, tee täsmällinen raportti)
    
## Vastaus Tehtävään B

Toimiva yhteys, ping google 8.8.8.8
<img width="665" height="536" alt="image" src="https://github.com/user-attachments/assets/97b94434-f3f9-439c-874c-b0ae938ac83f" />

Ei toimiva yhteys > internet yhteys poistettu hetkellisesti, ping google 8.8.8.8
<img width="664" height="533" alt="image" src="https://github.com/user-attachments/assets/0eedb513-2af2-44c0-a03f-b6f127225fc8" />

    b) Ei voi kalastaa. Osoita, että pystyt katkaisemaan ja palauttamaan virtuaalikoneen Internet-yhteyden.

## Vastaus Tehtävään C

Kali distron mukana tuli wireshark joten asennusta ei tarvitse tehdä.

Avasin Firefox selaimen, läpi tuli ja meni n. 5000 pakettia parin sekunnin sisällä.
<img width="1000" height="726" alt="image" src="https://github.com/user-attachments/assets/065285e3-12c3-4580-86de-ad525b30d2be" />

    c) Wireshark. Asenna Wireshark. Sieppaa liikennettä Wiresharkilla. (Vain omaa liikennettäsi. Voit käyttää tähän esimerkiksi virtuaalikonetta).

## Vastaus Tehtävään D

    d) Oikeesti TCP/IP. Osoita TCP/IP-mallin neljä kerrosta yhdestä siepatusta paketista. Selityksen lisäksi laatikoi ne ruutukaappauksesta.

    e) Mitäs tuli surffattua? Avaa surfing-secure.pcap. Tutustu siihen pintapuolisesti ja kuvaile, millainen kaappaus on kyseessä. Tässä siis vain lyhyesti ja yleisellä tasolla. Voit esimerkiksi vilkaista, montako konetta näkyy, mitä protokollia pistää silmään. Määrästä voit arvioida esimerkiksi pakettien lukumäärää, kaappauksen kokoa ja kestoa.

    f) Vapaaehtoinen, vaikea: Mitä selainta käyttäjä käyttää? surfing-secure.pcap (Päivitys 2025-03-31 w14 ma - muutin tehtävän vapaaehtoiseksi Giang:n suosituksesta)

    g) Minkä merkkinen verkkokortti käyttäjällä on? surfing-secure.pcap

    h) Millä weppipalvelimella käyttäjä on surffaillut? surfing-secure.pcap (Huonoja uutisia: yhteys on suojattu TLS-salauksella.)

    i) Analyysi. Sieppaa pieni määrä omaa liikennettäsi. Analysoi se, eli selitä mahdollisimman perusteellisesti, mitä tapahtuu. (Tässä pääpaino on siis analyysillä ja selityksellä, joten liikennettä kannattaa ottaa tarkasteluun todella vähän - vaikka vain pari pakettia. Gurut huomio: Selitä myös mielestäsi yksinkertaiset asiat.)

Vinkit

Karvinen 2024: Install Debian on Virtualbox - Updated 2024
Verkkoyhteyttä testatessa voi vaikkapa ottaa yhteyttä Internet-mammuttien nimipalvelimiin, joilla on helposti muistettavat numerot
        ping 1.1.1.1 # Cloudfare
        ping 8.8.8.8 # Google
TCP/IP-pinosta löytyy hyvä kertaus: Wikipedia: Internet protocol suite
Läpikävely selaimen selvittämiseen kohdassa f. Giang 2025: H1 Sniff: f) Mitä selainta käyttäjä käyttää? (spoiler)
