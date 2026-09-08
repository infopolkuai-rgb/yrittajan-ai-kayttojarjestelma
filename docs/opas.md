# Yrittäjän AI-käyttöjärjestelmä

Opas alusta loppuun. Lue tämä kerran läpi, sitten tee mitä siinä sanotaan.

Jos jokin kohta tökkää, luku 4 on nimeltään "Jos jokin ei toimi". Siellä on ne neljä tavallisinta ongelmaa. Ja jos sekään ei auta, mun sähköposti on lopussa. Vastaan samana päivänä.

---

## 1. Mistä tässä on kyse

Sä käytät varmaan jo tekoälyä. Avaat keskustelun, selität tilanteen, saat vastauksen. Seuraavana päivänä avaat uuden keskustelun ja selität saman tilanteen uudestaan.

Se selittäminen on se ongelma. Se maksaa muutaman minuutin joka kerta ja tekee vastauksista yleisiä.

Tämä paketti korjaa sen. Se on kansio tekstitiedostoja, joissa lukee kuka sä olet, mitä sä myyt, kenelle ja millä tyylillä sä kirjoitat. Assistentti lukee ne joka kerta automaattisesti. Sun ei tarvitse selittää enää.

Sen lisäksi mukana tulee viisi valmista komentoa. Komento tarkoittaa tässä sanaa, joka alkaa kauttaviivalla. Kirjoitat sen tavalliseen viestikenttään ja painat enter, aivan kuten minkä tahansa viestin. Sen jälkeen assistentti vie monivaiheisen homman läpi ilman että sä ohjaat sitä joka välissä.

**Mitä tämä ei ole.** Tämä ei ole ohjelma eikä sovellus. Tässä ei ole omia tunnuksia eikä pilvipalvelua. Tämä on kansio, jonka jokaisen tiedoston sä voit avata ja lukea.

**Mitä sä saat.** Assistentin, joka vastaa kysymyksiin sun firmasta ilman että taustoitat ne joka kerta. Kirjoitusapu kuulostaa sulta eikä markkinointiesitteeltä. Päätökset ja niiden perustelut säilyvät yhdessä paikassa.

**Mihin tämä perustuu.** Toimiva järjestelmä koostuu neljästä kerroksesta. Ne ovat **Tieto** eli se tuntee sun firman, **Työkalut** eli se yltää sinne missä sun tieto on, **Taidot** eli se osaa tehdä sun työsi vaiheet ja **Tahti** eli se toimii ilman että pyydät. Tieto on aina ensin ja Tahti aina viimeisenä. Kaksi ensimmäistä syntyvät tämän oppaan aikana, kaksi jälkimmäistä myöhemmin jos haluat.

Neljä kerrosta ja niiden takana oleva ajattelutapa on avattu tiedostossa `ohjeet/tyoskentelymalli.md`. Sitä ei tarvitse lukea nyt.

---

## 2. Mitä sä tarvitset

**Claude Pro -tilaus, 20 dollaria kuussa.** Se on noin 19 euroa. Ilmaisversio ei riitä, koska se ei pääse käsiksi kansioihin. Pro riittää, kalliimpaa Max-tilausta ei tarvita.

Jos sulla on jo tili, tarkista tilaustaso osoitteesta claude.ai. Klikkaa nimeäsi vasemmassa alakulmassa ja katso mitä siinä lukee. Jos lukee Free, tilaus pitää päivittää.

**Claude-työpöytäsovellus.** Windowsille tai Macille. Lataa osoitteesta claude.ai/download. Selain ei käy, koska se ei näe sun koneen kansioita.

**Aikaa näin paljon:**

| Vaihe | Kesto |
|---|---|
| Lataus ja asennus | noin 15 min |
| Alkuhaastattelu | 20-30 min |
| Tottuminen | pari viikkoa |

Varaa asennukselle ja haastattelulle yksi tunti yhdellä istumalla. Se kolmas rivi ei ole työtä vaan tavan muuttumista. Siitä lisää luvussa 6.

