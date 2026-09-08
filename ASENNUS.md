# Asennusohje

*Tämä tiedosto on tekoälylle. Ihmisen ohje on docs/opas.md samassa paketissa.*

Sinua on pyydetty asentamaan Yrittäjän AI-käyttöjärjestelmä käyttäjän kansioon. Tee vaiheet järjestyksessä.

---

## Vaihe 1. Varmista kohde

Olet käyttäjän omassa kansiossa. Katso ensin mitä siellä on.

```bash
ls -a
```

```powershell
Get-ChildItem -Force
```

**Jos kansiossa on jo `CLAUDE.md` ja kansio `.claude/skills/aloita/`, paketti on jo asennettu.** Älä asenna uudestaan. Kerro käyttäjälle, että kansio on jo kunnossa ja että hän voi kirjoittaa `/aloita`. Lopeta tähän.

Muussa tapauksessa kansion pitää olla tyhjä. Tyhjäksi lasketaan myös kansio, jossa on vain käyttöjärjestelmän omia tiedostoja: `desktop.ini`, `.DS_Store`, `Thumbs.db`. Ne eivät estä asennusta, ja ne jätetään paikoilleen.

Jos kansiossa on mitä tahansa muuta, kysy käyttäjältä ennen kuin jatkat. Älä koskaan asenna tätä kansioon, jossa on käyttäjän muita töitä.

---

## Vaihe 2. Nouda ja pura paketti

Valitse lohko komentotulkin mukaan, ei käyttöjärjestelmän. **Jos käytössäsi on bash, myös Windowsissa, käytä bash-lohkoja. Jos käytössäsi on vain PowerShell, käytä PowerShell-lohkoja.**

Jokaisessa lohkossa on kaksi vaihtoehtoa. **Kokeile ensin vaihtoehtoa A.**

Vaihtoehto A on epäonnistunut, jos **mikä tahansa** sen neljästä rivistä kaatuu. Pelkkä clonen onnistuminen ei riitä. Kun A epäonnistuu, tee kaksi asiaa tässä järjestyksessä:

1. **Siivoa ensin.** Poista `.tmp-aios` kokonaan. Se sisältää `.git`-kansion, ja jos jätät sen paikalleen, seuraava vaihtoehto siirtää sen käyttäjän kansioon. Juuri sitä lopputulosta tämä ohje yrittää estää.
2. Aja vasta sitten vaihtoehto B **samasta lohkosta**.

Älä sekoita bash- ja PowerShell-lohkoja keskenään, äläkä aja vaihtoehtoja A ja B päällekkäin. Ne tuottavat eri kansiorakenteen.

Aja komennot yksi rivi kerrallaan ja katso jokaisen tulos. Jos jokin rivi epäonnistuu, älä jatka seuraavaan.

Komennot on kirjoitettu niin, että piilotiedostot `.claude/` ja `.gitignore` siirtyvät mukana. Ne ovat pakollisia, ja ilman niitä käyttäjän viisi komentoa eivät toimi. Tavallinen `mv .tmp-aios/* .` jättää ne siirtämättä, joten älä korvaa alla olevia komentoja sillä.

### Bash: vaihtoehto A, git

```bash
git clone --depth 1 https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma.git .tmp-aios
rm -rf .tmp-aios/.git
cp -a .tmp-aios/. .
rm -rf .tmp-aios
```

### Bash: vaihtoehto B, arkiston lataus

```bash
curl -L -o aios.zip https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/archive/refs/heads/main.zip
unzip -q aios.zip -d .tmp-aios
cp -a .tmp-aios/yrittajan-ai-kayttojarjestelma-main/. .
rm -rf .tmp-aios aios.zip
```

### PowerShell: vaihtoehto A, git

```powershell
git clone --depth 1 https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma.git .tmp-aios
Remove-Item ".tmp-aios\.git" -Recurse -Force
Get-ChildItem -Path ".tmp-aios" -Force | Move-Item -Destination "." -Force
Remove-Item ".tmp-aios" -Recurse -Force
```

### PowerShell: vaihtoehto B, arkiston lataus

```powershell
[Net.ServicePointManager]::SecurityProtocol = 'Tls12'
Invoke-WebRequest -Uri "https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/archive/refs/heads/main.zip" -OutFile "aios.zip"
Expand-Archive -Path "aios.zip" -DestinationPath ".tmp-aios" -Force
Get-ChildItem -Path ".tmp-aios\yrittajan-ai-kayttojarjestelma-main" -Force | Move-Item -Destination "." -Force
Remove-Item ".tmp-aios", "aios.zip" -Recurse -Force
```

