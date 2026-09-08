---
name: aloita
description: Ensimmäisen päivän alkuhaastattelu. Käytä kun käyttäjä on juuri ottanut tämän kansion käyttöön, sanoo "aloita", "aloitetaan", "ota käyttöön", "täytä pohjat", "kuka mä olen", tai kun haastattelu.md on muuttunut ja pohjat pitää päivittää. Kysyy 7 kysymystä ja täyttää niistä CLAUDE.md:n, tausta-kansion tiedostot ja yhteydet.md:n.
---

# Alkuhaastattelu

Tämä ajetaan kerran ensimmäisenä päivänä. Sen jälkeen aina kun `haastattelu.md` muuttuu.

Lopputulos: käyttäjän tyhjä kansio muuttuu järjestelmäksi, joka tuntee hänet.

## Ennen kuin aloitat

Lue `haastattelu.md`. Jos siinä on jo vastauksia, älä kysy niitä uudelleen. Kysy vain tyhjät kohdat ja kerro heti alussa, mitkä ohitat.

Lue myös `CLAUDE.md`, `tausta/yritys.md`, `tausta/prioriteetit.md`, `tausta/aani.md` ja `yhteydet.md`. Jos niissä on jo sisältöä, tämä on päivitysajo: säilytä se mikä pitää yhä paikkansa ja kysy vain muuttunut.

Kerro käyttäjälle kolme asiaa ennen ensimmäistä kysymystä:
1. Kysymyksiä on seitsemän. Koko homma vie noin puoli tuntia.
2. Kysymys 2 vaatii liittämään omaa tekstiä. Se kannattaa etsiä valmiiksi.
3. Vastaukset menevät tiedostoihin tässä kansiossa, ei mihinkään pilveen.

Kysy samassa yhteydessä, miksi käyttäjä haluaa kutsua sinua. Tämä ei ole yksi seitsemästä kysymyksestä vaan nimen antaminen, ja se tehdään ennen niitä. Tallenna vastaus `haastattelu.md`:n kohtaan "Assistentin nimi". Jos käyttäjä ei keksi nimeä, ehdota kolmea ja anna hänen valita.

## Kysymykset

Yksi kysymys kerrallaan. Odota vastaus ennen seuraavaa. Älä näytä koko listaa etukäteen.

**Tallenna jokainen vastaus heti `haastattelu.md`-tiedostoon, ennen kuin kysyt seuraavan.** Älä odota loppuun. Haastattelu kestää puoli tuntia, ja siinä ajassa ehtii tulla käyttöraja vastaan, puhelu väliin tai koneen sulkeminen. Jos vastaukset ovat levyllä, käyttäjä kirjoittaa `/aloita` uudelleen ja homma jatkuu. Jos ne ovat vain keskustelussa, kaikki alkaa alusta ja käyttäjä lopettaa.

Muut tiedostot kirjoitetaan vasta lopussa, koska ne johdetaan useammasta vastauksesta.

**1. Kuka olet, mitä myyt ja kenelle.**
Kysy nimi, yritys, mitä yritys tekee, kuka on paras asiakas ja mistä hänet tunnistaa. Jos vastaus jää yleiselle tasolle, kuten "autan yrityksiä kasvamaan", kysy yksi tarkentava kysymys: kuka oli viimeisin asiakas ja mitä hän osti.

**2. Näyte omasta kirjoituksesta.**
Pyydä liittämään 1-2 tekstiä, jotka käyttäjä on oikeasti kirjoittanut. Sähköposti asiakkaalle, LinkedIn-postaus, tarjous.

Tämä on ainoa kova sääntö koko haastattelussa: **näytteet on liitettävä sellaisenaan.** Jos käyttäjä alkaa kirjoittaa näytettä tähän keskusteluun, pysäytä ja pyydä liittämään vanha teksti. Keskustelussa kirjoitettu näyte on jo tämän keskustelun muovaama ja silloin ääniprofiilista tulee väärä.

Jos käyttäjä sanoo, ettei löydä mitään, ohjaa katsomaan lähetetyt sähköpostit viimeiseltä kuukaudelta.

**3. Kolme tärkeintä asiaa seuraavalle 90 päivälle.**
Vaadi jokaiseen joko luku tai päivämäärä. Jos vastaus on "kasvattaa myyntiä", kysy paljonko ja mihin mennessä. Tämä on ainoa kohta, jossa painostat.

Kysy kerran ja anna yksi esimerkki. Jos käyttäjä ei silti anna mittaria, älä jää jankkaamaan. Kirjaa tavoite sellaisenaan ja merkitse sen perään `mittari: sopimatta`. Se on rehellinen tulos, ja `/tarkista` nostaa sen esiin viikon päästä. Keksitty mittari olisi pahempi kuin puuttuva, koska se näyttää valmiilta.

**4. Mihin raha oikeasti laskeutuu ja missä sitä seurataan.**
Mitkä kaupat tuovat rahan ja missä tiedostossa tai järjestelmässä sitä katsotaan. Jos vastaus on "päässä", kirjaa se sellaisenaan.

Tämä vastaus jakautuu kahtia. Itse asia menee tiedostoon `tausta/prioriteetit.md`. Jos käyttäjä nimeää järjestelmän, kuten kirjanpito-ohjelman tai taulukon, se menee lisäksi tiedostoon `yhteydet.md` kohtaan "Ei kytketty". Sama järjestelmä saa siis esiintyä molemmissa, mutta eri roolissa: toisessa se on rahan mittari ja toisessa tavoittamaton järjestelmä.

