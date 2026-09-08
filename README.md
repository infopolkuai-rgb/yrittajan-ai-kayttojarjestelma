# Yrittäjän AI-käyttöjärjestelmä

Tyhjä pohja, joka muuttaa Clauden yleisavustajasta sinun yrityksesi assistentiksi. Asennus vie noin viisitoista minuuttia. Ei vaadi ohjelmointitaitoa.

Kun tämä on käytössä, sinun ei tarvitse selittää joka keskustelussa mitä yrityksesi tekee, kenelle myyt tai millä tyylillä kirjoitat. Assistentti tietää sen, koska se lukee ne tästä kansiosta joka kerta.

**Aloita tästä: [docs/opas.md](docs/opas.md).** Se on koko ohje alusta loppuun.

## Mitä tämä on

Kansio tiedostoja. Ei ohjelma, ei sovellus, ei tunnuksia. Osa tiedostoista on faktoja sinusta ja yrityksestäsi. Osa on komentoja, joita assistentti osaa ajaa.

Tiedostot pysyvät sinun koneellasi. Voit lukea ja muokata jokaista niistä tavallisella tekstieditorilla.

## Mitä tarvitset

- Claude-tilaus
- Claude-työpöytäsovellus (Windows tai Mac)
- Vartti aikaa ja kaksi omaa tekstiä, jotka olet itse kirjoittanut

## Pikastartti

1. Lataa tämä kansio koneellesi. Vihreä **Code**-painike ylhäällä, sitten **Download ZIP**. Pura zip.
2. Avaa Claude-työpöytäsovellus ja valitse tämä kansio.
3. Kirjoita `/aloita` ja vastaa seitsemään kysymykseen.
4. Kysy lopuksi: *"Mihin mun kannattaa keskittyä tällä viikolla?"*

Jos jokin näistä askeleista tökkää, [oppaassa](docs/opas.md) on jokainen kohta kuvien kanssa.

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
└── docs/opas.md           Koko ohje
```

Laajentaminen: [LAAJENNUKSET.md](LAAJENNUKSET.md). Älä luo kansioita etukäteen.

## Kaksi muistisääntöä

**Kolme A:ta** on ajattelutapa: Asenne, Askeleet, Automaatio. **Neljä T:tä** on rakenne: Tieto, Työkalut, Taidot, Tahti. Molemmat auki tiedostossa [ohjeet/tyoskentelymalli.md](ohjeet/tyoskentelymalli.md).

Lyhyesti: kysy jokaisen uuden tehtävän kohdalla missä määrin tekoäly voi hoitaa sen, etene pullonkaulasta mittariin, rakenna pieninä paloina ja aja ensin käsin. Järjestelmässä Tieto tulee ensin ja Tahti viimeisenä.

## Yksityisyys

Haastattelut ja tarkistusraportit on jätetty gitin ulkopuolelle, koska niissä on yleensä asiakastietoa. Salasanat ja avaimet eivät kuulu mihinkään tämän kansion tiedostoon.

## Lisenssi

MIT. Tee tällä mitä haluat, myös kaupallisesti. Katso [LICENSE](LICENSE).

Tehnyt Ilmari Salmisto, [PolkuAI](https://polkuai.com). Jos rakennat tästä jotain, kuulisin siitä mielelläni.
