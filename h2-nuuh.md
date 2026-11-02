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

Avasin Firefox selaimen, läpi tuli ja meni n. 5000 pakettia pienessä hetkessä.

<img width="1000" height="726" alt="image" src="https://github.com/user-attachments/assets/065285e3-12c3-4580-86de-ad525b30d2be" />

    c) Wireshark. Asenna Wireshark. Sieppaa liikennettä Wiresharkilla. (Vain omaa liikennettäsi. Voit käyttää tähän esimerkiksi virtuaalikonetta).

## Vastaus Tehtävään D

DNS paketti, kuvassa näkyy TCP/IP mallin neljä kerrosta. (Sovellus kerros = DNS, Kuljetus kerros = UDP, Internet kerros = IPv4 ja Linkki kerros = Ethernet II)

<img width="1000" height="726" alt="image" src="https://github.com/user-attachments/assets/fe621318-1ce9-47e0-b664-27aa983722d7" />

DNS = Kysyy verkkotunnuksen tietoja kuten IP osoite
UDP = Ohjaa liikennettä porttien avulla oikeaan paikkaan
IPv4 = Lähde ja kohde ip osoitteet
Ethernet = Lähde ja kohde MAC osoitteet

    d) Oikeesti TCP/IP. Osoita TCP/IP-mallin neljä kerrosta yhdestä siepatusta paketista. Selityksen lisäksi laatikoi ne ruutukaappauksesta.

## Vastaus Tehtävään E

Surfing-secure.pcap tiedosto, avattiin wiresharkilla. Ekat asiat mitä huomasi = Tiedosto on pieni 124 KB ja paketteja oli vain 283 joten ei ole mahdottoman iso paketti ettei voisi selata yksitellen läpi.

Selailessa huomaa että henkilö on selannut nettiä ja mennyt eri netti osoitteisiin kuten, google näkyy heti tiedoston alussa terokarvinen.com löytyy myös.

IP osoitteet.

<img width="595" height="185" alt="image" src="https://github.com/user-attachments/assets/76f4eaff-5f8d-4294-b2c2-8a16e62ef262" />

MAC osoitteet.

<img width="553" height="94" alt="image" src="https://github.com/user-attachments/assets/b07ab49d-3aac-4745-bac1-c1e57c7f627e" />

Tiedoston statistiikat.

<img width="530" height="192" alt="image" src="https://github.com/user-attachments/assets/22c019a2-4d13-4e91-81de-556653d0372b" />

    e) Mitäs tuli surffattua? Avaa surfing-secure.pcap. Tutustu siihen pintapuolisesti ja kuvaile, millainen kaappaus on kyseessä. Tässä siis vain lyhyesti ja yleisellä tasolla. Voit esimerkiksi vilkaista, montako konetta näkyy, mitä protokollia pistää silmään. Määrästä voit arvioida esimerkiksi pakettien lukumäärää, kaappauksen kokoa ja kestoa.

## Vastaus Tehtävään F

EN TEHNYT TEHTÄVÄÄ F

    f) Vapaaehtoinen, vaikea: Mitä selainta käyttäjä käyttää? surfing-secure.pcap (Päivitys 2025-03-31 w14 ma - muutin tehtävän vapaaehtoiseksi Giang:n suosituksesta)

## Vastaus Tehtävään G

Näitten MAC osoite tietojen perusteella selvitin että kyseessä ei pitäisi olla fyysinen oikean tuottajan kortti vaan virtuaalinen kortti (QEMU / KVM virtuaali ympäristön verkkokortti).

<img width="545" height="90" alt="image" src="https://github.com/user-attachments/assets/8f9505c5-ea91-47d0-ba40-2992ec24a7eb" />

<img width="616" height="87" alt="image" src="https://github.com/user-attachments/assets/89e7b1f2-d5f8-4f1f-8f4b-5aaef16878a9" />

    g) Minkä merkkinen verkkokortti käyttäjällä on? surfing-secure.pcap

