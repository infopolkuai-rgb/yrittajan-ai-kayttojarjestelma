---
name: tarkista
description: Tarkistaa todisteisiin nojaten, toimiiko järjestelmä. Käytä kun käyttäjä sanoo "tarkista", "toimiiko tämä", "missä mennään", "arvioi järjestelmä", "mitä puuttuu", tai viikoittaisessa katsauksessa. Ajaa viisi hakukoetta, pisteyttää Neljä T:tä, nimeää kolme tärkeintä korjausta ja tallentaa päivätyn raportin.
---

# Tarkista

Tämä ei kysy tuntuuko järjestelmä hyvältä. Tämä kokeilee toimiiko se.

Aja päivänä 7 ja sen jälkeen viikoittain niin kauan kuin rakennat. Kun järjestelmä on vakaa, kuukausittain riittää.

## Pisteytyksen perussääntö

**Piste annetaan todisteesta, ei olemassaolosta.**

Todiste on jokin näistä: onnistunut haku, jonka teit tässä ajossa. Tiedosto, jonka luit ja jossa oli oikeaa sisältöä. Päivätty merkintä siitä, että jokin ajettiin. Käyttäjän vahvistus, että jokin toimi viime viikolla.

Todiste ei ole: kansio, joka on olemassa. Tiedosto, jossa on otsikot mutta ei sisältöä. Skilli, jota ei ole koskaan ajettu. Yhteys, joka on kirjattu mutta jota ei ole kokeiltu.

Jos et pysty toteamaan asiaa itse, se on nolla pistettä ja merkintä "ei varmennettu". Se ei ole rangaistus vaan tieto siitä, mitä pitää seuraavaksi kokeilla.

## Vaihe 1: viisi hakukoetta

Ennen pisteitä testaa löytääkö järjestelmä oman tietonsa. Muodosta viisi kysymystä käyttäjän oman toiminnan pohjalta, älä yleisiä kysymyksiä.

1. **Perustieto.** Mitä tämä yritys tekee ja kuka on paras asiakas?
2. **Tilanne.** Mitkä ovat tämän jakson kolme prioriteettia ja missä kukin menee?
3. **Projekti.** Mikä oli viimeisin tuotos aktiivisessa projektissa ja mikä on seuraava askel?
4. **Muisti.** Mikä päätös tehtiin viimeksi ja miksi?
5. **Ulkopuolinen tieto.** Missä on se tiedosto tai järjestelmä, josta luvut haetaan, ja pääsetkö siihen?

Merkitse jokaisesta neljä asiaa: kysymys, mitä reittiä yritit, mitä löytyi ja kuinka tuoretta se oli.

Tulos on yksi kolmesta:
- **Osuma:** löytyi suoraan reittiä pitkin.
- **Haku pelasti:** ei löytynyt reittiä pitkin mutta löytyi etsimällä. Tämä on puolikas: tieto on olemassa mutta reitti puuttuu.
- **Ei löytynyt:** tieto puuttuu tai on tavoittamattomissa.

Merkitse myös vanhentunut tieto. Kuukauden vanha "tilanne" on löydös, vaikka se löytyisi heti.

## Vaihe 2: pisteet

Neljä kerrosta, kukin 0-25. Kerrokset ja niiden merkitys: `ohjeet/tyoskentelymalli.md`.

**Tieto (0-25).** Tuntee yrityksen ja tilanteen.

| Pisteet | Tila |
|---|---|
| 0-6 | Pohjat tyhjiä tai täytetty yleisillä lauseilla |
| 7-13 | Perustiedot kunnossa, tilannetieto vanhentunutta |
| 14-20 | Hakukokeet 1, 2 ja 4 osuvat, tieto on alle kuukauden vanhaa |
| 21-25 | Myös rajat, hinnat ja hylätyt asiat kirjattu, päätöslokissa merkintöjä useammalta viikolta |

**Työkalut (0-25).** Yltää sinne missä tieto on.

| Pisteet | Tila |
|---|---|
| 0-6 | Kaikki liitetään käsin |
| 7-13 | Yksi yhteys kokeiltu ja toimii |
| 14-20 | Kaksi tai kolme yhteyttä toimii, `yhteydet.md` pitää paikkansa |
| 21-25 | Hakukoe 5 osuu ilman käyttäjän apua, myös puuttuvat yhteydet on tunnistettu |

