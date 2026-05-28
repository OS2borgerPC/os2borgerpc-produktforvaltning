# Tillæg til krav

## Her opsamles ønsker, kommentarer og krav fra interessenter i ubearbejdet form.


Vi kom til at snakke om borgerPCere og superuser-kode. Der er princippet, at det er samme kode på mange (alle), men med sikkerhedsbriller på er det jo et ringe princip. 
Er der mon tænkt på noget med et autogenereret password pr. enhed, som så stemples ind i admin-site, så man kan slå det op efter behov (med logning på hvem der har kigget hvornår). Måske endda med at password ruller på interval, så ingen kan kende passworded uden at kigge.

*Klaus M. Sønderborg*

---

Det image til OS2borgerPC som ligger på github er den gamle Ubuntu 22.04 LTS (Jammy Jellyfish). Jeg kan se, at Magenta har opdateret til den nye version.
 
I Core image:
Slå manuel opdatering fra, så OS ikke spørger om man vil opdatere efter installation.
Status Menu mangler visning af Ubuntu versionsnummer (som i Magenta versionen).
 
Ønsker:
Mulighed for export af listerne status og computer i csv-format.
 
Mulighed for adgang til en konfigurationsfil til core-image, som vi kan overskrive med vores egen fil. I Horsens tilfælde skal den f.eks. kunne:
 
1.	Tilføje trådløstnetværk ”HK-hotspot”
2.	Hente SE-nummer med ”sudo dmidecode -s system-serial-number” og vælge det som forslag til Pc navn.
3.	Skrive ”default” som forslag til site.
4.	Vælge ”3” for Horsens.
 
*Brian H. , Horsens*

---

Fra Aarhus:

https://github.com/OS2borgerPC/os2borgerpc-produktforvaltning/blob/main/dokumenter/os2borgerpc-v3/Brugerhistorier%20om%20BorgerPC%20fra%20Aarhus.pdf

