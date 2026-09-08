# Yrittäjän AI-käyttöjärjestelmä

Opas alusta loppuun. Asennus on kolme askelta. Loppu on sitä, mitä sillä tehdään.

---

## 1. Mikä ongelma tässä ratkaistaan

Sä käytät varmaan jo tekoälyä. Avaat keskustelun, selität tilanteen, saat vastauksen. Seuraavana päivänä avaat uuden keskustelun ja selität saman tilanteen uudestaan.

Se selittäminen on se ongelma. Se maksaa muutaman minuutin joka kerta ja tekee vastauksista yleisiä. Assistentti ei tunne sun hinnoittelua, asiakkaita eikä kirjoitustyyliä, joten se antaa neuvoja jotka sopivat kenelle tahansa.

Tämä paketti korjaa sen. Se on kansio tekstitiedostoja, joissa lukee kuka sä olet, mitä sä myyt, kenelle ja millä tyylillä sä kirjoitat. Assistentti lukee ne joka kerta automaattisesti.

Mukana tulee viisi valmista komentoa. Komento on sana, joka alkaa kauttaviivalla. Kirjoitat sen tavalliseen viestikenttään kuten minkä tahansa viestin, ja assistentti vie monivaiheisen homman läpi ilman että ohjaat sitä joka välissä.

| Komento | Mitä tekee | Milloin |
|---|---|---|
| `/aloita` | Haastattelee sinut ja täyttää pohjat | Ensimmäisenä päivänä |
| `/syvenna` | Purkaa yhden asian päästäsi tiedostoon | Aina kun tarve |
| `/linkita` | Lisää uuden kansion tai lähteen löydettäväksi | Kun otat jotain uutta käyttöön |
| `/tarkista` | Testaa toimiiko järjestelmä ja antaa pisteet | Päivänä 7, sitten viikoittain |
| `/kehita` | Vie yhden parannuksen maaliin | Päivänä 14, sitten viikoittain |

**Mitä tämä ei ole.** Ei ohjelma eikä sovellus. Ei omia tunnuksia eikä pilvipalvelua. Kansio, jonka jokaisen tiedoston sä voit avata ja lukea.

**Mihin tämä perustuu.** Toimiva järjestelmä koostuu neljästä kerroksesta. **Tieto** eli se tuntee sun firman, **Työkalut** eli se yltää sinne missä sun tieto on, **Taidot** eli se osaa tehdä sun työsi vaiheet ja **Tahti** eli se toimii ilman että pyydät. Tieto on aina ensin ja Tahti aina viimeisenä. Kaksi ensimmäistä syntyvät tämän oppaan aikana.

---

## 2. Mitä tarvitset

**Claude Pro -tilaus, 20 dollaria kuussa.** Noin 19 euroa. Se sisältää Claude Coden, joka on se osa Clauden sovellusta joka osaa lukea koneesi kansioita. Ilmaisversio ei riitä eikä kalliimpaa Max-tilausta tarvita.

**Claude-työpöytäsovellus.** Lataa osoitteesta claude.ai/download. Selain ei käy, koska se ei näe sun koneen kansioita.

**Tunti aikaa.** Asennus vie viisi minuuttia. Alkuhaastattelu 20-30 minuuttia. Uuteen tapaan tottuminen pari viikkoa, mutta se ei ole työtä.

**Kaksi omaa tekstiä.** Sähköposti asiakkaalle, LinkedIn-postaus, tarjous. Mikä tahansa, minkä sä olet oikeasti itse kirjoittanut. Etsi ne valmiiksi, lähetetyt-kansio on paras paikka.

Ohjelmointitaitoa ei tarvita. Komentoriviä ei tarvita.

---

## 3. Asennus

Sun ei tarvitse ladata mitään eikä purkaa mitään. Assistentti kasaa kansion puolestasi.

**1. Luo uusi tyhjä kansio.** Vaikka työpöydälle, vaikka yrityksesi nimellä. Älä laita sitä OneDriveen tai Dropboxiin, koska synkronointi ja tiedostojen muokkaus tekevät joskus yhdessä tyhmyyksiä.

