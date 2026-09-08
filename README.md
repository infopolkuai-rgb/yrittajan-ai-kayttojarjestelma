# Yrittäjän AI-käyttöjärjestelmä

Tyhjä pohja, joka muuttaa Claude Coden yleisavustajasta sinun yrityksesi assistentiksi.

Kun tämä on käytössä, sinun ei tarvitse selittää joka keskustelussa mitä yrityksesi tekee, kenelle myyt tai millä tyylillä kirjoitat. Assistentti tietää sen, koska se lukee ne tästä kansiosta joka kerta.

## Asennus

Kolme askelta. Sun ei tarvitse ladata mitään eikä purkaa mitään, assistentti kasaa kansion puolestasi.

1. Luo koneellesi uusi tyhjä kansio, vaikka yrityksesi nimellä.
2. Avaa se Claude Codessa.
3. Liitä tämä viesti:

```
Asenna tähän kansioon Yrittäjän AI-käyttöjärjestelmä.
Ohjeet ovat tiedostossa ASENNUS.md:
https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/blob/main/ASENNUS.md
```

Kun kansio on kasassa, avaa uusi keskustelu ja kirjoita `/aloita`.

Koko ohje ja se mitä asennuksen jälkeen tapahtuu: [docs/opas.md](docs/opas.md).

## Mitä tämä on

Kansio tiedostoja. Ei ohjelmaa, ei sovellusta, ei omia tunnuksia. Osa tiedostoista on faktoja sinusta ja yrityksestäsi. Osa on komentoja, joita assistentti osaa ajaa.

Tiedostot pysyvät sinun koneellasi. Voit lukea ja muokata jokaista niistä tavallisella tekstieditorilla.

## Mitä tarvitset

- Claude Pro -tilaus, 20 dollaria kuussa. Se sisältää Claude Coden.
- Tunti aikaa ja kaksi omaa tekstiä, jotka olet itse kirjoittanut.

Ohjelmointitaitoa ei tarvita.

## Viisi komentoa

| Komento | Mitä tekee | Milloin |
|---|---|---|
| `/aloita` | Haastattelee sinut ja täyttää pohjat | Ensimmäisenä päivänä |
| `/syvenna` | Purkaa yhden asian päästäsi tiedostoon | Aina kun tarve |
| `/linkita` | Lisää uuden kansion tai lähteen löydettäväksi | Kun otat jotain uutta käyttöön |
| `/tarkista` | Testaa toimiiko järjestelmä ja antaa pisteet | Päivänä 7, sitten viikoittain |
| `/kehita` | Vie yhden parannuksen maaliin | Päivänä 14, sitten viikoittain |

## Kansiot

```
├── CLAUDE.md              Assistentin käyttöohje. /aloita täyttää tämän
├── haastattelu.md         Alkuhaastattelun 7 kysymystä
├── yhteydet.md            Mihin assistentti yltää ja mihin ei
├── tausta/                Faktat: yritys, prioriteetit, kirjoitustyyli
├── ohjeet/                Työskentelymalli ja päätöspohja
├── paatokset/loki.md      Mitä päätit ja miksi
├── haastattelut/          /syvenna tallentaa tänne. Yksityinen
├── tarkistukset/          /tarkista tallentaa tänne. Yksityinen
├── arkisto/               Vanhentunut tavara
├── docs/opas.md           Koko ohje ihmiselle
└── ASENNUS.md             Asennusohje tekoälylle
```

Laajentaminen: [LAAJENNUKSET.md](LAAJENNUKSET.md). Älä luo kansioita etukäteen.

## Kaksi muistisääntöä

**Kolme A:ta** on ajattelutapa: Asenne, Askeleet, Automaatio. **Neljä T:tä** on rakenne: Tieto, Työkalut, Taidot, Tahti. Molemmat auki tiedostossa [ohjeet/tyoskentelymalli.md](ohjeet/tyoskentelymalli.md).

Kysy jokaisen uuden tehtävän kohdalla, missä määrin tekoäly voi hoitaa sen. Etene pullonkaulasta mittariin. Rakenna pieninä paloina ja aja ensin käsin. Järjestelmässä Tieto tulee ensin ja Tahti viimeisenä.

## Yksityisyys

Jätin haastattelut ja tarkistusraportit gitin ulkopuolelle, koska niihin päätyy yleensä asiakastietoa. Salasanat ja avaimet eivät kuulu mihinkään tämän kansion tiedostoon.

## Lisenssi

MIT. Tee tällä mitä haluat, myös kaupallisesti. Ehdot suomeksi: [LISENSSI.md](LISENSSI.md). Sitova teksti: [LICENSE](LICENSE).

Tehnyt Ilmari Salmisto, [PolkuAI](https://polkuai.com). Jos rakennat tästä jotain, kuulisin siitä mielelläni.
