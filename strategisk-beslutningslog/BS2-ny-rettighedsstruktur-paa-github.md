# Beslutning 2: Ny rettighedsstruktur på Github

## Status
- [x] Udkast
- [ ] Godkendt af koordinationsgruppen - Dato:
- [ ] Godkendt af styregruppen - Dato:

## Kontekst

I det nuværende setup har alle udviklere *Owner*-rettigheder i GitHub-organisationen. Dette inkluderer også personer fra eksterne leverandører, hvor der ikke længere foreligger en formel aftale om bidrag til softwareproduktet. Den nuværende rettighedsmodel giver bred adgang til alle repositories og organisatoriske indstillinger, uanset faktisk ansvar og behov.

Denne tilgang medfører øget sikkerhedsrisiko, manglende sporbarhed af ansvar. Derudover vanskeliggør det overholdelse af principper om “least privilege” og god governance.


## Beslutning

Der etableres en **team-baseret rettighedsstruktur** i GitHub-organisationen.

- Personlige rettigheder fjernes, og adgang tildeles udelukkende via teams  
- Brugere får kun adgang til de repositories, der er relevante for deres rolle  
- Rettighedsniveauer tildeles efter behov (fx *Read*, *Write* eller *Maintain*)  
- *Owner*-rettigheder begrænses til et lille antal interne nøglepersoner  
- Eksterne leverandører tildeles kun tidsbegrænset og afgrænset adgang, når der foreligger en aktiv aftale  

Denne struktur skal understøtte klar ansvarsfordeling, bedre sikkerhed og nemmere administration.


## Konsekvens

Ændringen reducerer risikoen for utilsigtede eller uautoriserede ændringer i kodebasen og organisatoriske indstillinger. Samtidig forbedres overblikket over, hvem der har ansvar for hvilke repositories.

Der vil være en kort overgangsperiode, hvor eksisterende adgange gennemgås og justeres, og hvor nogle brugere vil opleve reducerede rettigheder. På længere sigt forventes beslutningen at styrke sikkerhed, compliance og vedligeholdelse af softwareproduktet samt gøre onboarding og offboarding mere struktureret.

