# Contributing to OS2BorgerPC

Dette dokument beskriver processen for kodebidrag til OS2BorgerPC’s kernekomponenter.

OS2BorgerPC anvender en flerleverandørstrategi, hvor flere uafhængige udviklingsleverandører kan bidrage til den samme kodebase. For at sikre kvalitet, sporbarhed og transparens følger alle kodebidrag en fælles proces baseret på *GitHub Flow*.

Repository-oversigt:
https://github.com/os2borgerpc

---

## Overordnede principper

- Al udvikling og vedligehold foregår i OS2BorgerPC’s officielle GitHub-repositories.
- Al kode skal gennemgå review, før den kan indgå i produktet.
- Al funktionalitet skal være testbar og dokumenteret.
- Udvikling på kernekomponenter må først påbegyndes efter godkendelse fra koordinationsgruppen.

---

flowchart TD
    A[Opret Issue på GitHub] --> B[Koordinationsgruppen behandler sag]
    B -->|Afvist| C[Sag lukkes]
    B -->|Godkendt| D[Løsningsbeskrivelse og estimering]
    D --> E[Bestilling hos udviklingsleverandør]
    E --> F[Udvikling i feature branch]
    F --> G[Pull Request oprettes]
    G --> H[Code Review]
    H -->|Ændringer kræves| F
    H -->|Godkendt| I[Merge til development]
    I --> J[Funktionel test]
    J -->|Fejl| F
    J -->|Godkendt| K[Merge til main]
    K --> L[Release og dokumentation]


## Arbejdsgang for kodebidrag

### 1. Oprettelse af sag (Issue)

Der oprettes en sag (issue) på GitHub i det relevante repository.

- Alle kan oprette sager.
- Sagen skal angive, om der er tale om vedligeholdelse eller nyudvikling.
- Beskrivelsen skal være forståelig for både udviklere og anvendere af OS2BorgerPC.
- Ved nye features skal der anvendes en user story-tilgang.

**Bemærk:** Der må ikke påbegyndes udvikling, før sagen er behandlet og godkendt af koordinationsgruppen.

---

### 2. Udvikling

Når sagen er godkendt og bestilt:

- Udviklingsleverandøren tildeles adgang til at oprette feature branches i relevante repositories.
- Udvikling foretages i én eller flere feature branches.
- Leverancen afleveres via én eller flere pull requests.

Pull requests skal:
- Linke til det relevante issue.
- Indeholde en klar beskrivelse af ændringerne.
- Overholde projektets kodestandarder.

---

### 3. Review

- Al ny kode skal gennemgå review.
- Review foretages via GitHub.
- Udviklingsleverandøren retter koden i henhold til reviewerens kommentarer.
- Review afsluttes, når reviewer har godkendt pull requesten.

---

### 4. Test

Efter godkendt review merges koden til `development`-branchen.

- Koden er herefter klar til funktionel test.
- Opgavestiller tester, at acceptkriterierne er opfyldt.
- Eventuelle fejl eller mangler håndteres via GitHub issues.

---

### 5. Release

Når funktionel test er godkendt:

- Koden merges til `main`-branchen.
- Der tagges en release.
- Relevant produktdokumentation opdateres, herunder:
  - Brugerdokumentation
  - Implementeringsvejledninger
  - Eventuelle release notes
