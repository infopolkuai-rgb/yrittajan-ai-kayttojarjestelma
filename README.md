# Yrittäjän AI-käyttöjärjestelmä

Tyhjä pohja, joka muuttaa Claude Coden yleisavustajasta sinun yrityksesi assistentiksi.

Kun tämä on käytössä, sinun ei tarvitse selittää joka keskustelussa mitä yrityksesi tekee, kenelle myyt tai millä tyylillä kirjoitat. Assistentti tietää sen, koska se lukee ne tästä kansiosta joka kerta.

## Asennus

Kolme askelta. Et lataa mitään etkä pura mitään, assistentti kasaa kansion puolestasi.

1. Luo koneellesi uusi tyhjä kansio, vaikka yrityksesi nimellä.
2. Avaa se Claude Codessa.
3. Liitä tämä viesti:

```
Asenna tähän kansioon Yrittäjän AI-käyttöjärjestelmä.
Ohjeet ovat repon README-tiedostossa:
https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma
```

Kun kansio on kasassa, avaa uusi keskustelu ja kirjoita `/aloita`.

Koko ohje ja se mitä asennuksen jälkeen tapahtuu: [docs/opas.md](docs/opas.md).

## Ohjeet tekoälylle

*Tämä osio on assistentille. Ihminen voi hypätä sen yli.*

Sinua on pyydetty asentamaan tämä paketti käyttäjän kansioon. Toimi näin.

**1. Varmista kohde.** Olet käyttäjän omassa kansiossa. Jos kansiossa on jo muuta sisältöä, kysy ennen kuin jatkat. Älä koskaan asenna tätä kansioon, jossa on käyttäjän muita töitä.

**2. Nouda paketti.** Kokeile ensin gitiä. Jos sitä ei ole, lataa arkisto ja pura se. Molemmat toimivat, käytä sitä joka onnistuu.

```bash
git clone --depth 1 https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma.git .tmp-aios
```

Jos git puuttuu, Windowsissa:

```powershell
Invoke-WebRequest -Uri "https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/archive/refs/heads/main.zip" -OutFile "aios.zip"
Expand-Archive -Path "aios.zip" -DestinationPath ".tmp-aios" -Force
```

Macissa ja Linuxissa:

```bash
curl -L -o aios.zip https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/archive/refs/heads/main.zip && unzip -q aios.zip -d .tmp-aios
```

**3. Siirrä sisältö paikalleen.** Arkiston sisällä on yksi kansio nimeltä `yrittajan-ai-kayttojarjestelma-main`. Siirrä **sen sisältö**, ei kansiota itseään, käyttäjän kansion juureen. Muista piilotiedostot: `.claude/` ja `.gitignore` ovat pakollisia, ilman niitä komennot eivät toimi.

**4. Siivoa.** Poista `.tmp-aios`, `aios.zip` ja mahdollinen `.git`-kansio. Käyttäjä ei tarvitse tämän repon historiaa.

**5. Tarkista.** Kansion juuressa pitää olla `CLAUDE.md`, `README.md`, `haastattelu.md`, `yhteydet.md`, kansiot `tausta/`, `ohjeet/`, `paatokset/`, `arkisto/`, `haastattelut/`, `tarkistukset/`, `docs/` sekä `.claude/skills/`, jossa on viisi alikansiota. Jos jokin puuttuu, kerro se äläkä väitä asennusta valmiiksi.

**6. Kerro käyttäjälle mitä seuraavaksi.** Sano kolme asiaa, lyhyesti:
- Kansio on kasassa.
- Hänen pitää avata **uusi keskustelu**, jotta viisi komentoa tulevat käyttöön.
- Uudessa keskustelussa hän kirjoittaa `/aloita`, ja siihen kannattaa varata puoli tuntia sekä kaksi omaa kirjoittamaansa tekstiä.

Älä aja `/aloita` puolesta äläkä täytä pohjia arvaamalla. Asennus päättyy tähän.

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
└── docs/opas.md           Koko ohje
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
