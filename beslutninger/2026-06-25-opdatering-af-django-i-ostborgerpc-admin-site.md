# [ODR] Opdatering af Django til sikker patch-version i os2borgerpc-admin-site

## Beskrivelse af beslutningen

- **Dato**: 2026-06-25  
- **Status**: Udkast  
- **Beslutningstagere**: Styregruppen  
- **Beslutningstype**: Operationel  

## Kontekst / Årsag

Den nuværende version af Django anvendt i **os2borgerpc-admin-site** (4.2.11) indeholder kendte sikkerhedssårbarheder, herunder mindst tre kritiske SQL-injection sårbarheder.

Disse sårbarheder er adresseret i nyere patch-releases af Django, herunder version 4.2.30. Da der er tale om en patch-opdatering inden for samme LTS-version, vurderes opdateringen at være lavrisiko, idet den primært indeholder fejlrettelser og sikkerhedsopdateringer uden breaking changes.

For at opretholde et acceptabelt sikkerhedsniveau anbefales det at opdatere til den nyeste patch-version.

## Konsekvenser

Ved at gennemføre opdateringen:

- reduceres risikoen for udnyttelse af kendte SQL-injection sårbarheder
- forbedres den generelle sikkerhed og driftssikkerhed i løsningen
- opretholdes compliance med gængse best practices for vedligeholdelse af afhængigheder

Der forventes ikke væsentlige negative konsekvenser, da der er tale om en bagudkompatibel patch-opdatering.

## Effektuering

Såfremt beslutningen godkendes:

- Django opdateres fra version 4.2.11 til 4.2.30 i **os2borgerpc-admin-site**
- Løsningen testes for regressionsfejl og centrale funktioner verificeres
- Eventuelle nødvendige dependency-justeringer gennemføres
- Der oprettes og tagges en ny release

Derudover udarbejdes dokumentation, der beskriver:

### Opgradering for KIT-kunder
- om opgraderingen er inkluderet i eksisterende aftaler  
- hvis ikke: hvordan opgaven bestilles  
- en indikation af pris for kunderne  

Opgaven gennemføres som **Time & Material** med en maksimal økonomisk ramme på **20.000 kr.**

## Risici

- Mindre risiko for regressionsfejl i forbindelse med opdatering af dependencies
- Risiko for at kunder ikke opgraderer rettidigt, hvis proces og ansvar ikke er tydeligt beskrevet

Risiciene vurderes som begrænsede og håndterbare gennem test og tydelig kommunikation.

## Yderligere information

- Opdateringen vurderes som en nødvendig sikkerhedsforanstaltning
- Beslutningen fremlægges til godkendelse på førstkommende styregruppemøde