## Vastaus Tehtävään H

Tässä on tummennettu 3 kiinnostavinta pakettia, koko homma alkaa ihan perus query:lla terokarvinen.com sivulle (Paketti 19) sitten tulee vastaus (Paketti 22) ja sitten Client Hello (Paketti 32)

TLS salaa sovellus liikennettä mutta silti nähdään DNS kyselyt ja vastukset joten tiedetään mihin henkilö on mennyt (Palvelin nimi on selkokielellä)

<img width="953" height="253" alt="image" src="https://github.com/user-attachments/assets/ff8063af-4134-4f5c-b14e-612ef164020a" />

    h) Millä weppipalvelimella käyttäjä on surffaillut? surfing-secure.pcap (Huonoja uutisia: yhteys on suojattu TLS-salauksella.)

## Vastaus Tehtävään I

Sieppasin omaa Wifi Windows 11 koneeni verkkoliikennettä sillä olisi kiinnostavempaa itselleni kuin VM verkkoliikenteen tarkistelu.

Kaappauksen statistiikat

<img width="540" height="198" alt="image" src="https://github.com/user-attachments/assets/1129f218-35df-4b2d-95f6-239f4680a7f3" />

Valitsin analyysia varten kaksi pakettia, paketit 33 & 34

<img width="1248" height="30" alt="image" src="https://github.com/user-attachments/assets/4d378b38-39ad-4976-a489-830607dd809e" />

DNS kysely pari, suurin valinta syy oli tutun kuuloinen osoite = g.live.com

https://learn.microsoft.com/en-gb/windows/privacy/windows-11-endpoints-non-enterprise-editions

<img width="643" height="84" alt="image" src="https://github.com/user-attachments/assets/bdf6782f-483b-49bb-9e34-38bdb5ac1055" />

Paketti 33 lähettää DNS kyselyn jotta saadaan tietää IP osoite jotta tietokone voi kommunikoida g.live.com osoitteen kanssa ei käytä selkokielistä g.live.com vaan xxx.xxx.xxx.xxx mallia (IPv4). Source on oma tietokoneeni IP ja sitten destination on oma tietokoneeni DNS palvelin.

<img width="242" height="56" alt="image" src="https://github.com/user-attachments/assets/a2627536-e709-40e0-8cde-46a05209a463" />

Paketti 34 lähettää uuden DNS vastauksen aikaisempaan DNS kyselyyn, vastaus tulee 192.168.1.1 eli oma DNS palvelin. Wiresharkin avulla näkyi millainen Query ja kuinka monta paikkaa piti etsiä että saadaan selville halutun osoitteen IP osoite. (liian pitkä tähän mutta viiden verkkotunnuksen ketju kunnes saatiin selville haluttu IPv4 osoite)

<img width="559" height="113" alt="image" src="https://github.com/user-attachments/assets/e13d9203-16ec-406c-be5e-5a35e9acbb0e" />

Valitsin selitykseen vain paketit 33 ja 34 mutta seuraavissa paketeissa näkyy myös se että kun haku oli onnistunut niin suoraan mennään omasta koneesta haluttuun osoitteeseen ja huomaa jopa ennen TLS salailua että tulee client hello g.live.com osoitteesta

<img width="1078" height="59" alt="image" src="https://github.com/user-attachments/assets/b6241c05-9eb1-4e16-95f9-05a8f8929fb4" />

    i) Analyysi. Sieppaa pieni määrä omaa liikennettäsi. Analysoi se, eli selitä mahdollisimman perusteellisesti, mitä tapahtuu. (Tässä pääpaino on siis analyysillä ja selityksellä, joten liikennettä kannattaa ottaa tarkasteluun todella vähän - vaikka vain pari pakettia. Gurut huomio: Selitä myös mielestäsi yksinkertaiset asiat.)
