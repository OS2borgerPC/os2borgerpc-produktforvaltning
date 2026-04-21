# Forslag til projektplan for Sikker Selvbetjening (OS2BorgerPC v3)

## Projektplan


| Deadline | Opgave | Involverede | Pris |
| :--- | :--- | :--- | :--- |
| Midt april (uge 17). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 1 | Sønderborg | Gratis |
| Primo juni (uge 23). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 2 | Sønderborg | Gratis |
| Primo juli (uge 28). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 3  | Sønderborg | Gratis |
| **Beslutningspunkt: ØNSKER VI AT FORTSÆTTE?** | - | - |
| **Ved fortsættelse** August | **Bestilling af tilstandsrapport.** Vi betaler en leverandør for at lave en grundig vurdering af prototypen og en mangelliste med overslag på, hvad det koster at udbedre. | Leverandør |Mindre beløb til tilstandsrapport |
| **Beslutningspunkt: ØNSKER VI AT FORTSÆTTE?** | - | - | - |
| **Ved fortsættelse** | **Driftsmodning.** Vi bestiller en eller flere leverandører til at bygge den færdige løsning med udgangspunkt i anbefalingerne fra tilstandsrapporten  | Leverandører | Større beløb til udvikling af driftsklart produkt |

### Indhold af prototype 1

- Sikker-selvbetjening image med borgerpc-funktionalitet. Bygges med Fedora Silverblue som base-image
- Sikker-selvbetjening-config image. Hver kommune har deres eget sikker-selvbetjenings-config miljø. Der bygges et automatisk et config-image med sikker-selvbetjening som base-image for hvert konfigurationssetup i en kommune. Her ligger f. eks. printerkonfiguration, wifi config, browser indstillinger, baggrundsbilleder osv.
- Infrastruktur med automatisk byg af image

### Indhold af prototype 2
Hvad synes I?

Forslag:
- Borger-brugeren med oprydning og autologin
- Tænd/sluk tidsplan
- Kiosk image

## Funktionelle krav

[Teknologineutral funktionsbeskrivelse af en BorgerPC](krav.md)

Det er med udgangspunkt i den, at prototypen bygges.

## Arkitektur i løsningen

Er bygget efter principperne skitseret i NornNet-projektet:

- TOP LAG:  Sikker Selvbetjening Config Layer Image (bygges automatisk for hvert konfigurationssetup i hver kommune) 
- MELLEM LAG: Sikker Selvbetjening Image (fælles for alle kommuner)
- BASE LAG: Fedora Silverblue base image - skal evt. udskiftes med base image fra NornNet-projektet på et tidspunkt

Hver kommune har deres eget Sikker Selvbetjening Config Layer Git repository. Her styrer de grupper og konfigurationer i yaml-config.
Når der gemmes ny config (commit) går der automatisk byggeprocesser i gang der bygger den kommunes nye image-sæt. Hver PC opdager selv at der er en ny version af det image, det er tilknyttet (f. eks. Broager Bibliotek eller Borgerservice) og hiver det ned og installerer det automatisk.

## Spørgsmål og svar

### Hvad er problemet med OS2BorgerPC V2 teknisk set?
Det nuværende OS2BorgerPC er kæmpestort og bygget helt fra bunden i Python kode + Django CMS. 
Hver ny release/image kræver håndholdte tilretninger mange steder i koden. Det er ressourcekrævende at holde ved lige og udvikle.

- OS2BorgerPC Admin: 68.825 linjers kode fordelt på 552 filer
- OS2BorgerPC Client: 1945 linjers kode fordelt på 34 filer
- OS2BorgerPC Image: 3688 linjers kode fordelt på 36 filer
- OS2BorgerPC Kiosk: 656 linjers kode fordelt på 22 filer
- OS2BorgerPC Core Scripts: 6118 linjers kode fordelt på 167 filer

**I alt 81.232 linjers kode**

---

### Hvorfor er immutable Linux med bootc velegnet som teknologisk platform til OS2BorgerPC V3?
Vi erstatter håndbygget kode med hyldevarer. Dvs. at der nærmest kun er konfiguration og meget lidt programkode.
Jeg har kigget på tilsvarende projekter og 

**I alt ca. 3000 linjers kode (4% af det nuværende system)**

En lille kodebase gør det billigt og nemt at lave nye releases og alternative image versioner (som f. eks. ARM-udgaver af images eller special-distributioner som f. eks. en kursist-pc)
En anden fordel er at vi fuldstændig undgår små konfigurations-forskelle mellem pcer. De er altid up-to-date på nyeste version og pcer i samme grupper, er altid helt ens. 

---