**2. Avaa se Claude Codessa.** Avaa Claude-työpöytäsovellus, siirry **Code**-näkymään ja valitse äsken luomasi kansio. Claude kysyy luultavasti lupaa lukea kansiota ja tehdä siihen muutoksia. Vastaa kyllä, kysymys koskee vain tätä kansiota.

**3. Liitä tämä viesti ja paina enter.**

> Asenna tähän kansioon Yrittäjän AI-käyttöjärjestelmä.
> Ohjeet ovat tiedostossa ASENNUS.md:
> https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/blob/main/ASENNUS.md

Assistentti hakee tiedostot ja kertoo kun kansio on kasassa. Se kestää minuutin. Voit seurata mitä se tekee, mutta sun ei tarvitse ymmärtää siitä mitään.

**Sen jälkeen avaa uusi keskustelu.** Tämä on tärkeää: viisi komentoa tulevat käyttöön vasta uudessa keskustelussa. Vanhassa ne eivät toimi.

---

## 4. Jos jokin ei toimi

**En löydä Code-näkymää.** Yleensä syy on tilaus. Tarkista claude.ai-sivulta, että tilaus on Pro eikä Free. Jos tilaus on kunnossa, sulje sovellus kokonaan ja avaa uudelleen. Jos se ei vieläkään näy, lataa sovellus uusimpana versiona osoitteesta claude.ai/download.

**Asennus ei onnistunut tai kansio jäi puolityhjäksi.** Sano assistentille: *"tarkista mitä kansiosta puuttuu ja hae puuttuvat tiedostot uudestaan"*. Se osaa korjata sen itse.

**Kirjoitin `/aloita` eikä mitään tapahtunut.** Avasitko uuden keskustelun asennuksen jälkeen? Komennot eivät ilmesty siihen keskusteluun, jossa asennus tehtiin. Jos avasit ja se ei silti toimi, kirjoita sen sijaan tämä ja se tekee saman asian:

> lue tiedosto .claude/skills/aloita/SKILL.md ja toimi sen mukaan

**Viestiraja tuli vastaan kesken haastattelun.** Maksullisessakin tilauksessa on käyttöraja, joka nollautuu muutaman tunnin välein. Vastauksesi eivät katoa, koska ne tallentuvat sitä mukaa kun vastaat. Kirjoita `/aloita` uudestaan, niin haastattelu jatkuu siitä mihin jäit. Sama pätee jos joudut lopettamaan kesken.

**Pitääkö kansio avata joka kerta uudestaan?** Ei. Se jää sovelluksen listaan ja valitset sen sieltä.

**Jos mikään näistä ei auta,** laita mulle sähköpostia osoitteeseen ilmari@polkuai.com. Kerro missä kohtaa jumitit ja mitä ruudulla luki. Vastaan samana päivänä. Kysymys ei ole tyhmä.

---

## 5. Ensimmäinen ajo

Kirjoita uudessa keskustelussa `/aloita`. Assistentti kysyy seitsemän kysymystä yksi kerrallaan:

1. Kuka olet, mitä myyt ja kenelle
2. Näyte omasta kirjoituksestasi
3. Kolme tärkeintä asiaa seuraavalle 90 päivälle
4. Mihin raha oikeasti laskeutuu ja missä sitä seurataan
5. Missä puhut asiakkaille, tiimille ja ulkomaailmalle
6. Missä tiedostot ja muistiinpanot ovat
7. Mikä tehtävä syö viikkosi

Vastaa rehellisesti, älä kauniisti. Tämä ei ole hakemus vaan asetustiedosto. Jos jokin asia on sekaisin, kirjoita että se on sekaisin.

Kolme kohtaa, joissa kannattaa hidastaa:

**Kysymys 2 haluaa oikeaa tekstiä.** Liitä ne kaksi tekstiä sellaisenaan. Älä siisti äläkä kirjoita uutta. Jos sä kirjoitat näytteen tähän keskusteluun, sä kirjoitat sen huolellisemmin kuin normaalisti, ja silloin assistentti oppii tyylin jolla sä et oikeasti kirjoita.

