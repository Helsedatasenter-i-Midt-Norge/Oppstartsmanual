# Visual Studio Code

_Allsidig integrert utviklingsmiljø (IDE)_

---

## Extensions og andre online-tjenester

Visual Studio Code i Analyserom har ikke tilgang til Microsofts online-tjenester, som Extension Marketplace, Copilot, og IntelliSense/språkservere.

Extensions kan bli installert manuelt



### Last ned extension på en maskin med internett

På en PC med nettilgang:

1. Gå til [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/vscode)

2. Finn ønsket extension

3. Last ned extension som en `.vsix`‑fil fra [VSIX Download](https://github.pratikpathak.com/vsix-downloader/) (bruk win32-x64 versjoner)

4. Overfør `.vsix`‑filen til analyserommet via Filemail eller FileSender

### Installer extension fra fil i VS Code

I analyserommet
1. Åpne VS Code
2. Gå til Extensions‑visningen ved * klikke på Extensions‑ikonet i sidepanelet, eller trykk `Ctrl+Shift+X`

3. Klikk på … (tre prikker) øverst i Extensions‑panelet

4. Velg "Install from VSIX..."

5. Velg `.vsix`‑filen du har overført

6. Start VS Code på nytt hvis nødvendig

---

## 3. Håndtering av avhengigheter

Noen utvidelser krever andre utvidelser.

Anbefalt fremgangsmåte:
- Sjekk Marketplace‑siden for avhengigheter
- Last ned alle nødvendige `.vsix`‑filer
- Installer dem manuelt på samme måte

---

## 4. Versjonskompatibilitet (kritisk)

Utvidelser må være kompatible med VS Code‑versjonen din.

Viktig å vite:
- Utvidelsen må støtte din spesifikke VS Code‑versjon
- Inkompatible utvidelser kan:
  - Feile under installasjon
  - Bli deaktivert automatisk

✅ Tips:
- Standardiser på én VS Code‑versjon i organisasjonen


## Dokumentasjon og lenker

- [Offisiell dokumentasjon](https://code.visualstudio.com/docs)
- [Extension Marketplace](https://marketplace.visualstudio.com/VSCode)
- [VSIX Download](https://github.pratikpathak.com/vsix-downloader/)


_Last updated: 2026-06-22_