Kirjattu mutta kokeilematon yhteys on nolla. Tarkista `yhteydet.md`:n päivämäärät.

**Taidot (0-25).** Osaa tehdä työn vaiheet.

| Pisteet | Tila |
|---|---|
| 0-6 | Vain keskustelua |
| 7-13 | Mukana tulleet komennot käytössä |
| 14-20 | Vähintään yksi oma komento, jota on ajettu useammin kuin kerran |
| 21-25 | Oma komento tuottaa valmiin tuotoksen, ja edellisestä ajosta on merkintä |

Skilli, jota ei ole ajettu, ei tuo pisteitä.

**Tahti (0-25).** Toimii ilman pyytämistä.

| Pisteet | Tila |
|---|---|
| 0-6 | Kaikki alkaa siitä että käyttäjä avaa keskustelun |
| 7-13 | Käyttäjällä on säännöllinen rutiini, ajaa itse |
| 14-20 | Jokin ajastettu tai toistuva ajo on käynnissä ja siitä on jälki |
| 21-25 | Ajo on tuottanut hyötyä ilman että sitä pyydettiin, useammin kuin kerran |

**Katot.** Kerros ei voi ylittää alempaa kerrosta enempää kuin viidellä pisteellä. Jos Tieto on 10, Taidot voi olla enintään 15. Syy: nopea kone väärällä tiedolla tekee vääriä asioita nopeammin.

Näytä laskutoimitus. Kerro jokaisesta pisteestä mihin todisteeseen se nojaa.

## Vaihe 3: kolme korjausta

Nimeä kolme parannusta tärkeysjärjestyksessä. Jokaisesta neljä riviä:

- **Mikä:** yksi lause.
- **Miksi nyt:** mihin löydökseen tämä liittyy.
- **Ensimmäinen askel:** konkreettinen teko, joka vie alle tunnin.
- **Mistä tiedän että se on kunnossa:** mitä pitää pystyä toteamaan seuraavassa ajossa.

Jos yksi kerros on selvästi muita heikompi, kaikki kolme korjausta saavat koskea sitä.

Ehdota lopuksi valmis komento tärkeimmälle korjaukselle. Yleensä `/kehita` tai `/linkita`.

## Vaihe 4: raportti

Tallenna `tarkistukset/VVVV-KK-PP.md`. Jos saman päivän tiedosto on jo olemassa, lisää perään `-2`.

Raportin osat: päivämäärä, kokonaispisteet ja neljä osapistettä, hakukokeiden taulukko, todisteet kerroksittain, kolme vahvuutta todisteineen, kolme korjausta, vertailu edelliseen raporttiin.

Anna jokaiselle löydökselle tunnus muotoa `L1`, `L2`. Käytä samaa tunnusta seuraavassa raportissa, jos löydös on yhä auki.

**Vertailu edelliseen.** Lue viimeisin raportti kansiosta. Merkitse jokainen vanha löydös: korjattu, yhä auki, palasi, ei tarkistettu, ei enää ajankohtainen.

Korjatuksi merkitseminen vaatii uuden todisteen. Käyttäjän ilmoitus siitä että hän korjasi asian ei riitä, jos et pysty toteamaan sitä.

Erottele pistemuutoksen syy: parantuiko järjestelmä, vai löysitkö tällä kertaa paremmat todisteet samasta asiasta. Nämä näyttävät raportissa samalta mutta tarkoittavat eri asiaa.

Vahvista käyttäjälle että tiedosto kirjoitettiin, ennen kuin näytät yhteenvedon.

## Rajat

- Älä korjaa mitään tässä ajossa. Tämä skilli katsoo ja kirjoittaa raportin. Korjaaminen on `/kehita`.
- Älä anna pisteitä kohteliaisuudesta. Matala luku ensimmäisessä ajossa on normaali ja hyödyllinen.
- Älä vertaa käyttäjää muihin. Ainoa vertailukohta on hänen edellinen raporttinsa.
- Raportit ovat yksityisiä ja gitin ulkopuolella. Ne voivat sisältää asiakastietoa.