**Kysymys 3 vaatii numeron.** "Kasvattaa myyntiä" ei kelpaa. "Kolme uutta asiakasta lokakuun loppuun mennessä" kelpaa. Assistentti painostaa tässä kohtaa, ja niin sen kuuluukin tehdä. Ilman lukua se ei voi myöhemmin kertoa, meneekö hyvin.

**Kysymys 6 haluaa totuuden.** Jos tiedostot ovat kolmessa paikassa ja osa työpöydällä, sano se. Tavoitetilan kertominen kostautuu heti.

Kokeile lopuksi tätä:

> Mihin mun kannattaa keskittyä tällä viikolla?

Vastauksen laatu kertoo, miten haastattelu meni. Jos vastaus on yleistä jaarittelua, jokin kohta jäi ohueksi. Sano assistentille mikä kohta, niin se kysyy siitä lisää.

---

## 6. Ensimmäinen viikko

Älä rakenna mitään. Käytä.

Tuo assistentille oikeita kysymyksiä. Asiakkaan sähköposti johon pitää vastata. Tarjous jota mietit. Hinnoittelupulma. Kalenteri joka on täynnä vääriä asioita.

Kolme tapaa, jotka kannattaa ottaa käyttöön heti:

**Pyydä kirjaamaan päätökset.** Kun sä päätät jotain, sano *"kirjaa tämä päätöslokiin"*. Puolen vuoden päästä sä muistat mitä päätit mutta et miksi. Silloin sama keskustelu alkaa alusta.

**Kysy ennen kuin teet käsin.** Kun eteesi tulee uusi homma, kysy *"missä määrin tekoäly voi hoitaa tämän?"* Vastaus on yllättävän usein "suurimman osan".

**Pura asioita päästäsi.** Kun jokin iso asia on selvittämättä, kirjoita `/syvenna`. Se haastattelee sut aiheesta ja tallentaa jokaisen vastauksen. Hyviä aiheita: miten hinnoittelu oikeasti menee, mitä viime projektissa opittiin, miten uusi palvelu pitäisi rakentaa.

Ensimmäisellä viikolla sä olet todennäköisesti hitaampi kuin ennen. Se on normaalia. Kankeus menee ohi noin kahdessa viikossa ja useimmat lopettavat sitä ennen.

---

## 7. Päivä 7 ja päivä 14

**Päivänä 7 kirjoita `/tarkista`.** Se testaa viidellä kysymyksellä, löytääkö järjestelmä oman tietonsa, ja antaa pisteet niistä neljästä kerroksesta. Sata on maksimi.

Ensimmäinen tulos on yleensä matala. Se on oikein. Pisteitä annetaan vain siitä, mikä on todistettavasti kokeiltu, ei siitä mikä on olemassa. Tyhjä pohja saa nollan vaikka se olisi kaunis. Raportti nimeää kolme korjausta tärkeysjärjestyksessä. Valitse niistä ensimmäinen.

**Päivänä 14 kirjoita `/kehita`.** Se haastattelee sut ja rakentaa yhden asian valmiiksi. Yhden, ei kolmea. Haastattelu tuntuu ehkä turhalta kun sä jo tiedät mitä haluat, mutta sen kysymykset ovat juuri ne, jotka kannattaa oppia kysymään itseltään.

**Sen jälkeen viikoittain.** `/tarkista` kertoo mikä ontuu, `/kehita` korjaa yhden asian. Kolmessa kuukaudessa siitä tulee kaksitoista parannusta.

---

## 8. Usein kysyttyä

**Paljonko tämä maksaa?**
Tämä paketti on ilmainen. Claude Pro maksaa 20 dollaria kuussa. Muuta ei tarvita.

**Missä mun tiedot ovat?**
Sun koneella, siinä kansiossa. Voit avata jokaisen tiedoston ja lukea sen. Voit myös poistaa koko kansion, jolloin kaikki on poissa.