**Kaksi omaa tekstiä.** Sähköposti asiakkaalle, LinkedIn-postaus, tarjous. Mikä tahansa, minkä sä olet oikeasti itse kirjoittanut. Etsi ne valmiiksi ennen kuin aloitat. Lähetetyt-kansio on paras paikka.

Ohjelmointitaitoa ei tarvita. Komentoriviä ei tarvita.

---

## 3. Asennus

### Vaihe 1. Lataa kansio

Mene siihen GitHub-osoitteeseen, jonka sait linkkinä.

GitHub on paikka, jossa tiedostoja jaetaan. Sivu näyttää tekniseltä ja siinä on paljon englanninkielisiä välilehtiä. Älä välitä niistä. Sä tarvitset yhden painikkeen.

Etsi sivun oikeasta yläreunasta **vihreä Code-painike**. Klikkaa sitä. Aukeaa pieni valikko, jonka alimpana kohtana lukee **Download ZIP**. Klikkaa sitä. Tiedosto latautuu Lataukset-kansioosi.

### Vaihe 2. Pura zip

Windowsissa: oikea klikkaus tiedoston päällä, valitse "Pura kaikki". Macissa: tuplaklikkaus riittää.

**Katso mitä sisälle jäi.** Purkaminen tekee usein kansion, jonka sisällä on toinen samanniminen kansio. Avaa kansiota niin kauan, että näet suoraan edessäsi tiedostot `README.md` ja `CLAUDE.md`. **Se kansio, jossa nuo kaksi tiedostoa ovat, on oikea kansio.** Sitä sä tarvitset seuraavassa vaiheessa.

Siirrä se paikkaan, jonka muistat. Tiedostot-kansio tai työpöytä käy hyvin.

Kansion saa nimetä uudelleen milloin vain, mikään ei mene siitä rikki. Sisällä olevien tiedostojen nimiä ei kannata muuttaa.

Älä laita kansiota OneDriveen tai Dropboxiin. Synkronointi ja tiedostojen muokkaus tekevät joskus yhdessä tyhmyyksiä.

### Vaihe 3. Avaa kansio Claudessa

Avaa Claude-työpöytäsovellus ja kirjaudu sisään.

Etsi **Code**-välilehti. Valitse sieltä se kansio, jonka löysit vaiheessa 2.

Claude kysyy tässä kohtaa todennäköisesti lupaa lukea kansion tiedostoja tai tehdä niihin muutoksia. Vastaa kyllä. Se on normaalia eikä se anna pääsyä muualle koneellesi.

### Vaihe 4. Tarkista että se toimii

Kirjoita viestikenttään:

> Mitä tiedostoja tässä kansiossa on?

Jos vastaus luettelee tiedostoja, kuten README, CLAUDE ja haastattelu, kaikki on kunnossa. Siirry lukuun 5.

Jos vastaus on jotain muuta, lue seuraava luku.

---

## 4. Jos jokin ei toimi

Neljä tavallisinta ongelmaa ja mitä niille tehdään.

**En löydä Code-välilehteä.**
Yleensä syy on tilaus. Tarkista claude.ai-sivulta, että tilaus on Pro eikä Free. Jos tilaus on kunnossa, sulje sovellus kokonaan ja avaa uudelleen. Jos se ei auta, päivitä sovellus uusimpaan versioon lataamalla se uudestaan osoitteesta claude.ai/download.

**Valitsin kansion mutta Claude ei näe mitään tiedostoja.**
Melkein aina kyse on siitä sisäkkäisestä kansiosta. Sulje kansio, avaa se uudelleen ja varmista, että valitsemasi kansion sisällä näkyvät suoraan tiedostot `README.md` ja `CLAUDE.md`. Jos siellä näkyy vain yksi kansio, mene sen sisään ja valitse se.

**Claude kysyy jotain lupaa enkä tiedä mitä vastata.**
Vastaa kyllä. Kysymys koskee vain tätä kansiota.

**Kirjoitin `/aloita` eikä mitään tapahtunut.**
Kirjoita se ilman lainausmerkkejä ja ilman välilyöntiä kauttaviivan jälkeen, sitten enter. Jos assistentti vastaa tavallisella keskustelulla eikä ala kysellä, kirjoita sen sijaan: *"lue tiedosto .claude/skills/aloita/SKILL.md ja toimi sen mukaan"*. Se tekee saman asian.

