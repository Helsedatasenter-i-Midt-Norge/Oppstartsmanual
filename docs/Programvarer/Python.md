# Python

_Allsidig høytnivå programmeringsspråk, mye brukt til datavitenskap, kunstig intelligens (KI) og oppgaveautomatisering._

---

## Lagring av data og installering av tilleggspakker

Filer som er lagret av brukere på analyserommets C:/ område vil av sikkerhetsmessige grunner bli slettet etter utlogging, samme som på andre Helse Midt Norge PCer.  Dette betyr at ikke kun data, men også Python innstillinger og pakker slettes om man ikke endrer område for lagring. For at pakker skal kunne gjenfinnes og gjenopprettes neste gang man logger inn må de lagres på analyserommets mappe på S:/ området. Følg punktene under for å endre mappe for lagring i Python.

Av sikkerhetshensyn er pypi.org og andre arkiver ikke tilgjengelige fra analyserom, men man kan installere pakker fra disse arkivene manuelt.

### Last ned pakker i .whl format på vanlig internet tilkoblet PC

##### Enkeltvis
Søk etter pakkene du trenger fra en nettside, f. eks. https://pypi.org/. 
Last ned som .whl (“Wheel”) format som er tilpasset versjonen av Python du skal bruke. I en vanlig HelseDS analyserom er dette: 

**Python versjon:** 3.11 

**OS:** Windows 

**ISA:** AMD64 

![PyPi](bilder/PyPi1.jpg)![PyPi](bilder/PyPi2.jpg)

##### Laste ned `.whl`-filer fra `requirements.txt`

Start på en PC med internett, og sørg for at Python-prosjektet ditt kjører som forventet.

Lag `requirements.txt`. Åpne terminal i prosjektmappen og kjør:

      pip freeze > requirements.txt

Dette oppretter en fil med alle avhengigheter og eksakte versjoner.

Opprett mappe for wheel-filer

      mkdir wheels
Last ned riktige `.whl`-filer for målmiljøet (Python 3.11, Windows, AMD64)

    pip download -r requirements.txt --only-binary=:all: --platform win_amd64 --python-version 311 --implementation cp --abi cp311 -d wheels

Dette vil:
- Laste ned alle avhengigheter
- Kun hente `.whl`-filer kompatibilt med Windows 64-bit og Python 3.11

### Endre banen for pakkeinstallering i analyserom
Hvis det ikke finnes allerede, opprett mappen du vil installere pakker i (f. eks. `S:\PythonLibs`). Det er mulig å gjøre dette i Python, men man kan også gjør det i Windows filutforsker. 
  
I Windows PowerShell (eller kommandotolken du foretrekker), endre PYTHONPATH slik at Python leter i to mapper for pakker – den du har opprettet, og den på C:\. Dette må man gjøre i hver analyserom sesjon.  
      
    $env:PYTHONPATH= "S:\PythonLibs;C:\Program Files\Python311\Lib\site-packages" 
I Python Shell kan man sjekke hvilken PYTHONPATH som er i bruk. 

    python
    import sys 
    print(sys.path) 
    exit() 


### Overfør filer til analyserom og installer

Overfør til analyserom med hjelp av Filemail eller FileSender
- requirements.txt
- wheelsfiler eller mappen

##### Enkeltvis
Kjør (bytt ut wheel filbanen og target installeringsbanen)

    pip install s:\libs\numpy.2.3.2-cp311-cp311-win_amd64.whl --target s:\pythonlibs --no-index
Denne kommandoen finner .whl filen lokalisert i den spesifiserte banen, og installerer det til banen spesifisert i --target alternativet.

##### Fra `requirements.txt` 
Kjør (bytt ut wheel filbanen og target installeringsbanen)

    pip install --find-links=./wheels -r requirements.txt --target s:\pythonlibs --no-index
Denne kommandoen finner .whl filene lokalisert i den spesifiserte banen, og installerer det til banen spesifisert i --target alternativet.

---

## Nyttige pip install alternativer
    --upgrade #Oppgrader pakken til den nyeste versjonen 
    --find-links s:\pythonlibs #bytte ut banen med den du ønsker – legg til en mappebane (f.eks. s:\pythonlibs) for å lete etter dependencies i den lokale mappen 
    --no-deps #Hopp over installasjon av dependencies (hvis du vet at de allerede er installerte) 
    --no-index #Stopper pip i å søke i PyPi

## Dokumentasjon og lenker
- [Official Python 3.11 dokumentasjon](https://docs.python.org/3.11/)
- [PyPI package repository](https://pypi.org/)


_Sist oppdatert: 2026-06-19_