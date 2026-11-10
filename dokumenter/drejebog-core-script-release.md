Kære KvalitetsIT

Jeg vil gerne booke et møde med jer. Det er obligatorisk at Sune deltager. Hvis der er andre fra KvalitetsIT som dagsordenen har relevans for, er de også velkomne.
Os2BorgerPC skal faktureres for jeres tid.

Emnet for mødet er at aftale en samarbejdsmodel og arbejdsgang for opdatering og release af admin-site og core-scripts, samt praksis for idriftsættelse hos jeres OS2BorgerPC kunder.

Baggrund: Styregruppen har besluttet at levetidsforlænge OS2BorgerPC. Dermed er det relevant at videreudvikle på produktet. Produktforvaltningen ønsker med interne medarbejderressourcer at videreudvikle produktet. 
Ud over det planlægges en ny tilbagevendende aktivitet - "Åbent Script-værksted" - der har til formål at engagere medlemmer af produktfællesskabet i vidensdeling og forbedring af produktet. Den aktivitet vil også medføre behov for produktreleases.

Dagsorden:
1. Etablering af fælles forståelse af opgaven.

2. 
Code Review: Produktforvaltningen ønsker at alle kodebidrag fra produktforvaltningen og medlemmer reviewes af KvalitesIT inden det merges ind i produktet. Hvordan bestiller vi et code review? Jeg tænker at vi bundler et antal pull requests og sender en email når vi har nok til nogle timers arbejde.

 3. Release
Når pull requests er godkendte ønsker vi at der tagges en release. Vi skal aftale om det er produktforvaltniongenb eller KvalitetsIT der releaser? Der skal laves en opskrift på hvad en release-aktiviteten indeholder ud over et tag på Github. F. eks. CHANGELOG, produktdokumentation.

 4. Idriftsætning
Nye versioner skal sættes i drift hos KLvalitetsITs kunder. I den driftsaftale som KvalitesIT har med deres driftskunder er det utydeligt om opgraderinger af OS2BorgerPC til nye versioner er inkluderet i9 driftsaftalen. Det nærmeste man kommer er afsnit 7. hvor der står:

> 7. Vedligehold
> OS2 forestår den løbende vedligehold af den leverede service OS2BorgerPC. 

Kan Servicevindue 1.+3. onsdag i hver måned evt. aftales som fast idriftsætningstidspunkt, hvis der ligger nye taggede releases klar?


6. Særligt i forhold til core scripts.
Produktforvaltningen har brug for en strammere styring af core scripts end hidtil praktiseret. Vi ønsker på en ressourceeffekltiv måde at sikre opdaterde og relevante skripts for alle medlemmer.

Følgende principper foreslås:

a. Indholdet i Globale scripts skal KUN være styret af den environment variabel der hedder CORE_SCRIPT_COMMIT_HASH. Environment variabel CORE_SCRIPT_VERSION_TAG nedlægges. Formålet er et gøre det lettere at teste ændringer til core scripts. En ny version kan indlæses uden at der er tagget en release. Desuden er det sært at have to pointere. Produktforvaltningen har lavet ændringen. Den ligger klar i en feature-branch.

b. Det skal ikke være muligt at slette individuelle core scripts fra Djangos admin-side som beskrevet her: https://os2borgerpc.os2.eu/docs/drift/globale-scripts.html
Produktet udvikles bedst hvis vi kan kommunikere entydigt om indholdet i Globale scripts. Individuel tilpasning af Globale Scripts er unødvendig og vil være en kilde til forvirring. Har man lokale behov må de imødekommes med lokale scripts.

c. Versionering på script-niveau fastholdes af hensyn til infomation til brugerne. Der skal være en changelog i beskrivelsen af scripts.

d. Opdateringer af globale scripts skal være bagudkompatible. Forstået på den måde at hvis et script er tilknyttet en gruppe med et givent parametersæt må scriptopdateringen ikke ødelægge den hidtidige virkemåde.
Nye parametre tilføjes til sidst og skal være optional.









De i involvere aktive medlemskommuner i videre
release af core script  er at vi skal have aftalt en praksis for hvordan 
Dagsorden for mødet:





# Drejebog for release af core scripts

Princip: Opdatering til eksisterende globale scripts skal være bagudkompatible. Må ikke ødelægge job log.
Princip: Indholdet i Globale scripts skal være styret af env var. Det skal ikke være muligt at slette individulle scripts. Har man lokale behov skal de addresseres via Loakel scripts.
Princip: Versionsnummer for hvert enkelt script skal fastholdes af hensyn til infomation til brugerne. Der skal være en changelog i beskrivelsen af scripts.
Pricip: Der indføres CHANGELOG for selve core-script repo.


Problem: Env var kræver i dag både et release tag og et commit hash. Det er et problem i forhold til test. Foreslået ændring. Der skal kun angives commit hash. Derved kan der testes inden release.
