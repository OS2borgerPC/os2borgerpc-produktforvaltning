# Forslag til projektplan for OS2BorgerPC v3

## Udkast til krav

Udkast til en teknologineutral funktionsbeskrivelse af en BorgerPC.
Det er med udgangspunkt i den at prototypen bygges.

[Funktionsbeskrivelse af en BorgerPC](krav.md)


| Deadline | Opgave | Involverede | Pris |
| :--- | :--- | :--- | :--- |
| Præsenteres på koordinationsgruppemøde og styregruppemøde den. | Prototype iteration 1 | Sønderborg | 0 kr. |
| | Prototype iteration 2 | Sønderborg | 0 kr. |
| **ÆNSKER VI AT FORTSÆTTE** | Code Review og vurdering prototypens af driftsparathed | | |
| | Vurdering af base image og byggeplatformens egenthed til drift | Leverandør. Evt KvalitetsIT | Mindre beløb til leverandør |
| **ØNSKER VI AT FORTSÆTTE** | Driftsmodning og test | Leverandør, Sønderborg | Større beløb til leverandør |

### Indhold af prototype 1
- BorgerPC image baseret på Ublue vv
- Infrastruktur med automatisk byg af image og ISO baseret på UBlue projektet
- Opsætning af Ansible repository med eksempel playbooks (Erstatter scripts – både globale og lokale)
- Service der sikrer konsistent deployment af Ansible Playbooks via Bootc baseret reset, der rydder op i `/etc` og `/var`. (Erstatter OS2BorgerPC klienten – men meget meget bedre!)

### Indhold af prototype 2
- Borger-brugeren med oprydning og autologin
- Tænd/sluk tidsplan
- Kiosk image

### Forudsætninger
- At vi bruger base image og byggeinfrastruktur fra Ublue Projektet i stedet for at vi bygger det selv jvf. NornNet projektet. Ublue er et modent stærkt community hvor man deler images til byggeinfrastruktur og...
- At vi kan rykke nu hvor vi har Bartosz
- At vi bruger ublue projektet der...

### Indhold af produktmodning
- Releasestyring
- Skrive og teste mange Ansible Playbooks (svarer til scripts)