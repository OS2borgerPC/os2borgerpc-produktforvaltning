## Dagsorden og referat
# OS2borgerPC styregruppemøde 17.09.2026

**Status**
- [x] Referat klar til godkendelse
- [x] Referat godkendt

## Mødefakta
  
**Mødenavn**: OS2borgerpc styregruppemøde  (Afholdes sædvanligvis 1. torsdag i måneden)

**Tid**: 17.09.2026  kl. 11 - 12

**Sted**: Virtuel


#### Deltagere:
- [x] Thor Dekov Buur
- [x] Bo Mathiasen Bladmose
- [x] Per Kjær
- [x] Toke Leth Laursen
- [x] Agnete Moos (Produkt Owner)
- [x] Sofie Søndergaard (Produktkoordinator)

#### Gæster: 
- [ ] Rune Gråbæk (Gladsaxe kommune) (ændret/flyttet til forudgående koordinationsgruppemøde 7. september) 

#### Afbud:
- [ ] 

#### Faciliteret af:
- [x] Agnete Moos (Mødeleder)  
- [x] Sofie Søndergaard (Referent)  
  

 
## Dagsorden
#### 1. Formalia
- 1.1 Verificering af tilstedeværelse, mødeleder og referent
- 1.2 Godkendelse af referat og dagsorden



