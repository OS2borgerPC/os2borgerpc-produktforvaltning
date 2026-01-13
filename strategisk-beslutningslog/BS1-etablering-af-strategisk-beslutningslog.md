# Beslutning 1: Etablering af strategisk beslutningslog

## Status
Udkast

## Kontekst

I OS2BorgerPC produktet er der gennem tiden truffet beslutninger omkring teknologi, organisering og prioritering. 
Uden systematisk dokumentation risikerer projektet videns-tab, uklarhed om rationale bag beslutninger samt udfordringer ved onboarding af nye interessenter og ved senere revision af tidligere valg.
Der er behov for et fælles, letvægtigt og vedvarende beslutningsgrundlag. 

Arkitekturbeslutninger dokumenteres i ADR.

Det er kun beslutninger beslutninger truffet fra xxx og fremad der dokumenteres.

## Beslutning

Der etableres en strategisk beslutningslog som en fast del af projektets dokumentation. Alle væsentlige strategiske beslutninger dokumenteres løbende i loggen i et standardiseret Markdown-format med fokus på kontekst, beslutning og konsekvenser.

Beslutningsloggen versionsstyres sammen med projektets øvrige artefakter.

## Context

Produktet har brug for en strategisk beslutningslog for at vi kan dokumentere og fastholde strategiske beslutninger i softwareprojektet, så rationaler og konsekvenser er transparente over tid.

## Decision

We will use Architectural Decision Records.

We will write down the original architectural decisions as ADRs even though years have passed, to help document the
thoughts behind the project.

## Consequences

This introduces an additional burden on core project maintainers to diligently follow architecture discussions and
record the decisions in this repo as an ADR.