**5. Missä puhut asiakkaille, tiimille ja ulkomaailmalle.**
Sähköposti, WhatsApp, Teams, Slack, LinkedIn, puhelin. Kysy myös, mikä kalenteri on käytössä.

**6. Missä tiedostot, muistiinpanot ja tärkeät dokumentit ovat.**
Drive, OneDrive, kovalevy, Notion, sähköpostin liitteet, vihko. Pyydä totuutta, ei tavoitetilaa.

**7. Mikä tehtävä syö viikkosi ja missä seuraat tekemistä.**
Se toistuva homma, josta käyttäjä ei pidä, ja se paikka, josta hän katsoo, mitä on tekemättä. Kysy arvio: montako tuntia viikossa se vie.

## Mitä kirjoitat

Kun kaikki seitsemän on vastattu, tee nämä tässä järjestyksessä.

**1. `haastattelu.md`.** Tämä on jo täytetty haastattelun aikana. Tarkista, että kaikki seitsemän vastausta ovat tallessa oikeiden kysymysten alla ja sanatarkasti. Tämä on lähde, josta kaikki muu johdetaan. Älä siisti käyttäjän sanamuotoja.

**2. `tausta/yritys.md`.** Kysymyksestä 1. Täytä mitä teemme, kenelle, mitä myymme ja asiakkaat nyt.

Kaksi kohtaa jää tyhjäksi, koska haastattelu ei niitä kysy: hintasarake ja "Mitä emme tee". Jätä ne tyhjiksi äläkä arvaa niihin mitään. Mainitse lopetuksessa, että ne kannattaa täyttää käsin kun ehtii.

**3. `tausta/prioriteetit.md`.** Kysymyksistä 3, 4 ja 7. Kolme tavoitetta mittareineen, rahan laskeutumispaikka ja viikon aikasyöppö tunteineen.

Jakso alkaa tästä päivästä ja kestää 90 päivää, ellei käyttäjä sano toisin. Laske loppupäivä ja kirjoita molemmat näkyviin.

Jokaisen tavoitteen "Tilanne"-kenttään kirjoitetaan `ei vielä kirjattu`, ellei käyttäjä kertonut tilannetta itse. Kenttä täyttyy viikoittaisessa käytössä. Älä arvaa siihen mitään.

**4. `tausta/aani.md`.** Kysymyksestä 2. Liitä näytteet sellaisenaan. Kirjoita sen jälkeen "Mitä näytteistä huomaa" -osioon havainnot: sinuttelu vai teitittely, puhekieli vai kirjakieli, lauseiden pituus, aloitus- ja lopetustapa, toistuvat sanat. Kirjoita havainnot, älä sääntöjä. Jos näytteessä on puhekielinen kirjoitusasu, merkitse, että se on ääntä eikä virhe.

**5. `yhteydet.md`.** Kysymyksistä 5, 6 ja 7, sekä kysymyksestä 4 siltä osin kuin siinä nimettiin järjestelmä. Kaikki mainitut järjestelmät menevät aluksi "Ei kytketty" -taulukkoon, koska mitään ei ole vielä kokeiltu. Kalenteri johdetaan kysymyksestä 5.

**6. `CLAUDE.md`.** Korvaa hakasulkeissa olevat paikanvaraajat: `[YRITYKSEN NIMI]`, `[ETUNIMI]` ja `[ASSISTENTIN NIMI]`. Assistentin nimi on `haastattelu.md`:ssä omana kohtanaan. Poista rivi, jossa lukee että tiedosto on tyhjä pohja.

Taivuta nimet oikein. Pohjassa lukee `[ETUNIMI]n` ja `[ETUNIMI]a`, mutta suora korvaus tuottaa väärän muodon konsonanttiin päättyvillä nimillä. Petri taipuu muotoon Petrin ja Petriä, Markus muotoon Markuksen ja Markusta. Lue lause läpi ennen kuin jätät sen.

Älä lisää CLAUDE.md-tiedostoon faktoja yrityksestä. Ne kuuluvat `tausta/`-kansioon ja CLAUDE.md vain osoittaa sinne.

## Lopetus

Näytä lyhyt lista siitä mitä kirjoitettiin, tiedosto per rivi. Kerro samalla, jos jokin kohta jäi tyhjäksi ja miksi.

Kerro sitten mitä tapahtuu seuraavaksi:
- Käytä järjestelmää viikko oikeisiin kysymyksiin.
- Kun teet päätöksen, pyydä kirjaamaan se päätöslokiin.
- Päivänä 7 kirjoita `/tarkista`.
- Päivänä 14 kirjoita `/kehita`.

Ehdota lopuksi ensimmäistä kysymystä, jonka käyttäjä voi kokeilla heti:

> "Mihin mun kannattaa keskittyä tällä viikolla?"

Tämä kysymys on tarkoituksella sellainen, että vastaus on hyvä vain jos haastattelu meni hyvin. Se on samalla ensimmäinen näyttö ja ensimmäinen testi.

## Rajat

- Älä kysy enempää kuin seitsemän kysymystä. Tarkentavaa jatkokysymystä ei lasketa mukaan, mutta kahdeksatta aihetta ei oteta.
- Älä täytä tyhjää kohtaa arvaamalla. Tyhjä kenttä on parempi kuin keksitty, koska `/tarkista` löytää tyhjän mutta ei keksittyä.
- Älä kirjoita mitään tämän kansion ulkopuolelle.
- Älä pyydä salasanoja, avaimia äläkä tunnuksia. Jos käyttäjä liittää sellaisen, älä tallenna sitä tiedostoon vaan kerro, että se kuuluu `.env`-tiedostoon.
