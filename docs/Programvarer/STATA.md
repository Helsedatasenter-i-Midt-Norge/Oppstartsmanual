# STATA

_Programvarepakke for datamanipulering, visualisering, statistikk og automatisert rapportering_

---
## Lisensbruk
Statalisensene fordeles ved hjelp av en egen lisensserver. Vi har totalt 25 samtidige lisenser tilgjengelig på deling mellom alle foretakene.

Man holder på en lisens for hver gang man starter ikonet. For å unngå å oppta unødige lisenser så ber vi om at dere kun starter selve programmet en gang, og deretter heller åpner flere datasett inni selve programmet.

## Lagring av data og tilleggspakker

Filer som er lagret av brukere på analyserommets C:/ område vil av sikkerhetsmessige grunner bli slettet etter utlogging, samme som på jobb-PC fra Helse Midt Norge.  Dette betyr at ikke kun data, men også Statainnstillinger og pakker slettes om man ikke endrer område for lagring. For at pakker skal kunne gjenfinnes og gjenopprettes neste gang man logger inn må de lagres på analyserommets mappe på S:/. Av sikkerhetsmessige grunner er ikke SSC (http://fmwww.bc.edu/) eller Github tilgjengelig fra analyserom.

En del tilleggspakker har blitt installert for alle brukere. Hvis du trenger andre pakker finnes veiledning for dette nederst på denne siden.

### Tilleggspakker installert som standard i Helsedatasenter analyserom 
| Package | Main Command(s) | Description |
|--------|----------------|-------------|
| asdoc | asdoc | Exports Stata output (tables, summaries, regression results) directly to nicely formatted Word documents. |
| batplot | batplot | Agreement/diagnostic plots (similar to Bland–Altman). |
| blandaltman | blandaltman | Bland–Altman agreement plots. |
| boottest | boottest | Wild bootstrap inference for robust hypothesis testing. |
| carryforward | carryforward | Fill missing values using last observed value. |
| cem | cem | Coarsened exact matching for causal inference. |
| coefplot | coefplot | Plot regression coefficients and confidence intervals. |
| csdid | csdid | Difference-in-differences with staggered treatment timing. |
| dataex | dataex | Export example datasets for reproducibility. |
| density2 | density2 | Alternative density plotting. |
| distinct | distinct | Count unique values of variables. |
| drdid | drdid | Doubly robust difference-in-differences estimation. |
| estout | esttab, estout, estpost, estadd | Flexible regression table creation and export. |
| forestplot | forestplot | Forest plots for meta-analysis or coefficient visualization. |
| ftools | fcollapse, fegen, fmerge, etc. | Fast data manipulation utilities used internally by reghdfe. |
| gtools | gcollapse, gegen, greshape, etc. | High-performance replacements for many built-in Stata data commands. |
| hashsort | hashsort | Fast sorting using hashing. |
| ivreg2 | ivreg2 | Advanced instrumental variables estimation with robust diagnostics and tests. |
| ivreghdfe | ivreghdfe | IV/2SLS regression with high-dimensional fixed effects (combines ivreg2 + reghdfe). |
| join | join | Data merging utilities beyond built-in merge. |
| labutil suite | labmask, labvalcombine, etc. | Label manipulation utilities. |
| listwise | listwise | Identify complete-case observations. |
| metan | metan | Meta-analysis (fixed/random effects, pooling). |
| missings | missings | Tools for handling and summarizing missing data. |
| outreg2 | outreg2 | Export regression results to formatted tables (Excel/Word). |
| parallel | parallel_map | Parallel computation tools for Stata. |
| ppmlhdfe | ppmlhdfe | Poisson pseudo-ML regression with high-dimensional fixed effects (for gravity models etc.). |
| psmatch2 | psmatch2 | Propensity score matching and treatment effects estimation. |
| rangestat | rangestat | Rolling/window statistics over ranges of observations. |
| ranktest | ranktest | Weak identification and rank tests for IV models. |
| rdrobust | rdrobust, rdplot, rdbwselect | Regression discontinuity analysis toolkit. |
| reghdfe | reghdfe | Linear regression with multiple high-dimensional fixed effects. |
| reproduce | reproduce | Tools for reproducible workflows. |
| schemepack-related (grstyle) | grstyle | Custom graph styles and themes. |
| seeout / shellout | seeout, shellout | Viewing/exporting output externally. |
| stnet | stnet | Network meta-analysis tools. |
| stpm2 / stmerlin / merlin | stpm2, merlin | Flexible parametric survival models and generalized modeling framework. |
| tabout | tabout | Export formatted tables (especially descriptive stats). |
| waldtest / scoretest | waldtest, scoretest | Hypothesis testing utilities. |
| winsor2 | winsor2 | Winsorize variables (trim extreme values). |

### Sett opp katalogen på S:/ og endre Statas mappeinnstillinger 
Stata bruker flere standardkataloger. De to viktigste for brukerpakkene er: 
- PLUS → Pakker installert fra repository, osv. 
- PERSONAL → Egendefinerte ADO filer du selv lager eller legger til

PLUS og PERSONAL mapper kan sjekkes ved å kjøre

    sysdir

I Windows Utforsker, opprett en ny mappe. Forslag:

    S:/stata/ 
    S:/<prosjektnavn>/stata 

Opprett to submapper inne i mappen, f.eks.: 

    S:/stata/plus 
    S:/stata/personal

Kjør følgende i Stata

    sysdir set PLUS "S:/stata/plus" 
    sysdir set PERSONAL "S:/stata/personal"

"sysdir set" må kjøres ved hver oppstart. 

### Last ned .ado og .sthlp/.hlp filer på vanlig PC med internettilkobling

På en vanlig PC med Stata installert og internettilkobling, finn PLUS-mappen 

    Sysdir 

Installer pakker via SSC eller andre nettsider, f.eks.: 

    Ssc install «pakkenavn» 
eller

    Net install «pakkenavn» from «URL» 

Pakken og avhengigheter blir lagret i PLUS-mappen, i en submappe oppkalt etter den første bokstaven i pakkenavnet. De viktigste filene er .ado og .sthlp eller .hlp filer. 
F.eks., batplotfiler finnes i C:/stata/plus/b/ og heter batplot.ado, og batplot.sthlp 
 
### Overfør pakkefilene til Analyserom 
Med bruk av enten Filemail (ta kontakt med rådgiveren din i Helsedatasenteret) eller hvis du har tilgang, FileSender, send filene til analyserommet ditt, og legg filene i PLUS-mappen. 
Nå skal det være mulig å kjøre pakken din i Stata i Analyserom. Hvis det ikke fungerer er det mulig at flere avhengigheter trengs – les gjennom .sthlp/.hlp og .adofilene. Ta kontakt med rådgiveren din for bistand. 


## Dokumentasjon
Offisiell dokumentasjon og veiledning for Stata [finnes her](https://www.statanordic.com/StataResources.html).



_Sist oppdatert: 2026-06-18_
