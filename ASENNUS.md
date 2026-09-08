# Asennusohje

*Tämä tiedosto on tekoälylle. Ihmisen ohje on [docs/opas.md](docs/opas.md).*

Sinua on pyydetty asentamaan Yrittäjän AI-käyttöjärjestelmä käyttäjän kansioon. Tee vaiheet järjestyksessä. Valitse vaiheessa 2 yksi polku ja pysy siinä.

---

## Vaihe 1. Varmista kohde

Olet käyttäjän omassa kansiossa. Katso mitä siellä on.

Kansio on tyhjä myös silloin, kun siellä on vain käyttöjärjestelmän omia tiedostoja: `desktop.ini`, `.DS_Store`, `Thumbs.db`. Ne eivät estä asennusta.

Kysy käyttäjältä ennen kuin jatkat, jos kansiossa on mitä tahansa muuta. Älä koskaan asenna tätä kansioon, jossa on käyttäjän muita töitä.

Jos kansiossa on jo `CLAUDE.md` ja `.claude/skills/aloita/`, paketti on jo asennettu. Älä asenna uudestaan. Kerro käyttäjälle, että kansio on jo kunnossa ja että hän voi kirjoittaa `/aloita`.

---

## Vaihe 2. Nouda ja pura paketti

Kaksi polkua. **Kokeile polkua A ensin.** Jos git puuttuu tai clone epäonnistuu mistä tahansa syystä, siirry polkuun B. Älä sekoita polkuja keskenään, koska ne tuottavat eri kansiorakenteen.

Aja komennot kokonaisina lohkoina. Ne on kirjoitettu niin, että piilotiedostot `.claude/` ja `.gitignore` siirtyvät mukana. Ilman niitä komennot eivät toimi, ja tavallinen `mv .tmp-aios/* .` jättää ne siirtämättä.

### Polku A: git

```bash
git clone --depth 1 https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma.git .tmp-aios
rm -rf .tmp-aios/.git
cp -a .tmp-aios/. .
rm -rf .tmp-aios
```

Tässä polussa arkiston sisältö on suoraan `.tmp-aios`-kansion juuressa. Väliin ei tule ylimääräistä kansiota.

`.git` poistetaan ennen kopiointia. Älä siirrä sitä käyttäjän kansioon missään vaiheessa. Käyttäjä ei tarvitse tämän repon historiaa, ja siirretty `.git` kytkisi hänen kansionsa tähän repoon.

### Polku B: arkiston lataus

Windowsissa:

```powershell
Invoke-WebRequest -Uri "https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/archive/refs/heads/main.zip" -OutFile "aios.zip"
Expand-Archive -Path "aios.zip" -DestinationPath ".tmp-aios" -Force
Get-ChildItem -Path ".tmp-aios\yrittajan-ai-kayttojarjestelma-main" -Force | Move-Item -Destination "." -Force
Remove-Item ".tmp-aios", "aios.zip" -Recurse -Force
```

Macissa ja Linuxissa:

```bash
curl -L -o aios.zip https://github.com/infopolkuai-rgb/yrittajan-ai-kayttojarjestelma/archive/refs/heads/main.zip
unzip -q aios.zip -d .tmp-aios
cp -a .tmp-aios/yrittajan-ai-kayttojarjestelma-main/. .
rm -rf .tmp-aios aios.zip
```

Tässä polussa arkiston sisällä on yksi kansio nimeltä `yrittajan-ai-kayttojarjestelma-main`. Komennot siirtävät sen sisällön, eivät kansiota itseään.

---

## Vaihe 3. Tarkista

Aja tämä ja katso tuloste:

```bash
ls -a
ls .claude/skills
ls .claude/skills/*/SKILL.md
```

Kansion juuressa pitää olla nämä tiedostot:

`CLAUDE.md`, `README.md`, `ASENNUS.md`, `LAAJENNUKSET.md`, `LICENSE`, `LISENSSI.md`, `haastattelu.md`, `yhteydet.md`, `.gitignore`

Ja nämä kansiot:

`.claude/`, `tausta/`, `ohjeet/`, `paatokset/`, `arkisto/`, `haastattelut/`, `tarkistukset/`, `docs/`

`.claude/skills/` alla pitää olla viisi kansiota: `aloita`, `syvenna`, `linkita`, `tarkista`, `kehita`. **Jokaisessa niistä pitää olla `SKILL.md`.** Tyhjä kansio ei riitä.

Kansiossa ei saa olla näitä: `.tmp-aios`, `aios.zip`, `.git`.

Jos jokin puuttuu, hae puuttuva osa uudestaan äläkä väitä asennusta valmiiksi.

---

## Vaihe 4. Kerro käyttäjälle mitä seuraavaksi

Sano kolme asiaa, lyhyesti ja suomeksi:

1. Kansio on kasassa.
2. Hänen pitää avata **uusi keskustelu**, jotta viisi komentoa tulevat käyttöön. Nykyisessä keskustelussa ne eivät vielä näy.
3. Uudessa keskustelussa hän kirjoittaa `/aloita`. Siihen kannattaa varata puoli tuntia ja kaksi omaa kirjoittamaansa tekstiä, esimerkiksi asiakassähköposti tai tarjous.

Lisää vielä yksi lause: jos `/aloita` ei uudessakaan keskustelussa tee mitään, hän voi kirjoittaa sen sijaan *"lue tiedosto .claude/skills/aloita/SKILL.md ja toimi sen mukaan"*.

Älä aja `/aloita` käyttäjän puolesta äläkä täytä pohjia arvaamalla. Asennus päättyy tähän.
