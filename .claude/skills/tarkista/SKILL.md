---
name: tarkista
description: Tarkistaa todisteisiin nojaten, toimiiko järjestelmä. Käytä kun käyttäjä sanoo "tarkista", "toimiiko tämä", "missä mennään", "arvioi järjestelmä", "mitä puuttuu", tai viikoittaisessa katsauksessa. Ajaa viisi hakukoetta, pisteyttää Neljä T:tä, nimeää kolme tärkeintä korjausta ja tallentaa päivätyn raportin.
---

# Tarkista

Tämä ei kysy, tuntuuko järjestelmä hyvältä. Tämä kokeilee, toimiiko se.

Aja päivänä 7 ja sen jälkeen viikoittain niin kauan kuin rakennat. Kun järjestelmä on vakaa, kuukausittain riittää.

## Pisteytyksen perussääntö

**Piste annetaan todisteesta, ei olemassaolosta.**

Todisteeksi kelpaa onnistunut haku, jonka teit tässä ajossa. Samoin kelpaa tiedosto, jonka luit ja jossa oli oikeaa sisältöä. Päivätty merkintä siitä, että jokin ajettiin, on todiste. Niin on myös käyttäjän vahvistus siitä, että jokin toimi viime viikolla.

Todiste ei ole:

- kansio, joka on olemassa
- tiedosto, jossa on otsikot mutta ei sisältöä
- komento, jota ei ole koskaan ajettu
- yhteys, joka on kirjattu mutta jota ei ole kokeiltu

Jos et pysty toteamaan asiaa itse, se on nolla pistettä ja merkintä "ei varmennettu". Se ei ole rangaistus vaan tieto siitä, mitä pitää seuraavaksi kokeilla.

## Vaihe 1: viisi hakukoetta

Ennen pisteitä testaa, löytääkö järjestelmä oman tietonsa. Alla on viisi aihetta. Muotoile jokainen käyttäjän omilla sanoilla ja hänen omista projekteistaan, älä kysy niitä yleisessä muodossa. Jos käyttäjä myy sähköurakoita, kysy sähköurakoista.

1. **Perustieto.** Mitä tämä yritys tekee ja kuka on paras asiakas?
2. **Tilanne.** Mitkä ovat tämän jakson kolme prioriteettia ja missä kukin menee?
3. **Projekti.** Mikä oli viimeisin tuotos aktiivisessa projektissa ja mikä on seuraava askel?
4. **Muisti.** Mikä päätös tehtiin viimeksi ja miksi?
5. **Ulkopuolinen tieto.** Missä on se tiedosto tai järjestelmä, josta luvut haetaan? Ja pääsetkö siihen käsiksi?

Merkitse jokaisesta neljä asiaa: kysymys, mitä reittiä yritit, mitä löytyi ja kuinka tuoretta se oli.

Tulos on yksi näistä:

| Tulos | Milloin |
|---|---|
| **Osuma** | Löytyi suoraan reittiä pitkin |
| **Haku pelasti** | Ei löytynyt reittiä pitkin mutta löytyi etsimällä. Tieto on olemassa, reitti puuttuu |
| **Löytyi, ei pääsyä** | Tiedetään missä tieto on, mutta siihen ei ylletä. Koskee lähinnä koetta 5 |
| **Ei löytynyt** | Tieto puuttuu kokonaan |
| **Ei sovellu** | Kysymys ei koske tätä käyttäjää. Ei lasketa epäonnistumiseksi |

"Ei sovellu" on olemassa kokeelle 3. Vasta käyttöön otetulla järjestelmällä ei ole aktiivisia projekteja, eikä yhden hengen yrittäjällä välttämättä koskaan ole projektikansiota. Kirjaa se sellaisenaan äläkä vähennä pisteitä.

Merkitse myös vanhentunut tieto. Kuukauden vanha "tilanne" on löydös, vaikka se löytyisi heti.

## Vaihe 2: pisteet

Neljä kerrosta, kukin 0-25. Kerrokset ja niiden merkitys: `ohjeet/tyoskentelymalli.md`.

Ennen pisteitä erottele kaksi asiaa, jotka näyttävät samalta mutta eivät ole: **puuttuuko tieto kokonaan vai onko tiedosto olemassa mutta tyhjä.** Tyhjä pohja on eri löydös kuin puuttuva kansio, ja korjaus on eri. Merkitse kumpi on kyseessä.

**Tieto (0-25).** Tuntee yrityksen ja tilanteen. Pisteet muodostuvat kahdesta puolikkaasta: kattavuudesta ja tuoreudesta.

Kattavuus, enintään 15:

| Pisteet | Tila |
|---|---|
| 0-3 | Pohjat tyhjiä tai täytetty yleisillä lauseilla |
| 4-8 | Yritys ja asiakkaat kirjattu, prioriteeteista puuttuu mittareita |
| 9-12 | Kokeet 1 ja 2 osuvat, kolme prioriteettia mittareineen |
| 13-15 | Myös rajat, hinnat ja hylätyt asiat kirjattu |

Tuoreus, enintään 10:

| Pisteet | Tila |
|---|---|
| 0-2 | Ei mitään merkintää siitä, milloin tietoa on viimeksi katsottu |
| 3-6 | Tieto on kirjattu kerran eikä siihen ole palattu |
| 7-10 | Koe 4 osuu, päätöslokissa merkintöjä useammalta viikolta |