**Jos mikään näistä ei auta,** laita mulle sähköpostia osoitteeseen ilmari@polkuai.com. Kerro missä kohtaa jumitit ja mitä ruudulla luki. Vastaan samana päivänä. Ei tarvitse osata mitään, kysymys ei ole tyhmä.

---

## 5. Ensimmäinen ajo

Kirjoita viestikenttään:

> /aloita

Assistentti kysyy seitsemän kysymystä yksi kerrallaan. Ne ovat nämä:

1. Kuka olet, mitä myyt ja kenelle
2. Näyte omasta kirjoituksestasi
3. Kolme tärkeintä asiaa seuraavalle 90 päivälle
4. Mihin raha oikeasti laskeutuu ja missä sitä seurataan
5. Missä puhut asiakkaille, tiimille ja ulkomaailmalle
6. Missä tiedostot ja muistiinpanot ovat
7. Mikä tehtävä syö viikkosi

Vastaa rehellisesti, älä kauniisti. Tämä ei ole hakemus vaan asetustiedosto. Jos jokin asia on sekaisin, kirjoita että se on sekaisin.

Kolme kohtaa, joissa kannattaa hidastaa:

**Kysymys 2 haluaa oikeaa tekstiä.** Liitä ne kaksi tekstiä, jotka etsit valmiiksi. Liitä ne sellaisenaan. Älä siisti äläkä kirjoita uutta.

Syy: jos sä kirjoitat näytteen tähän keskusteluun, sä kirjoitat sen huolellisemmin kuin normaalisti. Silloin assistentti oppii sellaisen tyylin, jolla sä et oikeasti kirjoita, ja jokainen sen luonnos kuulostaa vieraalta.

**Kysymys 3 vaatii numeron.** "Kasvattaa myyntiä" ei kelpaa. "Kolme uutta asiakasta lokakuun loppuun mennessä" kelpaa. Assistentti painostaa tässä kohtaa, ja niin sen kuuluukin tehdä. Ilman lukua se ei voi myöhemmin kertoa, meneekö hyvin.

**Kysymys 6 haluaa totuuden.** Jos tiedostot ovat kolmessa paikassa ja osa työpöydällä, sano se. Tavoitetilan kertominen tässä kohtaa kostautuu heti.

Haastattelun päätteeksi assistentti täyttää tiedostot ja kertoo mitä se kirjoitti. Käy lista läpi silmämääräisesti. Jos jokin meni väärin, sano se, niin se korjaa.

**Kokeile heti tätä:**

> Mihin mun kannattaa keskittyä tällä viikolla?

Vastauksen laatu kertoo, miten haastattelu meni. Jos vastaus on yleistä jaarittelua, jokin kohta jäi ohueksi. Sano assistentille mikä kohta, niin se kysyy siitä lisää.

---

## 6. Ensimmäinen viikko

Älä rakenna mitään. Käytä.

Tuo assistentille oikeita kysymyksiä. Asiakkaan sähköposti, johon pitää vastata. Tarjous, jota mietit. Hinnoittelupulma. Kalenteri, joka on täynnä vääriä asioita.

Kolme tapaa, jotka kannattaa ottaa käyttöön heti:

**Pyydä kirjaamaan päätökset.** Kun sä päätät jotain, sano: *"kirjaa tämä päätöslokiin"*. Puolen vuoden päästä sä muistat mitä päätit mutta et miksi. Silloin sama keskustelu alkaa alusta.

**Kysy ennen kuin teet käsin.** Kun eteesi tulee uusi homma, kysy: *"missä määrin tekoäly voi hoitaa tämän?"* Vastaus on yllättävän usein "suurimman osan".

**Pura asioita päästäsi.** Kun jokin iso asia on selvittämättä, kirjoita `/syvenna`. Se haastattelee sut aiheesta ja tallentaa jokaisen vastauksen. Hyviä aiheita: miten hinnoittelu oikeasti menee, mitä viime projektissa opittiin, miten uusi palvelu pitäisi rakentaa.

