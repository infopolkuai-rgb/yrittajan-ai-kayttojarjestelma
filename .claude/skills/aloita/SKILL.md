---
name: aloita
description: Ensimmäisen päivän alkuhaastattelu. Käytä kun käyttäjä on juuri ottanut tämän kansion käyttöön, sanoo "aloita", "aloitetaan", "ota käyttöön", "täytä pohjat", "kuka mä olen", tai kun haastattelu.md on muuttunut ja pohjat pitää päivittää. Kysyy 7 kysymystä ja täyttää niistä CLAUDE.md:n, tausta-kansion tiedostot ja yhteydet.md:n.
---

# Alkuhaastattelu

Tämä ajetaan kerran ensimmäisenä päivänä. Sen jälkeen aina kun `haastattelu.md` muuttuu.

Lopputulos: käyttäjän tyhjä kansio muuttuu järjestelmäksi, joka tuntee hänet. Tavoiteaika 15 minuuttia.

## Ennen kuin aloitat

Lue `haastattelu.md`. Jos siinä on jo vastauksia, älä kysy niitä uudelleen. Kysy vain tyhjät kohdat ja kerro heti alussa mitkä ohitat.

Lue myös `CLAUDE.md`, `tausta/yritys.md`, `tausta/prioriteetit.md`, `tausta/aani.md` ja `yhteydet.md`. Jos niissä on jo sisältöä, tämä on päivitysajo: säilytä se mikä pitää yhä paikkansa ja kysy vain muuttunut.

Kerro käyttäjälle kolme asiaa ennen ensimmäistä kysymystä:
1. Kysymyksiä on seitsemän ja ne kestävät noin viisitoista minuuttia.
2. Kysymys 2 vaatii liittämään omaa tekstiä. Se kannattaa etsiä valmiiksi.
3. Vastaukset menevät tiedostoihin tässä kansiossa, ei mihinkään pilveen.

## Kysymykset

Yksi kysymys kerrallaan. Odota vastaus ennen seuraavaa. Älä näytä koko listaa etukäteen.

**1. Kuka olet, mitä myyt ja kenelle.**
Kysy nimi, yritys, mitä yritys tekee, kuka on paras asiakas ja mistä hänet tunnistaa. Jos vastaus jää yleiselle tasolle ("autan yrityksiä kasvamaan"), kysy yksi tarkentava kysymys: kuka oli viimeisin asiakas ja mitä hän osti.

**2. Näyte omasta kirjoituksesta.**
Pyydä liittämään 1-2 tekstiä, jotka käyttäjä on oikeasti kirjoittanut. Sähköposti asiakkaalle, LinkedIn-postaus, tarjous.

Tämä on ainoa kova sääntö koko haastattelussa: **näytteet on liitettävä sellaisenaan.** Jos käyttäjä alkaa kirjoittaa näytettä tähän keskusteluun, pysäytä ja pyydä liittämään vanha teksti. Keskustelussa kirjoitettu näyte on jo tämän keskustelun muovaama, ja silloin ääniprofiilista tulee väärä.

Jos käyttäjä sanoo ettei löydä mitään, ohjaa katsomaan lähetetyt sähköpostit viimeiseltä kuukaudelta.

**3. Kolme tärkeintä asiaa seuraavalle 90 päivälle.**
Vaadi jokaiseen joko luku tai päivämäärä. Jos vastaus on "kasvattaa myyntiä", kysy paljonko ja mihin mennessä. Älä hyväksy kolmea ilman mittaria. Tämä on ainoa kohta, jossa painostat.

**4. Mihin raha oikeasti laskeutuu ja missä sitä seurataan.**
Mitkä kaupat tuovat rahan ja missä tiedostossa tai järjestelmässä sitä katsotaan. Jos vastaus on "päässä", kirjaa se sellaisenaan. Se on rehellinen vastaus ja `/tarkista` nostaa sen esiin myöhemmin.

**5. Missä puhut asiakkaille, tiimille ja ulkomaailmalle.**
Sähköposti, WhatsApp, Teams, Slack, LinkedIn, puhelin. Kysy myös mikä kalenteri on käytössä.

