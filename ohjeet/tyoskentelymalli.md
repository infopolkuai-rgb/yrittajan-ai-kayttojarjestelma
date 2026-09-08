# Työskentelymalli

Kaksi muistisääntöä. Toinen on sinua varten, toinen järjestelmää varten.

**Kolme A:ta** kertoo miten yrittäjä ajattelee, kun tekoäly on käytettävissä.
**Neljä T:tä** kertoo mistä osista toimiva järjestelmä koostuu.

Lue tämä kerran läpi. Sen jälkeen palaa tänne aina kun `/kehita` tai `/tarkista` viittaa johonkin kohtaan.

---

## Kolme A:ta: miten ajattelet

### Asenne

Vanha tapa aloittaa uusi tehtävä on kysyä "miten mä teen tämän". Uusi tapa on kysyä ensin **"missä määrin tekoäly voi hoitaa tämän?"**

Kysymys ei ole kyllä tai ei. Se on liukuma. Joskus vastaus on "se kirjoittaa raakaversion ja mä viimeistelen". Joskus "se tekee kaiken ja mä katson tuloksen kerran viikossa". Joskus "ei mitenkään, tämä on käsityötä". Kaikki kolme ovat oikeita vastauksia. Väärä vastaus on se, ettei kysy.

Kolme tapaa pitää asenne kunnossa:

**Pilko työ osiin.** "Asiakasraportointi" ei ole tehtävä vaan nippu tehtäviä: hae luvut, tarkista poikkeamat, kirjoita selitys, muotoile, lähetä. Tekoäly ei ehkä osaa koko nippua. Se osaa melkein varmasti kolme viidestä. Ihmiset hylkäävät automaation liian aikaisin, koska katsovat isoa möykkyä eivätkä paloja.

**Kokeile kun et tiedä.** Jos et osaa sanoa hoituuko jokin tekoälyllä, kokeilu kestää viisi minuuttia ja arvailu kestää kuukauden. Kokeile.

**Odota alkukankeutta.** Ensimmäisellä viikolla olet hitaampi kuin ennen. Se ei ole merkki siitä että tämä ei toimi. Se on merkki siitä että opettelet. Kankeus menee ohi noin kahdessa viikossa. Useimmat lopettavat sitä ennen.

### Askeleet

Kun olet päättänyt että jokin kannattaa automatisoida, mene näin. Järjestys ei ole koriste.

**1. Etsi pullonkaula.** Mikä yksi asia hidastaa juuri nyt eniten? Älä automatisoi sitä mikä on helpointa automatisoida. Automatisoi se mikä sattuu. Hyvä testi: jos tämä katoaisi huomenna, huomaisitko sen?

**2. Poista, automatisoi tai delegoi. Tässä järjestyksessä.** Ensin kysy pitääkö tätä tehdä ollenkaan. Iso osa toistuvasta työstä on tapa, ei tarve. Sen jälkeen kysy voiko tekoäly hoitaa sen. Vasta viimeisenä kysy kuka ihminen sen tekee. Automatisoitu turha työ on edelleen turhaa työtä.

**3. Kuvaa prosessi ennen kuin rakennat.** Kirjoita auki mitä tapahtuu ensin, mitä sitten ja mistä tiedät että se meni oikein. Jos et osaa kirjoittaa sitä auki, et osaa myöskään automatisoida sitä. Tämä vaihe paljastaa yleensä että prosessi ei ollut selvä sinullekaan.

**4. Valitse kuinka itsenäisesti se toimii.** Neljä tasoa:

| Taso | Mitä tarkoittaa | Milloin |
|---|---|---|
| 1 | Sinä pyydät, se tekee, sinä tarkistat | Aina alussa |
| 2 | Se tekee luonnoksen, sinä hyväksyt ennen lähetystä | Kun luonnokset ovat toistuvasti hyviä |
| 3 | Se tekee ja ilmoittaa jälkikäteen | Kun virhe on halpa korjata |
| 4 | Se tekee etkä kuule siitä ellei tule ongelmaa | Vasta kun on ajettu kuukausi tasolla 3 |

Yleisin virhe on hypätä suoraan tasolle 4. Toiseksi yleisin on jäädä ikuisesti tasolle 1.

**5. Sido mittariin.** Mikä luku muuttuu jos tämä toimii? Säästetyt tunnit, vastausaika, virheiden määrä, myydyt kaupat. Jos et osaa nimetä lukua, et tiedä myöhemmin kannattiko tämä. Kirjaa lähtötilanne ennen kuin rakennat.

### Automaatio

Kun rakennat, nämä säännöt pitävät homman kasassa.

**Pieniä paloja, ei yhtä möhkälettä.** Viisi pientä osaa, jotka tekevät kukin yhden asian, on parempi kuin yksi iso joka tekee kaiken. Kun jokin hajoaa, tiedät heti mikä.

**Tarkistus joka väliin.** Jokaisen vaiheen jälkeen kysy: onko tulos järkevä? Tyhjä vastaus, väärä muoto ja outo luku pitää huomata siinä kohtaa missä ne syntyvät, ei vasta asiakkaan sähköpostissa.

**Aja ensin käsin.** Tee homma kolme kertaa itse ja katso mitä oikeasti tapahtuu. Vasta sitten automatisoi. Automaatio, joka rakennettiin kuvitellun prosessin päälle, hajoaa ensimmäisenä päivänä.

**Kohtele sitä kuin uutta harjoittelijaa.** Harjoittelija on fiksu mutta ei tunne taloa. Se ei tiedä mitä et sanonut. Anna sille sama konteksti, jonka antaisit ihmiselle: mitä tehdään, kenelle, miltä hyvä lopputulos näyttää, mitä ei saa tehdä.

**Aina pysäytysnappi.** Sinun pitää pystyä lopettamaan automaatio yhdellä liikkeellä. Ilman sitä et uskalla nostaa sitä tasolle 3, ja järjestelmä jää ikuiseksi demoksi.

**Tylsä on kaunista.** Yksinkertainen kone, joka toimii joka päivä, voittaa nokkelan kokeilun. Jos kaksi tapaa tekee saman, valitse tylsempi.

---

## Neljä T:tä: mistä järjestelmä koostuu

Neljä kerrosta. `/tarkista` antaa jokaisesta pisteet.

| | Kerros | Mitä tarkoittaa | Näin tiedät että se on kunnossa |
|---|---|---|---|
| 1 | **Tieto** | Assistentti tuntee sinut ja yrityksesi | Uusi tyhjä keskustelu vastaa kysymykseen "mitä tämä yritys tekee ja kenelle" ilman että etsit mitään |
| 2 | **Työkalut** | Se yltää siihen missä tietosi on | Kysyt "mitä mulla on huomenna kalenterissa" ja saat oikean vastauksen ilman että liität mitään |
| 3 | **Taidot** | Se osaa tehdä työsi vaiheet | Kirjoitat lyhyen komennon ja saat valmiin tuotoksen, et keskustelua |
| 4 | **Tahti** | Se toimii ilman että pyydät | Kone on kiinni ja silti postilaatikossasi on aamukatsaus |

**Järjestys on pakollinen.** Tieto ensin, aina. Ilman sitä loput kerrokset tekevät nopeasti vääriä asioita. Työkalut ja Taidot voi rakentaa rinnakkain. Tahti on viimeinen. Älä koskaan ajasta työnkulkua, joka ei toimi käsin ajettuna.

Yleisin tapa mennä metsään on rakentaa Taitoja, kun Tieto on puolityhjä. Silloin saat sujuvia vastauksia, jotka koskevat jotakuta muuta kuin sinua.
