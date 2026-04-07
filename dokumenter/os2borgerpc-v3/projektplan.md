# Forslag til projektplan for OS2BorgerPC v3

## Udkast til krav

Udkast til en teknologineutral funktionsbeskrivelse af en BorgerPC.
Det er med udgangspunkt i den at prototypen bygges.

[Funktionsbeskrivelse af en BorgerPC](krav.md)

## Projektplan (Udkast)


| Deadline | Opgave | Involverede | Pris |
| :--- | :--- | :--- | :--- |
| Primo juni (uge 23). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 1 | Sønderborg | Gratis |
| Primo juli (uge 28). Præsentation på koordinations- og styregruppemøde. | Prototype iteration 2  | Sønderborg | Gratis |
| August | **Beslutningspunkt: ØNSKER VI AT FORTSÆTTE?** | - | - |
| August | Eksternt code review, vurdering af prototypens mangler i forhold til driftsparathed | Leverandør. Evt KvalitetsIT | Mindre beløb til leverandør |
| **Beslutningspunkt: ØNSKER VI AT FORTSÆTTE?** | - | - | - |
| **Ved fortsættelse** | Driftsmodning og test | Leverandør, Sønderborg | Større beløb til leverandør |

### Indhold af prototype 1

- BorgerPC image baseret på Ublue silverblue-main med borgerpc-specifikke tilretninger af desktop
- Infrastruktur med automatisk byg af image og ISO baseret på UBlues image-template
- Opsætning af Ansible repository med eksempel-playbooks til f. eks. printerinstallation.
- Service der sikrer konsistent deployment af Ansible Playbooks.

### Indhold af prototype 2
- Borger-brugeren med oprydning og autologin
- Erstatning for Tænd/sluk tidsplan
- Kiosk image

### Spørgsmål og svar


- At vi bruger base image og byggeinfrastruktur fra Ublue Projektet i stedet for at vi bygger det selv jvf. NornNet projektet. Ublue er et modent stærkt community hvor man deler images til byggeinfrastruktur og...
- At vi kan rykke nu hvor vi har Bartosz
- At vi bruger ublue projektet der...

### Indhold af produktmodning
- Releasestyring
- Skrive og teste mange Ansible Playbooks (svarer til scripts)