Ensimmäisellä viikolla sä olet todennäköisesti hitaampi kuin ennen. Se on normaalia. Kankeus menee ohi noin kahdessa viikossa. Useimmat lopettavat sitä ennen.

---

## 7. Päivä 7 ja päivä 14

**Päivänä 7 kirjoita `/tarkista`.**

Se testaa viidellä kysymyksellä, löytääkö järjestelmä oman tietonsa. Sen jälkeen se antaa pisteet niistä neljästä kerroksesta, jotka esiteltiin luvussa 1: Tieto, Työkalut, Taidot ja Tahti. Jokaisesta 25 pistettä, sata yhteensä.

Ensimmäinen tulos on yleensä matala. Se on oikein. Pisteitä annetaan vain siitä, mikä on todistettavasti kokeiltu, ei siitä mikä on olemassa. Tyhjä pohja saa nollan vaikka se olisi kaunis.

Raportti nimeää kolme korjausta tärkeysjärjestyksessä. Valitse niistä ensimmäinen.

**Päivänä 14 kirjoita `/kehita`.**

Se haastattelee sut ja rakentaa yhden asian valmiiksi. Yhden, ei kolmea. Haastattelu tuntuu ehkä turhalta kun sä jo tiedät mitä haluat, mutta sen kysymykset ovat juuri ne, jotka kannattaa oppia kysymään itseltään.

**Sen jälkeen viikoittain.** `/tarkista` kertoo mikä ontuu, `/kehita` korjaa yhden asian. Kolmessa kuukaudessa siitä tulee kaksitoista parannusta.

---

## 8. Usein kysyttyä

**Paljonko tämä maksaa?**
Tämä paketti on ilmainen. Claude Pro -tilaus maksaa 20 dollaria kuussa, noin 19 euroa. Muuta ei tarvita.

**Toimiiko tämä ChatGPT:llä?**
Ei sellaisenaan. Komennot ja tiedostojen luku on tehty Clauden työpöytäsovellukselle. Itse ajatus toimii muuallakin, mutta silloin joudut liittämään tiedostot käsin joka keskusteluun, mikä on juuri se ongelma jonka tämä poistaa.

**Missä mun tiedot ovat?**
Sun koneella, siinä kansiossa. Voit avata jokaisen tiedoston ja lukea sen. Voit myös poistaa koko kansion, jolloin kaikki on poissa.

**Näkeekö joku muu nämä? Entä asiakastiedot?**
Tiedostot pysyvät sun koneella. Mutta kun sä keskustelet assistentin kanssa, se lukee tiedostot ja niiden sisältö kulkee samalla tavalla Anthropicin palvelimille kuin mikä tahansa viesti, jonka sä kirjoitat chattiin. Se on siis sama tilanne kuin liittäisit tekstin keskusteluun käsin.

Käytännössä tämä tarkoittaa kolmea asiaa. Maksullisten tilausten keskusteluja ei oletuksena käytetä mallien opettamiseen, mutta tarkista asetus itse tilisi kohdalta. Jos sulla on asiakassopimuksissa ehtoja tietojen käsittelystä, ne koskevat myös tätä. Ja arkaluontoisimmat tiedot, kuten henkilötunnukset tai terveystiedot, kannattaa jättää kokonaan pois näistä tiedostoista.

Haastattelut ja tarkistusraportit merkitsin erikseen yksityisiksi, koska niihin päätyy usein asiakastietoa.

**Mitä jos mun kone hajoaa?**
Sitten kansio on poissa, koska se on vain sun koneella. Ota siitä varmuuskopio samalla tavalla kuin muistakin työtiedostoistasi. Helpoin tapa on kopioida kansio muistitikulle kerran kuussa.

**Voinko laittaa tänne salasanoja tai API-avaimia?**
Et. Ne kuuluvat erilliseen tiedostoon, joka on jätetty jakamisen ulkopuolelle. Jos et tiedä mikä API-avain on, sä et tarvitse sitä vielä.