#### 2. Temaer for dagens møde
- 2.1 Afrunding af sikkerhedssagerne.
  - Samarbejde med Gladsaxes sikkerhedsteam.
  - Status på sikkerhedsrelease (åbne udgave af OS2BorgerPC + Magenta)
  - Kommunikation om sikkerhedssagen. 
  - [Beslutningsforslag: Midler til håndtering af akutte sikkerhedshændelser i OS2BorgerPC](https://github.com/OS2borgerPC/os2borgerpc-produktforvaltning/blob/main/beslutninger/2026-08-21-midler-til-sikkerhedshaendelser.md).
- 2.2 Godkendelse af tekst til nyhedsbrev. 
  - Sofie har skrevet et udkast til et nyhedsbrev som vi ønsker at udsende.
- 2.3 Konklusioner fra OS2Fri workshop d. 8. september og implikationer for OS2BorgerPC.
- 2.4 Risiko mitigering: Hvordan forholder vi os til end-of-life på Ubuntu 22.04 til april 2027.
  - [Beslutningsforslag: Levetidsforlængelse af OS2BorgerPC via opgradering til Ubuntu 24.04](https://github.com/OS2borgerPC/os2borgerpc-produktforvaltning/blob/main/beslutninger/2026-09-17-levetidsforlaengelse-af-os2borgerpc.md).
  
 

- 2.5 Stillingtagen til [Beslutningsforslag: Dækning af transportudgifter til møder i OS2 regi](https://github.com/OS2borgerPC/os2borgerpc-produktforvaltning/blob/main/beslutninger/2026-08-24-bevilling-af-transport-til-produktforvaltningen-til-os2-m%C3%B8der.md)
- 2.6 Orientering: Årlig regulering af takster for OS2-produkter fra 2027.



#### 3. Evt og kik til næste møde
- 3.1 Næste Styregruppemøde: Torsdag den 8. oktober


## Mødereferat

> #### 1. Formalia
> - 1.1 Verificering af tilstedeværelse, mødeleder og referent
> - 1.2 Godkendelse af referat og dagsorden
Referat godkendt efter kort gensyn. Dagsorden godkendt.



> #### 2. Temaer for dagens møde
> - 2.1 Afrunding af sikkerhedssagerne.
>   - Samarbejde med Gladsaxes sikkerhedsteam.
>   - Status på sikkerhedsrelease (åbne udgave af OS2BorgerPC + Magenta)
>   - Kommunikation om sikkerhedssagen.
>  
Agnete giver en status på sikkerhedssagerne:

I dialog mellem OS2BorgerPC’s produktforvaltning og styregruppe, Gladsaxe Kommunes IT-sikkerhedsteam og leverandørerne bag OS2BorgerPC, er sårbarhederne blevet patchet. Alle kunder hos henholdsvis Magenta og KvalitetsIT kører nu på en sikker version af admin-portalen. 

Desværre kan det ikke fuldt udelukkes, at den kritiske sårbarhed kan være blevet udnyttet, inden rettelsen blev udrullet, da ulovlig indtrængen ikke nødvendigvis efterlader spor. Ønsker man at være på den helt sikre side, er den eneste løsning at geninstallere sine BorgerPC’er. 

Styregruppen anbefaler kommunikation i nyhedsbrev samt GHSA om sikkerhedshændelsen.
Enighed om at anbefale ominstallering og skrive det direkte i nyhedsbrevet. 
Styregruppen drøftede behovet for at OS2 fællesskabet etablerer en ordning for sårbarhedsscanning af kildekoden for alle OS2 produkter. Det vil styrke kvalitet og tiltro til OS2s produkter hvis der er styr på sikkerheden fra centralt hold. Hvis sikkerhedsmonitorering skal iværksættes ude i hvert enkelt produkt vil kvaliteten blive svingende. 

>   - [Beslutningsforslag: Midler til håndtering af akutte sikkerhedshændelser i OS2BorgerPC](https://github.com/OS2borgerPC/os2borgerpc-produktforvaltning/blob/main/beslutninger/2026-08-21-midler-til-sikkerhedshaendelser.md).

Beslutningsforslag: Midler til håndtering af akutte sikkerhedshændelser i OS2BorgerPC blev besluttet. Det betyder at der afsættes 20.000 kt. til akutte sikkerhedsproblemer. 
>     
> - 2.2 Godkendelse af tekst til nyhedsbrev. 
>   - Sofie har skrevet et udkast til et nyhedsbrev som vi ønsker at udsende.
Det blev besluttet at sende nyhedsbrevet til orientering til leverandørerne Magenta og KvalitetsIT inden offentlig udsendelse.

> - 2.3 Konklusioner fra OS2Fri workshop d. 8. september og implikationer for OS2BorgerPC.
Thor orienterede kort om teknologiske valg. Tidshorisont på OS2Basis er endnu uklar. Arbejdet med SikkerSelvbetjening prototype sættes i bero indtil OS2Basis tager form. 

> - 2.4 Risiko mitigering: Hvordan forholder vi os til end-of-life på Ubuntu 22.04 til april 2027.
>   - [Beslutningsforslag: Levetidsforlængelse af OS2BorgerPC via opgradering til Ubuntu 24.04](https://github.com/OS2borgerPC/os2borgerpc-produktforvaltning/blob/main/beslutninger/2026-09-17-levetidsforlaengelse-af-os2borgerpc.md).
  
Styregruppen er indstillet på at levetidsforlænge OS2BorgerPC. Inden beslutning ønskes et revideret budget. Det blev besluttet at Thor og Agnete til næste styregruppe den 8. oktober leverer et nyt budgetudkast. 

> - 2.5 Stillingtagen til [Beslutningsforslag: Dækning af transportudgifter til møder i OS2 regi](https://github.com/OS2borgerPC/os2borgerpc-produktforvaltning/blob/main/beslutninger/2026-08-24-bevilling-af-transport-til-produktforvaltningen-til-os2-m%C3%B8der.md)

Beslutningsforslaget godkendt.
Thor foreslår at der i budget kommer en post omkring udgifter til produktforvaltning. 

> - 2.6 Orientering: Årlig regulering af takster for OS2-produkter fra 2027.

Fra 2027 træder OS2's fælles model for årlig regulering af produkternes vederlag fuldt i kraft. Det betyder, at det årlige vederlag for tilslutning til et OS2-produkt som udgangspunkt automatisk fremskrives ved årsskiftet efter KL's offentliggjorte løn- og prisskøn.

> #### 3. Evt og kik til næste møde
> - 3.1 Næste Styregruppemøde: Torsdag den 8. oktober



