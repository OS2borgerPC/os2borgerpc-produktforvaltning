# [SDR] Der skal lanceres en ny version af OS2borgerPC i 2027

- **Dato**: 2025-12-02
- **Status**: Accepteret
- **Beslutningstagere**: Styregruppen-Koordinationgruppen
- **Beslutningstype**: Strategisk

## Beskrivelse af beslutningen

Der er taget en initial beslutning om at der skal lanceres en ny og fremtidssikret version af OS2borgerPC i første kvartal 2026.

- Den nye version skal baseres på genanvendelse af moderne/ tidssvarende open source løsninger,
- Den skal kunne driftes af kommunerne selv eller driftsleverandører efter eget valg.
- Der er hverken tale om opgradering eller udbedring af eksisterende kodebase, men udskiftning af denne til et nyt, vedligeholdelseslet og fremtidssikret design
- Etablering foregår i parallel med vedligehold af den eksisterende løsning.
- Løsningen skal være klar tidsnok til at der ikke er behov for at foretage en opgradering fra Ubuntu 22.04. inden standardsupporten ophører 1 april 2027. 
- Den eksisterende version af OS2borgerPC skal holdes driftssikkert i 6 måneder efter den nye løsning er implementeret i produktion, såfremt der stadig er kommuner der anvender løsningen. 
- Der skal afsættes midler i produktbudgettet til gennemførelse af behovsafklaring, POC og MVP aktiviteter

Det aftalt målbillede for udvikling og vedligehold ser ud som flg.

<img width="1404" height="565" alt="Image" src="https://github.com/user-attachments/assets/8020217e-1af9-47ae-a8f2-2d224328c53d" />

Beslutningen medfører at forarbejdet med at planlægge, design, konfigurering og implementering kan påbegyndes.

## Kontekst/ Årsag

**Årsag**

I forbindelse med kode review og hjemtagningsaktiviteterne blev det klart for Koordinationsgruppen at OS2borgerpc ville have gavn af, at man foretog gennemgribende revision og modernisering af kildekoden. Analyser har senere vist at det er alt for omkostningstungt at modernisere den eksisterende kodebase, samt at der i dag findes langt mere kost effektive open source alternativer der ude.

Da der derudover vil blive behov for en større og omkostningstung opgradering af det anvendte styresystem ( Ubuntu), blev man enige om at se sig om efter alternative løsninger.

## Konsekvenser

Beskriv hvad denne beslutning betyder fremadrettet (både godt og skidt):

- Positive: Der lanceres et nyt koncept for biblioteks pc’en i 2027 som gør det enklere og mere økonomisk at holde enhederne opgraderede, sikre og compliance. 
- Negative: nuværende brugere af OS2borgerPC version2 får ikke  opgraderet kildekoden til at kunne fungere på nyere versioner af Ubuntu, og der bliver ikke udviklet nye features til produktet i 2026.
- Neutral: Der kan lanceres en ny og fremtidssikret verison af OS2borgerPC i 2027, hvorefter OS2borgerPC v2 version kan udfases. 

## Effektuering

Der er behov for flg. i forbindelse med effektuering af beslutningen:

- Øremærkning af budgetmidler til planlægning, design og afprøvning ( POC)
- etablering af et core team og udpegning af program lead
- uarbejdelse af detailplan for POC ( target januar 2026)
- afvkling af POC ( Qg iværksættes umiddelbart derefter.

## Risici:

De væsentligste risici i forbindelse med effektuering af beslutningen er flg.:

- Den foreslåede løsningsarkitektur understøtter ikke brugssenarierne for en Biblioteks PC / Mitigeres ved gennemførelse af POC 
- Den foreslåede løsningsarkitektur understøtter ikke brugssenarierne for drift af en kommunal biblioteks pc / Mitigeres ved gennemførelse af MVP
- Den foreslåede løsningsarkitektur kræver for meget vedligehold / Mitigeres ved gennemførelse af MVP
- Den nye version af OS2borgerPC bliver ikke færdig inden standard supporten for Ubuntu 22.04 udløber: Mitigeres ved at der afsættes midler i budgettet til at tilkøbe support i 2027 for alle brugere af OS2borgerpc v2
- Etableringen af OS2borgerPC v3 drukner i diskussionen om hvorvidt den foreslåede arkitektur skal danne grundlag for andet og mere end etablering af ny biblioteks PC: mitigeres ved at OS2borgerPC selvfinanciere pos og MVP for biblioteks pc en sidenlbende med at der foretages en strategiske afklaring af om der er andre anvendelses områder for løsningens insfrastruktur komponenter. 

## Yderligere information:

- Beslutningen fremlægges til information på koordinationsgruppe mødet 02.02.2025
- Beslutningen fremlægges til ratificering på styregruppeødet  05.02.2025
- Rammer, scope og tidsplan for POC og udvikling vil bliver dokumenteret og diskuteret  i et særskilt repository ( oprettet til formålet)
- Beslutningen kan til enhver tid omgøre såfremt risici og omkostninger overstiger gevinstpotentialet.
