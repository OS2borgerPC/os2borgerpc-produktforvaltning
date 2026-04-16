# Forslag til projektplan for Sikker Selvbetjening (OS2BorgerPC v3)

## Udkast til krav

[Teknologineutral funktionsbeskrivelse af en BorgerPC](krav.md)

Det er med udgangspunkt i den, at prototypen bygges.

## Visualisering af løsning

- TOP LAG:  Sikker Selvbetjening Config Layer Image (bygges automatisk for hvert konfigurationssetup i hver kommune) 
- MELLEM LAG: Sikker Selvbetjening Image (fælles for alle kommuner)
- BASE LAG: Fedora Silverblue base image - skal evt. udskiftes med base image fra NornNet-projektet på et tidspunkt

Hver kommune har deres eget Sikker Selvbetjening Config Layer Git repository. Her styrer de grupper og konfigurationer i yaml-config.
Når der gemmes ny config (commit) går der automatisk byggeprocesser i gang der bygger den kommunes nye image-sæt. Hver PC opdager selv at der er en ny version af det image, det er tilknyttet (f. eks. Broager Bibliotek eller Borgerservice) og hiver det ned og installerer det automatisk.

## Projektplan (Udkast)


| Deadline | Opgave | Involverede | Pris |
| :--- | :--- | :--- | :--- |
| Midt april (uge 17). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 1 | Sønderborg | Gratis |
| Primo juni (uge 23). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 2 | Sønderborg | Gratis |
| Primo juli (uge 28). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 3  | Sønderborg | Gratis |
| **Beslutningspunkt: ØNSKER VI AT FORTSÆTTE?** | - | - |
| **Ved fortsættelse** August | Eksternt code review. Vurdering af prototypens mangler i forhold til driftsparathed | Leverandør. Evt KvalitetsIT | Mindre beløb til leverandør |
| **Beslutningspunkt: ØNSKER VI AT FORTSÆTTE?** | - | - | - |
| **Ved fortsættelse** | Driftsmodning og test. Indsamling af behov fra hver kommuner der bruger OS2BorgerPC2, så vi sikrer dem kontinuerlig drift.  | Leverandør, Sønderborg | Større beløb til leverandør |

### Indhold af prototype 1

- Sikker-selvbetjening image med borgerpc-funktionalitet. Bygges med Fedora Silverblue som base-image
- Sikker-selvbetjening-config image. Hver kommune har deres eget sikker-selvbetjenings-config miljø. Der bygges et automatisk et config-image med sikker-selvbetjening som base-image for hvert konfigurationssetup i en kommune. Her ligger f. eks. printerkonfiguration, wifi config, browser indstillinger, baggrundsbilleder osv.
- Infrastruktur med automatisk byg af image

- Opsætning af Ansible repository med eksempel-playbooks til f. eks. printerinstallation.
- Service der sikrer konsistent deployment af Ansible Playbooks.

### Indhold af prototype 2
- Borger-brugeren med oprydning og autologin
- Erstatning for Tænd/sluk tidsplan
- Kiosk image

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

### Hvorfor er immutable Linux, Bootc og Ansible-pull en velegnet teknologisk platform til OS2BorgerPC V3?
Vi erstatter håndbygget kode med hyldevarer. Herunder skitseres hvordan teknologierne bringes i anvendelse og hvordan de skal forstås i forhold til nuværende begrebsunivers.

- OS2BorgerPC Admin: UDGÅR. Erstattes med standard grafisk brugergrænseflade til Ansible-pull og standardsystemer til driftsovervågning.
- OS2BorgerPC Client: UDGÅR. Erstattes med Bootc grundfunktionalitet og Ansible-pull infrastruktur.
- OS2BorgerPC Image: Image baseres på Universal Blue-projektets base image (silverblue-main). Vil skulle tilpasses med ca. 1500 linjers kode hvoraf 90% kan kopieres fra andre projekter i samme univers.
- OS2BorgerPC Kiosk Image: Baseres på et base image uden GUI. F. eks. Fedora IoT. Vil kræve ca. 500 kodelinjers tilpasning.
- OS2BorgerPC Core Scripts: UDGÅR. Funktionalitet indbygges i image. Det der ikke egner sig hertil, implementeres i Ansible playbooks. Lokale playbooks, der svarer til lokale scripts, vil kunne tilføjes af hver kommune. (~ 1000 kodelinjer)

**I alt ca. 3000 linjers kode (4% af det nuværende system)**

En lille kodebase gør det billigt og nemt at lave nye releases og alternative image versioner (som f. eks. ARM-udgaver af images eller special-distributioner som f. eks. en kursist-pc)

---

### Hvad med Nornnet-projektet, når prototypen laves med United Blue-projektets base image og byggeinfrastruktur?
For at arbejde med immutable Linux-images skal man have en byggeinfrastruktur og et base image. Uden det kommer man ingen vegne. For at komme hurtigt i gang med en OS2BorgerPC V3 prototype, giver det mening, at vi kobler os på en eksisterende infrastruktur, som er klar til brug her og nu. 

United Blue infrastrukturen er meget benyttet og populær. Kendte distributioner der bygger på den er Aurora, Bluefin og Bazzite. 
United Blue base image bygger oven på Fedora Silverblue, så vi vil relativt nemt kunne udskifte base image og byggeinfrastruktur med et andet Fedora-baseret grundlag, hvis vi ønsker det. Prototypen vil give os værdifuld indsigt i hvilke krav OS2BorgerPC-produktet stiller til et base image.

---

### Hvordan kan Sønderborg tilbyde at bygge en prototype helt gratis?
Frem til januar 2027 er Agnete mentor for en IT-studerende fra uddannelsen AspIT. Det er en IT-uddannelse, der er skræddersyet til unge med autisme. Vi har været så heldige at få en ung mand i praktik, Bartosz, der interesserer sig for Linux og er meget lærenem. Han er hos os 20 timer/uge og har OS2BorgerPC-prototypen som sin primære opgave.
