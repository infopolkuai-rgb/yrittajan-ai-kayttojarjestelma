---
name: linkita
description: Lisää uuden kansion, projektin, tiedoston tai lähteen assistentin löydettäväksi. Käytä kun käyttäjä sanoo "linkitä", "lisää tämä", "ota tämä kansio mukaan", "muista tämä paikka", "miksi et löydä tätä", tai kun uusi projekti tai lähde otetaan käyttöön. Lisää CLAUDE.md:hen yhden reittirivin ja tarkistaa että polku toimii.
---

# Linkitä

Assistentti löytää vain sen, mihin on reitti. Uusi kansio kovalevyllä ei ole olemassa ennen kuin se on kirjattu.

Tämä skilli lisää yhden rivin `CLAUDE.md`-tiedostoon ja varmistaa että se toimii. Pieni homma, mutta ilman sitä järjestelmä alkaa unohtaa asioita sitä mukaa kun se kasvaa.

## Kulku

**1. Selvitä kohde ja käyttötarkoitus.**
Tarvitset kaksi asiaa. Polun tai osoitteen ja yhden lauseen siitä, milloin tätä käytetään.

Jos käyttäjä antoi vain polun, kysy käyttötarkoitus. Jos hän antoi vain kuvauksen, kysy polku. Älä arvaa kumpaakaan.

**2. Tarkista että kohde on olemassa.**
Paikallinen polku: katso, että se löytyy. Jos ei löydy, kysy tarkoittiko käyttäjä jotain muuta. Älä lisää rikkinäistä reittiä.

Verkko-osoite: merkitse se varmistamattomaksi, jos et pääse sitä avaamaan. Reitin saa silti lisätä. Merkintä kertoo myöhemmin, ettei osoitetta ole testattu.

**3. Katso löytyykö reitti jo.**
Lue `CLAUDE.md` ja "Missä mikäkin on" -taulukko. Jos kohde löytyy jo jonkin olemassa olevan rivin kautta, älä lisää mitään. Kerro käyttäjälle mitä riviä pitkin se löytyy. Kahdesta reitistä samaan paikkaan tulee myöhemmin kaksi eri totuutta.

**4. Lisää yksi rivi.**
Rivi menee `CLAUDE.md`:n "Missä mikäkin on" -taulukkoon. Vasempaan sarakkeeseen polku, oikeaan yksi lause siitä, milloin sinne mennään ja mistä tiedostosta aloitetaan.

Esimerkki:

    | `projektit/lampokarhu/` | Lämpökarhun projekti. Aloita tiedostosta tilanne.md |

Käytä suhteellista polkua, jos kohde on tämän kansion sisällä. Käytä täyttä polkua tai osoitetta, jos se on ulkopuolella.

Pidä rivi lyhyenä. Reitti kertoo minne mennään, ei sitä mitä siellä on. CLAUDE.md luetaan joka ajossa ja jokainen turha sana maksaa.

**5. Jos kohde on iso kansio, tee sille oma sisällysluettelo.**
Kun kansiossa on yli viisi tiedostoa, älä listaa niitä CLAUDE.md:hen. Tee kansioon `README.md`, joka kertoo mistä aloittaa, ja osoita CLAUDE.md-rivi siihen. Näin pääohje pysyy lyhyenä.

**6. Tarkista koko ketju.**
Kulje reitti läpi niin kuin assistentti kulkisi: CLAUDE.md → rivi → polku → aloitustiedosto. Jos jokin lenkki ei aukea, korjaa se nyt.

Kerro käyttäjälle lopuksi yhdellä rivillä mitä lisättiin ja mihin.

## Rajat

- Yksi reitti per ajo. Jos käyttäjä haluaa lisätä viisi kohdetta, tee ne yksi kerrallaan ja tarkista jokainen erikseen.
- Älä siivoa muuta samalla. Jos huomaat rikkinäisen vanhan rivin, mainitse se mutta älä korjaa ilman lupaa.
- Älä siirrä äläkä kopioi tiedostoja. Tämä skilli kirjoittaa reitin, ei liikuta tavaraa.
- Älä lisää CLAUDE.md-tiedostoon salasanoja, avaimia äläkä yksityisiä osoitteita, joissa on tunnus mukana. Reitti voi osoittaa `.env`-tiedostoon, mutta sisältö pysyy siellä.
- Älä lisää kohdetta, jota et pystynyt tarkistamaan, ilman että merkitset sen varmistamattomaksi.
