Kære KvalitetsIT

Jeg vil gerne booke et møde med jer. Det er obligatorisk at Sune deltager. Hvis der er andre fra KvalitetsIT som dagsordenen har relevans for, er de også velkomne.
Os2BorgerPC skal faktureres for jeres tid.

Emnet for mødet er at aftale en samarbejdsmodel og arbejdsgang for opdatering og release af admin-site og core-scripts, samt praksis for idriftsættelse hos jeres OS2BorgerPC kunder.

Baggrund: Styregruppen har besluttet at levetidsforlænge OS2BorgerPC. Dermed er det relevant at videreudvikle på produktet. Produktforvaltningen ønsker med interne medarbejderressourcer at videreudvikle produktet. 
Ud over det planlægges en ny tilbagevendende aktivitet - "Åbent Script-værksted" - der har til formål at engagere medlemmer af produktfællesskabet i vidensdeling og forbedring af produktet. Den aktivitet vil også medføre behov for produktreleases.



De i involvere aktive medlemskommuner i videre
release af core script  er at vi skal have aftalt en praksis for hvordan 
Dagsorden for mødet:





# Drejebog for release af core scripts

Princip: Opdatering til eksisterende globale scripts skal være bagudkompatible. Må ikke ødelægge job log.
Princip: Indholdet i Globale scripts skal være styret af env var. Det skal ikke være muligt at slette individulle scripts. Har man lokale behov skal de addresseres via Loakel scripts.
Princip: Versionsnummer for hvert enkelt script skal fastholdes af hensyn til infomation til brugerne. Der skal være en changelog i beskrivelsen af scripts.
Pricip: Der indføres CHANGELOG for selve core-script repo.


Problem: Env var kræver i dag både et release tag og et commit hash. Det er et problem i forhold til test. Foreslået ændring. Der skal kun angives commit hash. Derved kan der testes inden release.
