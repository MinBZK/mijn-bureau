# Solution-architectuur MijnBureau (DRAFT)

Dit document beschrijft de solution architectuur van MijnBureau. MijnBureau is
een Digitale Werkomgeving voor ambtenaren samengesteld uit open-source
componenten. De nadruk van dit systeem ligt op veiligheid,
gebruiksvriendelijkheid, informatiehuishouding en digitale autonomie. Het
systeem is geïnspireerd op [OpenDesk](https://opendesk.eu/en/) en
[La-Suite](https://lasuite.numerique.gouv.fr/).

Dit document bestaat uit 4 delen:
* [Introductie](#samenvatting)
* [Business architectuur](business-architectuur.md)
* [Informatiearchitectuur](informatie-architectuur.md)
* [Technische architectuur](techniche-architectuur.md)

## Samenvatting

De architectuur is gericht op het faciliteren van een schaalbare, veilige en
gebruiksvriendelijke digitale werkomgeving waarbij goede informatie huidhouding
gewaarborgd wordt. Ook wordt alle relevante wet- en regelgeving meegenomen in
deze architectuur. Denk hierbij aan de archiefwet, Wet Open Overheid, Informatie
& cyber beveiliging regelgeving en Privacywetgeving.

De architectuur sluit waar mogelijk aan bij
[common ground](https://commonground.nl/). Common Ground is de visie die
beschrijft hoe gemeenten hun informatievoorziening willen inrichten.

MijnBureau is een toekomstgericht ecosysteem van open-source software. De
ontwikkelstrategie richt zich voornamelijk op het hergebruiken van componenten
uit OpenDesk en LaSuite, met enkele belangrijke aanpassingen die wij als
cruciaal beschouwen voor de flexibiliteit. Deze aanpassingen worden aangevuld
met specifieke onderdelen voor verbeterde integratie en zaakgericht werken. Door
maximaal hergebruik bevorderen we de efficiënte uitvoering van MijnBureau en
bevorderen we de samenwerking met onze partners.

De aanpak voor het creëren van MijnBureau is om open source-producten samen te
voegen tot een universeel applicatie platform. Dit betekent dat er een
overkoepelende structuur gemaakt wordt waar open source-producten toegevoegd
kunnen worden, en weggehaald kunnen worden. Ook moet het mogelijk zijn om te
integreren met al bestaande componenten binnen de organisatie als deze een
soortgelijke functie heeft zodat dubbelingen worden voorkomen. Deze integratie
met bestaande componenten moet via generiek gestandaardiseerde
protocollen/interfaces lopen.

Bij de selectie van componenten wordt rekening gehouden met beheerbaarheid, open
interfaces en standaarden, open-source en gebruik door partners.

## Aanleiding

Ministeries gebruiken eigen systemen om informatie te registreren en te
archiveren. Uit verschillende onderzoeken blijkt dat de huidige systemen niet
gebruiksvriendelijk zijn ingericht. Geordende vastlegging vindt pas laat plaats,
interdepartementaal samenwerken is lastig, en bewaren en vernietigen van
informatie gebeurt nog onvoldoende gecontroleerd. Daardoor is er kritiek op de
transparantie van het Rijk en lukt het vaak niet om informatieverzoeken van
burgers binnen de wettelijke termijnen af te ronden. Om dit te verhelpen hebben
4 departementen het BSW-programma gestart. Na een rapport van AC-ICT over BSW
heeft BSW OpenBSW gestart om te kijken naar OpenSource alternatieven voor de
BSW-functionaliteiten.

### Introductie Beter Samen Werken (BSW)

Het Programma Beter Samen Werken is gestart op februari 2023 en betreft een
programma van vier ministeries:

- Financiën
- Volksgezondheid, Welzijn en Sport (VWS)
- Sociale Zaken en Werkgelegenheid (SZW)
- Binnenlandse Zaken en Koninkrijksrelaties (BZK)

In het programma BSW werken vier departementen samen aan het verbeteren van de
informatiehuishouding (IHH) door het vernieuwen van de ICT-ondersteuning.
Rijksbreed is afgesproken dat andere departementen de gerealiseerde oplossing
later kunnen overnemen.

BSW wil komen tot een voor ambtenaren duidelijk betere en gebruiksvriendelijke
ondersteuning van het werkproces en de informatiehuishouding. Ook willen ze een
systeem realiseren die kan voldoen aan de
[Archiefwet](https://wetten.overheid.nl/BWBR0007376/2024-06-19) en de
[Wet open overheid](https://wetten.overheid.nl/BWBR0045754/2025-02-12).

De Doelarchitectuur van Beter Samenwerken (BSW) is het bieden van een
toekomstgerichte en robuuste basis voor de digitale informatiehuishouding van
overheidsorganisaties.

### Introductie OpenBSW

In het
[rapport](https://www.adviescollegeicttoetsing.nl/onderzoeken/documenten/publicaties/2024/09/02/advies-beter-samen-werken)
van Adviescollege ICT dat afgerond werd op mei 2024 werd aan BSW een aantal
adviezen gegeven. Een aantal van deze adviezen volgende in juni 2024 tot een
voorstel om het project Open BSW te starten als onderdeel van het BSW Programma.
De uitvoering van OpenBSW start op 1 december 2024 met de start van de
projectleider, op 1 januari 2025 start de eerste engineer.

Het project is in toenemende mate van belang als gevolg van kamer vragen rondom
de risico’s die verbonden zijn aan het gebruikt van Cloud en de autonomie van
Nederland zoals de initiatiefnota
['Wolken aan de horizon'](https://www.rijksoverheid.nl/documenten/kamerstukken/2025/01/17/kamerbrief-initiatiefnota-wolken-aan-de-horizon)
en het kamerdebat
[migraties van overheid-ICT naar het buitenland](https://www.tweedekamer.nl/debat_en_vergadering/plenaire_vergaderingen/details/activiteit?id=2024A08625).

Het doel van het originele openBSW voorstel van 2024 is om een Proof of Concept
uitwerking van Beter Samen Werken (BSW) functionaliteiten in te richten die de
autonomie van de overheid versterkt met open source. Hiervoor wordt gekeken naar
[LaSuite](https://lasuite.numerique.gouv.fr/en),
[OpenDesk](https://opendesk.eu/en/), [Common Ground](https://commonground.nl/)
en een EU-initiatief. Er is een budget van 445.000 euro. Op februari 2025 is er
een werkende uitvoering van de functionaliteiten zoals beschreven in de
BSW-architectuur voor de samenwerkruimte.

In maart 2025 worden rapporten opgeleverd aan het programma BSW met een voorstel
om pilots te starten. Het voorstel is om geselecteerde beproefde producten
verder te verkennen met gebruikers en te voldoen aan alle wet en regelgeving,
accessibility eisen etc.

De ontwikkelrichting voor de pilot is voornamelijk het hergebruik van OpenDesk
en LaSuite maar met een paar significante aanpassingen. Deze aanpassingen zijn
van cruciaal belang voor het gebruik door onze organisaties en ambtenaren. Ook
worden de suites aangevuld met specifieke onderdelen voor integratie met
informatiehuishoudingssystemen.

Deze solution architectuur is een gevolg van het voorstel voor pilots.

## Introductie architectuur

Dit document beschrijft de solution architectuur voor MijnBureau. MijnBureau is
een autonome Digitale Werkomgeving. Een groot deel van de architectuur is
geïnspireerd op de
[architectuur van OpenDesk](https://gitlab.opencode.de/bmi/opendesk-architekturkonzept/).

### Doel van dit document

Het doel is het definiëren van een oplossing voor de digitale werkomgeving met
als uitgangspunten een autonome oplossing die voldoet aan alle wet- en
regelgeving en schaalbaar is naar 60.000 gebruikers.

Dit document is bedoeld als discussie en richtinggevend document voor alle
stakeholders om MijnBureau te implementeren. Wij hopen dat personen of
organisaties die impact voelen door dit systeem mee wil werken aan dit document
en belangrijke punten willen aandragen vanuit de expertise die zij hebben.

## Lees verder
- [Business architectuur](business-architectuur.md)
- [Informatiearchitectuur](informatie-architectuur.md)
- [Technische architectuur](techniche-architectuur.md)
