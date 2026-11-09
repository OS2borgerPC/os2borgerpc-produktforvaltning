# Drejebog for release af core scripts

Princip: Opdatering til eksisterende globale scripts skal være bagudkompatible. Må ikke ødelægge job log.
Princip: Indholdet i Globale scripts skal være styret af env var. Det skal ikke være muligt at slette individulle scripts. Har man lokale behov skal de addresseres via Loakel scripts.
Princip: Versionsnummer for hvert enkelt script skal fastholdes af hensyn til infomation til brugerne. Der skal være en changelog i beskrivelsen af scripts.
Pricip: Der indføres CHANGELOG for selve core-script repo.


Problem: Env var kræver i dag både et release tag og et commit hash. Det er et problem i forhold til test. Foreslået ændring. Der skal kun angives commit hash. Derved kan der testes inden release.