Ensimmäisessä ajossa tuoreus jää yleensä alle kolmen, koska päätöslokia ei ole vielä ehditty käyttää. Se on oikea tulos eikä virhe.

**Työkalut (0-25).** Yltää sinne missä tieto on.

| Pisteet | Tila |
|---|---|
| 0-6 | Kaikki liitetään käsin |
| 7-13 | Yksi yhteys kokeiltu ja toimii |
| 14-20 | Kaksi tai kolme yhteyttä toimii, `yhteydet.md` pitää paikkansa |
| 21-25 | Koe 5 osuu ilman käyttäjän apua |

Kirjattu mutta kokeilematon yhteys on nolla. Tarkista `yhteydet.md`:n päivämäärät.

Lisäpiste, enintään 3, jos puuttuvat yhteydet on tunnistettu ja lueteltu. Tämä lisätään mihin tahansa bändiin, myös nollan päälle. Käyttäjä, joka tietää tarkalleen mitä puuttuu, on paremmassa asemassa kuin se joka ei tiedä.

**Taidot (0-25).** Osaa tehdä työn vaiheet.

| Pisteet | Tila |
|---|---|
| 0-6 | Vain keskustelua |
| 7-13 | Mukana tulleet komennot käytössä |
| 14-20 | Vähintään yksi oma komento, jota on ajettu useammin kuin kerran |
| 21-25 | Oma komento tuottaa valmiin tuotoksen, ja edellisestä ajosta on merkintä |

Komento, jota ei ole ajettu, ei tuo pisteitä.

**Tahti (0-25).** Toimii ilman pyytämistä.

| Pisteet | Tila |
|---|---|
| 0-6 | Kaikki alkaa siitä että käyttäjä avaa keskustelun |
| 7-13 | Käyttäjällä on säännöllinen rutiini, jonka hän ajaa itse |
| 14-20 | Jokin ajastettu tai toistuva ajo on käynnissä ja siitä on jälki |
| 21-25 | Ajo on tuottanut hyötyä ilman että sitä pyydettiin, useammin kuin kerran |

**Kattosääntö.** Mikään kerros ei voi saada enempää pisteitä kuin Tieto-kerros plus viisi. Jos Tieto on 10, muut ovat enintään 15 kukin. Vertailu tehdään aina Tietoon eikä ketjussa kerrokselta toiselle.

Syy: nopea kone väärällä tiedolla tekee vääriä asioita nopeammin. Katto on siksi kiinni perustassa eikä naapurikerroksessa.

Näytä laskutoimitus. Kerro jokaisesta pisteestä, mihin todisteeseen se nojaa.

## Vaihe 3: kolme korjausta

Nimeä kolme parannusta tärkeysjärjestyksessä. Jokaisesta neljä riviä:

- **Mikä:** yksi lause.
- **Miksi nyt:** mihin löydökseen tämä liittyy.
- **Ensimmäinen askel:** konkreettinen teko, joka vie alle tunnin.
- **Mistä tiedän että se on kunnossa:** mitä pitää pystyä toteamaan seuraavassa ajossa.

Jos yksi kerros on selvästi muita heikompi, kaikki kolme korjausta saavat koskea sitä.

Ehdota lopuksi valmis komento tärkeimmälle korjaukselle. Yleensä `/kehita` tai `/linkita`.

## Vaihe 4: raportti

Tallenna raportti tiedostoon `tarkistukset/VVVV-KK-PP.md`. Jos saman päivän tiedosto on jo olemassa, lisää perään `-2`.

Raportin osat järjestyksessä:

1. Päivämäärä, kokonaispisteet ja neljä osapistettä
2. Hakukokeiden taulukko tuloksineen
3. Todisteet kerroksittain, laskutoimitus näkyvissä
4. Kolme vahvuutta todisteineen
5. Kolme korjausta
6. Vertailu edelliseen raporttiin

Anna jokaiselle löydökselle tunnus muotoa `L1`, `L2`, `L3`. Numeroi ne siinä järjestyksessä kuin ne raportissa esiintyvät. Käytä samaa tunnusta seuraavassa raportissa, jos löydös on yhä auki. Tunnus on se, joka tekee vertailusta mahdollisen, joten anna se heti ensimmäisessä ajossa.

**Vertailu edelliseen.** Lue viimeisin raportti kansiosta. Merkitse jokainen vanha löydös: korjattu, yhä auki, palasi, ei tarkistettu, tai ei enää ajankohtainen.

Korjatuksi merkitseminen vaatii uuden todisteen. Käyttäjän ilmoitus siitä, että hän korjasi asian, ei riitä, jos et pysty toteamaan sitä.

Erottele pistemuutoksen syy: parantuiko järjestelmä, vai löysitkö tällä kertaa paremmat todisteet samasta asiasta. Nämä näyttävät raportissa samalta mutta tarkoittavat eri asiaa.

Kirjoita tiedosto ennen kuin näytät yhteenvedon keskustelussa, ja mainitse yhteenvedon alussa tiedoston polku.

## Rajat

- Älä korjaa mitään tässä ajossa. Tämä komento katsoo ja kirjoittaa raportin. Korjaaminen on `/kehita`.
- Älä anna pisteitä kohteliaisuudesta. Matala luku ensimmäisessä ajossa on normaali ja hyödyllinen.
- Älä vertaa käyttäjää muihin. Ainoa vertailukohta on hänen edellinen raporttinsa.
- Raportit ovat yksityisiä ja gitin ulkopuolella. Ne voivat sisältää asiakastietoa.