**Näkeekö joku muu nämä? Entä asiakastiedot?**
Tiedostot pysyvät sun koneella. Mutta kun sä keskustelet assistentin kanssa, se lukee tiedostot ja niiden sisältö kulkee samalla tavalla Anthropicin palvelimille kuin mikä tahansa viesti jonka sä kirjoitat chattiin. Sama tilanne kuin liittäisit tekstin keskusteluun käsin.

Käytännössä tämä tarkoittaa kolmea asiaa. Maksullisten tilausten keskusteluja ei oletuksena käytetä mallien opettamiseen, mutta tarkista asetus itse tilisi kohdalta. Jos sulla on asiakassopimuksissa ehtoja tietojen käsittelystä, ne koskevat myös tätä. Arkaluontoisimmat tiedot, kuten henkilötunnukset ja terveystiedot, kannattaa jättää kokonaan pois näistä tiedostoista.

**Jaan kansion kollegalle. Mitä pitää muistaa?**
Kolme tiedostoa täyttyy asiakastiedolla: alkuhaastattelu, ääniprofiili ja yritystiedot. Ääniprofiiliin päätyy kokonaisia asiakassähköposteja nimineen ja hintoineen. Siivoa ne ennen jakamista.

**Mitä jos mun kone hajoaa?**
Kansio on vain sun koneella. Kopioi se muistitikulle kerran kuussa, samalla tavalla kuin muutkin työtiedostosi.

**Vastasin johonkin väärin. Voinko korjata?**
Voit. Sano assistentille *"kysymyksen 3 vastaus meni väärin, korjaa se näin"*. Voit myös muokata tiedostoa `haastattelu.md` käsin ja kirjoittaa sitten `/aloita`, jolloin se päivittää muuttuneen kohdan.

**Voinko lisätä omia kansioita?**
Voit, mutta vasta kun sulla on niihin jotain pantavaa. Kun lisäät jotain, kirjoita `/linkita`, muuten assistentti ei löydä sitä. Tiedostossa `LAAJENNUKSET.md` on lista siitä mitä kannattaa lisätä ja missä vaiheessa.

**Saanko assistentin lukemaan kalenterini ja sähköpostini?**
Saat, liittimillä. Ne otetaan käyttöön Clauden asetuksista. Tämä on toinen kerros, Työkalut, ja se kannattaa tehdä vasta kun ensimmäinen kerros on kunnossa. Nopea kone väärällä tiedolla tekee vääriä asioita nopeammin.

**Mitä jos assistentti keksii asioita?**
Kerro sille. Tiedostoissa lukee, että se ei saa arvata lukuja ja että sen pitää sanoa jos se ei tiedä. Jos se silti arvaa, jokin tieto puuttuu. Kirjoita `/tarkista`, se näyttää mistä.

**Meitä on kolme henkeä. Mitä teen?**
Tee ensin omasi ja käytä sitä kuukausi. Jos se toimii, anna kollegan tehdä samat kolme askelta omaan kansioonsa ja ajaa `/aloita` omilla vastauksillaan.

**Toimiiko tämä ChatGPT:llä?**
Ei sellaisenaan. Komennot ja tiedostojen luku on tehty Claude Codelle.

**Pitääkö tätä päivittää?**
Ei tarvitse. Jos teen parannuksia, kerron niistä. Omat vastauksesi eivät katoa, jos otat niistä kopion ensin.

---

## 9. Kuka tämän teki

Ilmari Salmisto, PolkuAI. Rakennan tekoälyjärjestelmiä ja automaatioita yrityksille.

Tämä paketti on ilmainen ja MIT-lisensoitu. Saat käyttää, muokata ja jakaa sitä vapaasti, myös kaupallisesti.

Jos jokin kohta tökkää tai jos rakennat tästä jotain, laita viestiä. Vastaan samana päivänä.

- Sähköposti: ilmari@polkuai.com
- LinkedIn: Ilmari Salmisto
- polkuai.com
