---
name: kehita
description: Nayttaa mitka parannukset kannattavat eniten suhteessa vaivaan ja rakentaa valitun. Käytä kun käyttäjä sanoo "kehitä", "paranna", "mitä automatisoidaan", "mitä seuraavaksi", "missä on helpoin voitto", tai heti /tarkista-ajon jälkeen. Ehdottaa ensin vaihtoehdot, sitten haastattelee ja rakentaa yhden asian valmiiksi.
---

# Kehitä

Näytä ensin mitä kannattaa parantaa. Anna käyttäjän valita. Rakenna sitten valittu valmiiksi.

Yksi ajo, yksi valmis parannus. Ei kolmea puolivalmista.

Lue ensin `ohjeet/tyoskentelymalli.md`. Lue myös viimeisin raportti kansiosta `tarkistukset/`, tiedosto `paatokset/loki.md` ja `tausta/prioriteetit.md`:n kohta "Viikon aikasyöppö".

## Vaihe 0: Näytä vaihtoehdot

Ennen kysymyksiä kokoa lista siitä, mitä juuri nyt kannattaisi parantaa. Vetäisit lähteet tässä järjestyksessä:

1. Viimeisimmän `/tarkista`-raportin kolme korjausta ja avoimet löydökset.
2. `tausta/prioriteetit.md`:n viikon aikasyöppö.
3. Se, minkä olet itse huomannut toistuvan käyttäjän kanssa.

Esitä 3-5 vaihtoehtoa taulukkona. Jokaisesta neljä saraketta: **mikä**, **mitä hyötyä**, **paljonko vaivaa** ja **mihin löydökseen liittyy**.

Arvioi vaiva kolmeportaisesti: pieni tarkoittaa alle tuntia, keskikokoinen yhtä istumaa, iso useampaa kertaa.

**Merkitse helpoin voitto erikseen.** Se on rivi, jossa hyöty on suuri ja vaiva pieni. Jos sellaista ei ole, sano se suoraan äläkä keksi sitä.

Järjestä taulukko hyödyn ja vaivan suhteen mukaan, älä pelkän hyödyn. Iso parannus, joka ei valmistu tänään, on huonompi kuin pieni joka valmistuu.

Kysy sitten yksi kysymys: minkä näistä otetaan? Käyttäjä saa myös ehdottaa jotain listan ulkopuolelta. Hänen tuntemansa kipu voittaa raportin.

Jos käyttäjä epäröi, suosittele helpointa voittoa ja perustele yhdellä lauseella.

## Vaihe 1: Asenne

Kun kohde on valittu, tarkenna se. Kaksi kysymystä, yksi kerrallaan.

**1. Pilkotaan se osiin. Mitä siinä oikeasti tapahtuu vaihe vaiheelta?**
Kirjoita vaiheet näkyviin. Tässä paljastuu yleensä, että tehtävä on viisi tehtävää.

**2. Käydään vaiheet läpi: missä määrin tekoäly voi hoitaa tämän?**
Jokaisesta vaiheesta erikseen. Vastaus on liukuma, ei kyllä tai ei.

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

- **Yksi asia per ajo.** Tämä on koko skillin idea. Vaiheessa 0 näytetään monta vaihtoehtoa, mutta rakennetaan vain yksi. Jos käyttäjä haluaa kolme, tee tärkein ja kirjaa kaksi muuta odottamaan.
- **Älä hyppää suoraan vaiheeseen 3.** Haastattelu ennen rakentamista on se osa, joka opettaa. Ilman sitä tämä on pelkkä koodipyyntö.
- **Älä nosta itsenäisyystasoa ilman ajohistoriaa.** Taso 4 vaatii kuukauden tasolla 3.
- **Älä rakenna sitä, mikä on jo olemassa.** Katso ensin, ratkaiseeko olemassa oleva komento tämän korjattuna.
- **Älä lupaa lukuja.** Kirjaa lähtötilanne ja mittaa ensi kerralla.
