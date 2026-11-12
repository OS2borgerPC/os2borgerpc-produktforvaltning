Kære KvalitetsIT

OS2borgerPCs produktforvaltning vil gerne invitere jer til et møde om vores samarbejde og arbejdsgange for udvikling, release og idriftsættelse af nye versioner af OS2borgerPC – med særligt fokus på core-scripts og admin-sitet.

Formålet med mødet er at indgå konkrete aftaler, så OS2borgerPC i 2027 igen kan være et aktivt forvaltet produkt med løbende videreudvikling og vedligeholdelse.

Produktforvaltningen er interesseret i at købe konkrete ydelser fra KvalitetsIT, for eksempel code review af kodebidrag.

Det er vigtigt, at Sune deltager. I vurderer selv, om dagsordenen også er relevant for andre fra KvalitetsIT. KvalitetsIT kan fakturere OS2borgerPCs produktfællesskab for den medgåede tid.

## Baggrund

Styregruppen har besluttet at levetidsforlænge OS2borgerPC. Det gør det relevant at videreudvikle produktet. Produktforvaltningen ønsker at stå for denne videreudvikling med interne medarbejderressourcer. Der forventes en ny release af core-scripts og admin-sitet i december.

I 2027 planlægger vi desuden en tilbagevendende aktivitet med arbejdstitlen "Åbent scriptværksted". Formålet er at engagere medlemmer af produktfællesskabet i videndeling og videreudvikling af produktet. Aktiviteten forventes også at skabe behov for regelmæssige releases af core-scripts.

## Forslag til dagsorden

1. Valg af mødeleder og referent.

2. Kort snak om image opdatering 22.04 > 24.04 i januar.

3. Retningslinjer for bidrag

   Vi foreslår, at al udvikling af OS2borgerPC følger retningslinjerne i `CONTRIBUTING.md` og det eksisterende feature-branch-workflow: issue → pull request → code review → merge til main → release. Manuel test foretages på feature-branchen. Det svarer til den arbejdsgang, vi hidtil har fulgt.

   På et senere tidspunkt kan vi overveje Gitflow med development- og release-branches, men umiddelbart vurderer vi ikke, at der er behov for det nu.

   - Er der noget ved retningslinjerne for bidrag, vi bør drøfte eller afklare?

4. Code review

   Produktforvaltningen ønsker, at kodebidrag fra produktforvaltningen og medlemmerne bliver gennemgået af KvalitetsIT, inden de merges ind i produktet.

   - Hvordan tilrettelægger vi en effektiv arbejdsgang?
   - Skal vi samle flere pull requests, så code review kan udføres i sammenhængende arbejdspas?
   - Hvordan bestiller vi et code review – for eksempel ved at skrive til os2borgerpc@kit.dk?

5. Release

   Når pull requests er godkendt, ønsker vi at tagge en release. Vi skal aftale, om produktforvaltningen eller KvalitetsIT står for releases, og hvad releaseprocessen skal omfatte ud over at oprette et tag på GitHub – for eksempel opdatering af changelog og produktdokumentation.

   Vi foreslår, at produktforvaltningen afprøver releaseprocessen for core-scripts og admin-sitet og dokumenterer den. KvalitetsIT kan understøtte arbejdet og gennemgå releasedokumentationen.

6. Idriftsættelse

   Nye versioner skal sættes i drift hos KvalitetsITs kunder. Det er uklart, om opgradering af OS2borgerPC til nye versioner er omfattet af den driftsaftale, KvalitetsIT har med sine driftskunder. Det nærmeste, aftalen kommer på dette, er afsnit 7:

> 7. Vedligehold
> OS2 forestår den løbende vedligehold af den leverede service OS2BorgerPC. 

Kan Servicevindue 1.+3. onsdag i hver måned evt. aftales som fast idriftsætningstidspunkt, hvis der ligger nye taggede releases klar?

7. Onboarding af nye OS2borgerPC-kunder hos KvalitetsIT

   Har KvalitetsIT en intern vejledning for onboarding? Herning blev eksempelvis ikke oprettet i `os2borgerpc-admin-site-urls`.

8. Principper for core-scripts

   Produktforvaltningen har behov for en tydeligere styring af core-scripts end hidtil. Vi ønsker på en ressourceeffektiv måde at sikre, at scriptsene er opdaterede og relevante for alle medlemmer.

   Vi foreslår følgende principper:

   a. Indholdet af globale scripts styres udelukkende af miljøvariablen `CORE_SCRIPT_COMMIT_HASH`. Miljøvariablen `CORE_SCRIPT_VERSION_TAG` udfases. Det vil gøre det lettere at teste ændringer til core-scripts, fordi ændringer i et testmiljø kan indlæses fra en feature-branch, uden at der først skal tagges en release. Vi vurderer desuden, at det er uhensigtsmæssigt at have to versionsreferencer. Produktforvaltningen udarbejder ændringen og sender den som pull request til review.

    b. Det skal ikke være muligt at have flere versioner ar et core script indlæst og manuelt at slette individuelle core scripts fra Djangos admin-side som beskrevet her: https://os2borgerpc.os2.eu/docs/drift/globale-scripts.html

    Produktet udvikles bedst hvis vi kan kommunikere entydigt om indholdet i Globale scripts. Individuel tilpasning af Globale Scripts er unødvendig og bliver en kilde til forvirring. Har man lokale behov må det klares via lokale scripts. Produktforvaltningen laver ændringen og lægger den i et pull request til review.

    c. Versionering på script-niveau fastholdes af hensyn til infomation til brugerne. Der skal være en changelog i beskrivelsen på det enekelte script.

    d. Opdateringer af globale scripts skal være bagudkompatible og må ikke medføre brud på eksisterende funktionalitet. Hvis en ændring kræver breaking changes, skal der udvikles et nyt script. Scripts, der er knyttet til grupper med et bestemt parametersæt, skal fortsat kunne anvendes med dette parametersæt efter en opdatering og bevare deres hidtidige funktionelle formål.