Ensimmäinen rivi asettaa TLS 1.2:n. Ilman sitä lataus kaatuu vanhemmassa Windowsissa virheeseen, joka puhuu SSL-kanavasta, eikä käyttäjä osaa tulkita sitä.

### Siivouskomento kesken jääneen yrityksen jälkeen

```bash
rm -rf .tmp-aios aios.zip
```

```powershell
Remove-Item ".tmp-aios", "aios.zip" -Recurse -Force -ErrorAction SilentlyContinue
```

### Kaksi asiaa molemmista vaihtoehdoista

Vaihtoehdossa A arkiston sisältö on suoraan `.tmp-aios`-kansion juuressa. Väliin ei tule ylimääräistä kansiota. `.git` poistetaan ennen kopiointia, eikä sitä siirretä käyttäjän kansioon missään vaiheessa. Siirretty `.git` kytkisi käyttäjän kansion tähän repoon, eikä hän tarvitse sen historiaa.

Vaihtoehdossa B arkiston sisällä on yksi kansio nimeltä `yrittajan-ai-kayttojarjestelma-main`. Komennot siirtävät sen sisällön, eivät kansiota itseään.

---

## Vaihe 3. Tarkista

Aja nämä ja katso tuloste. Aja jokainen erikseen.

```bash
ls -a
ls .claude/skills
ls .claude/skills/*/SKILL.md
```

```powershell
Get-ChildItem -Force
Get-ChildItem ".claude\skills"
Get-ChildItem ".claude\skills\*\SKILL.md"
```

Kansion juuressa pitää olla nämä tiedostot:

`CLAUDE.md`, `README.md`, `ASENNUS.md`, `LAAJENNUKSET.md`, `LICENSE`, `LISENSSI.md`, `haastattelu.md`, `yhteydet.md`, `.gitignore`

Ja nämä kansiot:

`.claude/`, `tausta/`, `ohjeet/`, `paatokset/`, `arkisto/`, `haastattelut/`, `tarkistukset/`, `docs/`

`.claude/skills/` alla pitää olla viisi kansiota: `aloita`, `syvenna`, `linkita`, `tarkista`, `kehita`. **Jokaisessa niistä pitää olla `SKILL.md`.** Tyhjä kansio ei riitä, ja viimeinen komento löytää täsmälleen viisi tiedostoa.

Kansiossa ei saa olla näitä: `.tmp-aios`, `aios.zip`, `.git`.

Vaiheen 1 käyttöjärjestelmätiedostot, kuten `desktop.ini`, saavat olla paikoillaan. Lista ei ole tyhjentävä niiden osalta.

---

## Vaihe 4. Jos jokin puuttuu

Älä paikkaa yksittäisiä tiedostoja äläkä väitä asennusta valmiiksi.

Poista kaikki, mitä asennus loi, eli edellisen listan tiedostot ja kansiot sekä mahdolliset `.tmp-aios` ja `aios.zip`. Jätä koskematta käyttöjärjestelmän omiin tiedostoihin. Aja sen jälkeen vaihe 2 uudestaan **toisella vaihtoehdolla** kuin ensimmäisellä kerralla. Jos A epäonnistui, kokeile B ja päinvastoin.

Tämä on ainoa tilanne, jossa saat asentaa kansioon, joka ei ole tyhjä. Vaiheen 1 sääntö ei koske omaa epäonnistunutta yritystäsi.

Jos toinenkin vaihtoehto epäonnistuu, kerro käyttäjälle mikä komento kaatui ja mitä virheilmoitus sanoi. Älä arvaa syytä.

---

## Vaihe 5. Kerro käyttäjälle mitä seuraavaksi

Sano nämä lyhyesti ja suomeksi:

1. Kansio on kasassa.
2. Hänen pitää avata **uusi keskustelu**, jotta viisi komentoa tulevat käyttöön. Nykyisessä keskustelussa ne eivät vielä näy.
3. Uudessa keskustelussa hän kirjoittaa `/aloita`. Siihen kannattaa varata puoli tuntia ja kaksi omaa kirjoittamaansa tekstiä, esimerkiksi asiakassähköposti tai tarjous.
4. Jos `/aloita` ei uudessakaan keskustelussa tee mitään, hän voi kirjoittaa sen sijaan *"lue tiedosto .claude/skills/aloita/SKILL.md ja toimi sen mukaan"*.

Älä aja `/aloita` käyttäjän puolesta äläkä täytä pohjia arvaamalla. Asennus päättyy tähän.