**6. Missä tiedostot, muistiinpanot ja tärkeät dokumentit ovat.**
Drive, OneDrive, kovalevy, Notion, sähköpostin liitteet, vihko. Pyydä totuutta, ei tavoitetilaa.

**7. Mikä tehtävä syö viikkosi ja missä seuraat tekemistä.**
Se toistuva homma josta käyttäjä ei pidä, ja se paikka josta hän katsoo mitä on tekemättä. Kysy arvio: montako tuntia viikossa se vie.

## Mitä kirjoitat

Kun kaikki seitsemän on vastattu, tee nämä tässä järjestyksessä.

**1. `haastattelu.md`** — tallenna vastaukset sanatarkasti oikeiden kysymysten alle. Tämä on lähde, josta kaikki muu johdetaan. Älä siisti käyttäjän sanamuotoja.

**2. `tausta/yritys.md`** — kysymyksestä 1. Täytä mitä teemme, kenelle, mitä myymme ja asiakkaat nyt. Jätä "mitä emme tee" tyhjäksi, jos käyttäjä ei maininnut rajoja.

**3. `tausta/prioriteetit.md`** — kysymyksistä 3 ja 4. Kolme tavoitetta mittareineen ja rahan laskeutumispaikka. Merkitse jakson alku- ja loppupäivä.

**4. `tausta/aani.md`** — kysymyksestä 2. Liitä näytteet sellaisenaan. Kirjoita sen jälkeen "Mitä näytteistä huomaa" -osioon havainnot: sinuttelu vai teitittely, puhekieli vai kirjakieli, lauseiden pituus, aloitus- ja lopetustapa, toistuvat sanat. Kirjoita havainnot, älä sääntöjä. Jos näytteessä on puhekielinen kirjoitusasu, merkitse että se on ääntä eikä virhe.

**5. `yhteydet.md`** — kysymyksistä 5, 6 ja 7. Kaikki mainitut järjestelmät menevät aluksi "Ei kytketty" -taulukkoon, koska mitään ei ole vielä kokeiltu. Kalenteri johdetaan kysymyksestä 5, vaikka sitä ei erikseen kysytty.

**6. `CLAUDE.md`** — korvaa hakasulkeissa olevat paikanvaraajat. `[YRITYKSEN NIMI]`, `[ETUNIMI]` ja `[ASSISTENTIN NIMI]`. Kysy assistentin nimi käyttäjältä, jos hän ei ole sitä maininnut. Poista rivi, jossa lukee että tiedosto on tyhjä pohja.

Älä lisää CLAUDE.md-tiedostoon faktoja yrityksestä. Ne kuuluvat `tausta/`-kansioon ja CLAUDE.md vain osoittaa sinne.

## Lopetus

Näytä lyhyt lista siitä mitä kirjoitettiin, tiedosto per rivi.

Kerro sitten mitä tapahtuu seuraavaksi:
- Käytä järjestelmää viikko oikeisiin kysymyksiin.
- Kun teet päätöksen, pyydä kirjaamaan se päätöslokiin.
- Päivänä 7 aja `/tarkista`.
- Päivänä 14 aja `/kehita`.

Ehdota lopuksi ensimmäistä kysymystä, jonka käyttäjä voi kokeilla heti:

> "Mihin mun kannattaa keskittyä tällä viikolla?"

Tämä kysymys on tarkoituksella sellainen, että vastaus on hyvä vain jos haastattelu meni hyvin. Se on samalla ensimmäinen näyttö ja ensimmäinen testi.

## Rajat

- Älä kysy enempää kuin seitsemän kysymystä. Tarkentava jatkokysymys ei laske omakseen, mutta kahdeksatta aihetta ei oteta.
- Älä täytä tyhjää kohtaa arvaamalla. Tyhjä kenttä on parempi kuin keksitty, koska `/tarkista` löytää tyhjän mutta ei keksittyä.
- Älä kirjoita mitään tämän kansion ulkopuolelle.
- Älä pyydä salasanoja, avaimia äläkä tunnuksia. Jos käyttäjä liittää sellaisen, älä tallenna sitä tiedostoon vaan kerro että se kuuluu `.env`-tiedostoon.
