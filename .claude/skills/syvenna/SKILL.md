---
name: syvenna
description: Syventävä haastattelu, joka purkaa käyttäjän pään sisällön tiedostoon. Käytä kun käyttäjä sanoo "syvennä", "haastattele mua", "kysele multa", "auta mua miettimään tätä", "purataan tämä auki", "grillaa mua", tai kun hän haluaa tallentaa suunnitelman, prosessin tai taustatiedon järjestelmään. Kysyy yhden kysymyksen kerrallaan ja tallentaa jokaisen vastauksen heti levylle.
---

# Syventävä haastattelu

`/aloita` kysyi seitsemän kysymystä. Tämä kysyy niin monta kuin tarvitaan, yhdestä aiheesta kerrallaan.

Käyttötapaus: käyttäjän päässä on jotain, mitä järjestelmä ei tiedä. Miten hinnoittelu oikeasti menee. Mikä meni pieleen viime projektissa. Miten uusi palvelu pitäisi rakentaa. Tämä skilli kaivaa sen ulos ja tallentaa.

## Tärkein sääntö

**Tallenna jokainen vastaus levylle heti kun se on annettu.** Ei lopuksi. Ei viiden vastauksen välein. Heti.

Syy on yksinkertainen: keskustelu voi katketa, konteksti voi täyttyä tai käyttäjä voi joutua lähtemään kesken. Tiedosto on totuus, keskustelumuisti ei ole.

Jos kirjoitus epäonnistuu, pysähdy ja kerro se. Älä jatka kysymistä ja älä väitä tallentaneesi.

## Kulku

**1. Kysy aihe.** Jos käyttäjä ei kertonut sitä komennon yhteydessä, kysy yhdellä lauseella mistä puhutaan.

**2. Lue mitä jo tiedetään.** Katso `CLAUDE.md`, `tausta/`-kansio ja aiheeseen liittyvät `haastattelut/`-tiedostot. Älä kysy sitä, mikä on jo kirjattu. Kysy sitä, mikä puuttuu tai on ristiriidassa.

**3. Luo tiedosto ennen ensimmäistä kysymystä.**
Polku: `haastattelut/VVVV-KK-PP-aihe.md`, esimerkiksi `haastattelut/2026-09-08-hinnoittelu.md`. Aihe pienillä kirjaimilla, sanat väliviivoilla, ei ääkkösiä tiedostonimessä.

Jos samana päivänä on jo saman niminen tiedosto, lisää perään `-2`. Älä koskaan korvaa vanhaa.

Tiedoston alkuun otsikko, päivämäärä ja yhden lauseen kuvaus siitä mitä ollaan selvittämässä.

**4. Kysy yksi kysymys.** Yksi. Ei kahta samassa viestissä, ei listaa vaihtoehdoista joihin pitää vastata erikseen.

Hyvä kysymys nojaa edelliseen vastaukseen. Huono kysymys on seuraava kohta valmiissa listassa.

**5. Tallenna vastaus heti.** Lisää tiedoston loppuun:

    ## [Kysymyksen aihe]

    **K:** kysymys sellaisena kuin se esitettiin
    **V:** käyttäjän vastaus sanatarkasti

    **Poimittu:** faktat, jotka tästä jäävät voimaan
    **Auki:** mikä jäi epäselväksi
    **Idea:** mitä käyttäjä pohti ääneen, ei vielä päätetty

Erottele varmat faktat ja keskeneräiset ajatukset. Tämä ero ratkaisee myöhemmin sen, mitä uskalletaan siirtää `tausta/`-kansioon.

Älä siisti käyttäjän sanamuotoja. Puhekieli, keskeneräiset lauseet ja sivupolut säilytetään. Ne ovat ääninäytettä siinä missä tietoakin.

**6. Lue tallennus varmistukseksi.** Lue kirjoittamasi kohta takaisin levyltä ennen seuraavaa kysymystä. Näin virhe huomataan yhden vastauksen kohdalla eikä kymmenen jälkeen.

**7. Jatka kunnes käyttäjä lopettaa.** Hän saa lopettaa milloin vain. Kun hän sanoo stop, tauko, riittää tai vastaava, lopeta heti äläkä kysy varmistusta.

Ehdota itse lopetusta, kun aihe on käyty läpi eikä uusi kysymys enää tuota uutta tietoa.

## Kysymystekniikka

**Mene juuresta latvaan.** Jos hinnoittelu riippuu siitä, kenelle myydään, kysy asiakas ensin. Väärässä järjestyksessä kysytty haastattelu joudutaan käymään uudelleen.

**Kysy esimerkkiä, älä periaatetta.** "Miten hinnoittelet" tuottaa teorian. "Mitä laskutit viimeisimmästä projektista ja miten päädyit siihen" tuottaa totuuden.

**Tartu ristiriitaan.** Jos vastaus on ristiriidassa aiemman kanssa, sano se ääneen ja kysy kumpi pätee. Älä korjaa hiljaa.

**Kysy myös se, mikä ei toiminut.** Epäonnistumiset ovat käyttökelpoisempaa tietoa kuin onnistumiset, ja ne jäävät kirjaamatta jos niitä ei kysy.

**Älä opeta.** Tämä on haastattelu. Jos käyttäjä kysyy mielipidettäsi, anna se lyhyesti ja palaa kysymään.

## Lopetus

Kun haastattelu päättyy:

1. Kirjoita tiedoston loppuun tiivistelmä: mitä nyt tiedetään, mikä jäi auki.
2. Käy läpi poimitut faktat ja kysy käyttäjältä, mitkä niistä siirretään pysyväksi tiedoksi `tausta/`-kansioon.
3. Siirrä vain vahvistetut. Lisää siirretyn kohdan perään päivätty viittaus tähän haastatteluun, jotta alkuperä säilyy.
4. Keskeneräiset ideat jäävät haastattelutiedostoon merkittyinä. Niitä ei siirretä.
5. Jos haastattelussa syntyi päätös, ehdota kirjausta päätöslokiin.

## Rajat

- Yksi kysymys kerrallaan. Aina.
- Ei muutoksia järjestelmiin, sähköpostiin tai kalenteriin. Tämä skilli vain kysyy ja kirjoittaa.
- Ei salasanoja eikä avaimia tiedostoon. Jos käyttäjä liittää sellaisen, jätä se pois tallennuksesta ja kerro miksi.
- Haastattelutiedostot ovat yksityisiä. Ne on jätetty gitin ulkopuolelle. Älä siirrä niitä muualle.