**Vastasin johonkin väärin. Voinko korjata?**
Voit. Helpoin tapa on sanoa assistentille: *"kysymyksen 3 vastaus meni väärin, korjaa se näin"*. Voit myös avata tiedoston `haastattelu.md` Muistiolla tai TextEditillä ja muokata sitä käsin. Kirjoita sen jälkeen `/aloita`, niin se päivittää muuttuneen kohdan.

**Voinko lisätä omia kansioita?**
Voit, mutta vasta kun sulla on niihin jotain pantavaa. Kun lisäät jotain, kirjoita `/linkita`, muuten assistentti ei löydä sitä. Tiedostossa `LAAJENNUKSET.md` on lista siitä, mitä kannattaa lisätä ja missä vaiheessa.

**Meitä on kolme henkeä. Mitä teen?**
Tee ensin omasi ja käytä sitä kuukausi. Jos se toimii, kopioi kansio kollegalle ja anna hänen ajaa `/aloita` omilla vastauksillaan. Yhteiset faktat, kuten hinnasto ja asiakaslista, kannattaa siinä vaiheessa pitää yhdessä paikassa johon molemmat kansiot osoittavat.

**Toimiiko tämä suomeksi?**
Kaikki komennot ja tiedostot ovat suomeksi. Assistentti vastaa sillä kielellä, jolla sä kirjoitat.

**Mitä jos assistentti keksii asioita?**
Kerro sille. Tiedostoissa lukee, että se ei saa arvata lukuja ja että sen pitää sanoa jos se ei tiedä. Jos se silti arvaa, se on merkki siitä että jokin tieto puuttuu. Kirjoita `/tarkista`, se näyttää mistä.

**Pitääkö tätä päivittää?**
Ei tarvitse. Paketti toimii sellaisenaan. Jos teen siihen parannuksia, kerron niistä ja voit halutessasi ladata uuden version. Omat vastauksesi eivät katoa, jos otat niistä kopion ensin.

---

## 9. Edistyneille

Nämä eivät ole pakollisia. Ohita, jos edellinen osio riitti.

Ensin yksi nimiasia, joka hämmentää monia. Se osa Clauden sovelluksesta, joka lukee kansioita, on nimeltään Claude Code. Sä et siis asentanut kahta eri ohjelmaa. Nimessä on sana koodi, mutta se toimii aivan yhtä hyvin tekstitiedostoille.

**Git.** Jos osaat käyttää gitiä, kloonaa repo zipin lataamisen sijaan. Silloin saat päivitykset yhdellä komennolla ja oma historiasi säilyy.

**Komentorivi.** Claude Code toimii myös terminaalissa. Samat komennot, sama kansio.

**Kalenteri ja sähköposti.** Assistentin saa yltämään kalenteriin, sähköpostiin ja tiedostoihin liittimillä. Liitin on valmis yhteys johonkin palveluun. Liittimet otetaan käyttöön Clauden asetuksista. Tämä on toinen kerros, Työkalut. Kannattaa tehdä vasta kun ensimmäinen kerros, Tieto, on kunnossa. Nopea kone väärällä tiedolla tekee vääriä asioita nopeammin.

**Omat komennot.** Kun sama monivaiheinen homma toistuu kolmatta kertaa, siitä kannattaa tehdä komento. `/kehita` osaa rakentaa sellaisen puolestasi.

**Ajastukset.** Neljäs kerros, Tahti. Älä ajasta mitään, mikä ei toimi käsin ajettuna. Tämä on se sääntö, jonka rikkomisesta seuraa eniten harmia.

---

## 10. Kuka tämän teki

Ilmari Salmisto, PolkuAI. Rakennan tekoälyjärjestelmiä ja automaatioita yrityksille.

Tämä paketti on ilmainen ja MIT-lisensoitu. Se tarkoittaa, että saat käyttää, muokata ja jakaa sitä vapaasti, myös kaupallisesti.

Jos jokin kohta tökkää, laita viestiä. Vastaan samana päivänä. Ja jos rakennat tästä jotain, kuulen siitä mielelläni.

- Sähköposti: ilmari@polkuai.com
- LinkedIn: Ilmari Salmisto
- polkuai.com
