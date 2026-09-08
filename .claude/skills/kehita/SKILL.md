---
name: kehita
description: Viikoittainen kehitysajo, joka vie yhden parannuksen maaliin. Käytä kun käyttäjä sanoo "kehitä", "paranna", "mitä automatisoidaan", "viikkopalaveri", "mitä seuraavaksi rakennetaan", tai päivänä 14 ja sen jälkeen viikoittain. Haastattelee Kolmen A:n mukaan ja rakentaa yhden asian valmiiksi.
---

# Kehitä

Yksi ajo, yksi valmis parannus. Ei kolmea puolivalmista.

Tämä on se skilli, joka opettaa työskentelymallin käyttöön. Haastattelu ei ole muodollisuus: sen kysymykset ovat samat, jotka käyttäjän kannattaa oppia kysymään itseltään.

Lue ensin `ohjeet/tyoskentelymalli.md`. Lue myös viimeisin raportti kansiosta `tarkistukset/`, tiedosto `paatokset/loki.md` ja `tausta/prioriteetit.md`:n kohta "Viikon aikasyöppö".

## Vaihe 1: Asenne

Tavoite: löytää oikea kohde. Kolme kysymystä, yksi kerrallaan.

**1. Mikä vei viime viikolla eniten aikaa tai ärsytti eniten?**
Jos `tausta/prioriteetit.md`:ssä on merkintä viikon aikasyöpöstä, ehdota sitä ja kysy pitääkö se yhä paikkansa. Jos vastaus on ympäripyöreä, kysy, mitä käyttäjä teki eilen. Konkreettinen päivä tuottaa paremman vastauksen kuin abstrakti viikko.

**2. Pilkotaan se osiin. Mitä siinä oikeasti tapahtuu vaihe vaiheelta?**
Kirjoita vaiheet näkyviin. Tässä paljastuu yleensä, että tehtävä on viisi tehtävää.

**3. Käydään vaiheet läpi: missä määrin tekoäly voi hoitaa tämän?**
Jokaisesta vaiheesta erikseen. Vastaus on liukuma, ei kyllä tai ei.

Jos edellinen tarkistus nosti esiin selvän aukon, ehdota sitä kohteeksi. Käyttäjä saa silti valita toisin. Hänen tuntemansa kipu voittaa raportin.

## Vaihe 2: Askeleet

Tavoite: rajata työ niin pieneksi, että se valmistuu tänään.

**1. Onko tämä oikea pullonkaula?** Jos tämä poistuisi, vapautuisiko oikeasti aikaa vai siirtyisikö jono vain eteenpäin?

**2. Poista, automatisoi vai delegoi?** Kysy tässä järjestyksessä. Yllättävän usein vastaus on ensimmäinen. Jos työ voidaan lopettaa, se on paras mahdollinen lopputulos ja ajo päättyy tähän. Kirjaa päätös lokiin.

**3. Kuvaa prosessi.** Mitä tapahtuu ensin, mitä sitten ja mistä tiedetään, että se meni oikein. Jos käyttäjä ei osaa kuvata sitä, homma ei ole vielä valmis automatisoitavaksi. Silloin tämän ajon tuotos on prosessikuvaus. Sekin on hyvä tuotos.

**4. Valitse itsenäisyyden taso.** Aloita tasolta 1 tai 2. Jos käyttäjä haluaa suoraan tasolle 4, kysy, mitä tapahtuu kun kone tekee virheen ja kuka sen huomaa.

**5. Mihin lukuun tämä sidotaan?** Vaadi luku tai päivämäärä. Kirjaa lähtötilanne nyt, muuten vertailukohtaa ei ole ensi kuussa.

## Vaihe 3: Automaatio

Tavoite: rakentaa se. Tässä vaiheessa lopetetaan kysyminen ja aletaan tehdä.

Rakenna pieninä paloina. Lisää tarkistus jokaisen vaiheen jälkeen. Kirjoita ohjeet niin kuin kirjoittaisit uudelle harjoittelijalle: mitä tehdään, kenelle, miltä hyvä lopputulos näyttää, mitä ei saa tehdä.

Varmista, että käyttäjä pystyy pysäyttämään sen yhdellä liikkeellä. Kerro myös miten.

Tuotos on yleensä yksi näistä:
- **Kokeiltu yhteys.** Otetaan jokin järjestelmä ulottuville, kokeillaan se oikealla kysymyksellä ja kirjataan tulos päivämäärineen `yhteydet.md`:hen. Tämä on tavallisin tuotos silloin, kun Työkalut-kerros on heikoin.
- **Uusi komento** kansioon `.claude/skills/[nimi]/SKILL.md`.
- **Korjaus olemassa olevaan.** Tämä on täysin kelvollinen tulos. Toimiva vanha komento on parempi kuin uusi rikkinäinen.
- **Uusi tausta- tai ohjetiedosto** ja reitti siihen. Aja `/linkita`.
- **Prosessikuvaus** silloin kun rakentaminen olisi ennenaikaista.

**Aja se kerran oikealla datalla ennen kuin sanot sen valmiiksi.** Kokeilematon tuotos ei ole tuotos. Jos ajo epäonnistuu, korjaa nyt. Tämä on se kohta, jossa useimmat kehitysajot menevät pieleen: valmiiksi julistetaan jotain, jota ei ole kertaakaan kokeiltu.

## Lopetus

1. Näytä mitä syntyi ja missä se on.
2. Kirjaa päätös `paatokset/loki.md`-tiedostoon: mitä rakennettiin, miksi, mikä hylättiin, mistä tiedetään toimiiko.
3. Kerro, mikä luku muuttuu jos tämä toimii, ja milloin sitä katsotaan.
4. Muistuta ajamaan `/tarkista` seuraavan kerran, jotta parannus näkyy todisteena.
5. Jos ajon aikana nousi toinen hyvä idea, kirjaa se lokiin odottamaan. Älä rakenna sitä nyt.

## Rajat

- **Yksi asia per ajo.** Tämä on koko skillin idea. Jos käyttäjä haluaa kolme, valitse tärkein ja kirjaa kaksi muuta odottamaan.
- **Älä hyppää suoraan vaiheeseen 3.** Haastattelu ennen rakentamista on se osa, joka opettaa. Ilman sitä tämä on pelkkä koodipyyntö.
- **Älä nosta itsenäisyystasoa ilman ajohistoriaa.** Taso 4 vaatii kuukauden tasolla 3.
- **Älä rakenna sitä, mikä on jo olemassa.** Katso ensin, ratkaiseeko olemassa oleva komento tämän korjattuna.
- **Älä lupaa lukuja.** Kirjaa lähtötilanne ja mittaa ensi kerralla.
