# Governance for OS2BorgerPC

Dette dokument beskriver governance-modellen for vedligehold og nyudvikling af OS2BorgerPC’s kernekomponenter.

---

## Flerleverandørstrategi

OS2BorgerPC anvender en flerleverandørstrategi for både udvikling og drift.

- Flere udviklingsleverandører kan bidrage til nyudvikling og vedligehold.
- Flere driftsleverandører kan levere drift af OS2BorgerPC.

For at sikre transparens og sporbarhed er det et krav, at hele udviklingsprocessen foregår på GitHub i OS2BorgerPC’s officielle repositories.

---

## Koordinationsgruppen

Koordinationsgruppen har ansvar for:

- Prioritering og godkendelse af sager vedrørende kernekomponenterne.
- Beslutning om, hvilke sager der igangsættes.
- Bestilling af udviklingsopgaver hos udviklingsleverandører.
- Fastlæggelse af vilkår for review og test.

Udvikling på kernekomponenter må ikke påbegyndes uden koordinationsgruppens godkendelse.

---

## Sagsbehandling

### Behandling af sager

- Sager behandles i henhold til gældende backlog-principper.
- Ved større opgaver (epics) kan der være behov for:
  - Yderligere dialog med forslagsstiller
  - Nedbrydning i delopgaver
  - Inddragelse af flere anvenderkommuner
  - Dialog med styregruppen om behov og finansiering

---

## Løsningsbeskrivelse og estimering

Ved godkendelse af en sag udarbejdes en løsningsbeskrivelse, som skal indeholde:

- Funktionel beskrivelse af løsningen
- Testbare acceptkriterier
- Krav til dokumentation
- Krav til automatiseret test

Der indhentes timeestimater fra en eller flere udviklingsleverandører.

---

## Bestilling og finansiering

- Koordinationsgruppen foretager bestilling hos udviklingsleverandør.
- Forud for bestilling aftales:
  - Vilkår for review
  - Hvem der udfører review
  - Forventet tidsforbrug til review
  - Hvem der udfører funktionel test

Opgavestiller afholder omkostninger til review.

---

## Transparens og sporbarhed

Alle beslutninger, ændringer og leverancer skal være dokumenteret på GitHub for at sikre:

- Fuld sporbarhed
- Gennemsigtighed for alle interessenter
- Mulighed for samarbejde på tværs af leverandører og kommuner
