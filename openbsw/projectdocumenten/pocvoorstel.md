# Project Initiatie Document
> **Beter Samen Werken**
>
> Open Source, Proof of concept.
>
> Onderdeel van Open Overheid

  Status          : Draft

  Versie          : 0.1

  Auteurs         : Rik Hooft

  Classificatie   : Publiek

  Opdrachtgever   : **persoonsgegevensweggehaald**

  Datum           : 21-1-2025


# Managementsamenvatting

Dit project is gestart na aanleiding van het advies van AcICT over het
programma BSW waarbij zij aangeven:

> *"Werk parallel aan een plan B voor die gevallen dat de conclusie ten
> aanzien van het inzetten van Microsoft 365 negatief is. Wij adviseren
> u ook om met prioriteit in EU-verband te investeren in (open source)
> alternatieven voor de langere termijn met een hoger niveau van
> digitale veiligheid.".*
>
Dit project is in toenemende mate van belang als gevolg van kamer
vragen rondom Open Source en de risico's die verbonden zijn aan de
Cloud. Het draagt bij door verschillende open source alternatief
technisch te beproeven om te komen tot een rapportage op de volgende
onderdelen:

-   Evaluatie van de beproeving, ervaringen en relatie tot de eisen in
    BSW met rapportage over de vergelijkingen met andere
    samenwerksoftware.

-   Nadere selectie van projecten om specifiek te beproeven, met analyse
    op de bruikbaarheid, risico's en verhouding tot de rest van het BSW
    project.

-   Aandachtspunten voor bredere ingebruikname waaronder implementatie,
    beheer en doorontwikkeling

Het project is gestart op 1-12-2024 en zal met een doorlooptijd van 9
maanden op 1-8-2025 zijn voltooid.

# Inhoud

[Managementsamenvatting
[3](#managementsamenvatting)](#managementsamenvatting)

[Voorwoord [6](#voorwoord)](#voorwoord)

[1 Projectdefinitie [7](#projectdefinitie)](#projectdefinitie)

[1.1 Projectdoel [7](#projectdoel)](#projectdoel)

[1.2 Gewenst projectresultaat
[7](#gewenst-projectresultaat)](#gewenst-projectresultaat)

[1.3 Gewenste einddatum [7](#gewenste-einddatum)](#gewenste-einddatum)

[1.4 Projectscope [7](#projectscope)](#projectscope)

[1.5 Niet in scope [7](#niet-in-scope)](#niet-in-scope)

[1.6 Stakeholders en hun belangen
[7](#stakeholders-en-hun-belangen)](#stakeholders-en-hun-belangen)

[2 Business Case [8](#_Toc184386520)](#_Toc184386520)

[2.1 Business case programmaplan [8](#_Toc184386521)](#_Toc184386521)

[2.2 Aanleiding van het project [8](#_Toc184386522)](#_Toc184386522)

[2.3 Overwogen opties en argumentatie voor gekozen optie
[8](#_Toc184386523)](#_Toc184386523)

[2.4 Te verwachten baten/voordelen [8](#_Toc184386524)](#_Toc184386524)

[2.5 Te verwachten kosten/nadelen [8](#_Toc184386525)](#_Toc184386525)

[2.6 Kosten-/batenanalyse [8](#_Toc184386526)](#_Toc184386526)

[3 Projectkaders [9](#projectkaders)](#projectkaders)

[3.1 Aanpak [9](#aanpak)](#aanpak)

[3.1.1 Methodische aanpak [9](#methodische-aanpak)](#methodische-aanpak)

[3.1.2 Beheer [9](#beheer)](#beheer)

[3.2 Producten [9](#producten)](#producten)

[3.3 Tijd [9](#tijd)](#tijd)

[3.4 Geld [9](#_Toc184386533)](#_Toc184386533)

[3.5 Capaciteit [9](#capaciteit)](#capaciteit)

[3.6 Projecttoleranties [9](#projecttoleranties)](#projecttoleranties)

[3.7 Randvoorwaarden [9](#randvoorwaarden)](#randvoorwaarden)

[4 Governance [10](#governance)](#governance)

[4.1 Governance programmaplan
[10](#governance-programmaplan)](#governance-programmaplan)

[4.2 Projectbesturing [10](#projectbesturing)](#projectbesturing)

[4.2.1 Kernteam [10](#kernteam)](#kernteam)

[4.2.2 Werkgroepen [10](#werkgroepen)](#werkgroepen)

[4.3 Medezeggenschap [10](#medezeggenschap)](#medezeggenschap)

[4.4 Rapportagestructuur
[10](#rapportagestructuur)](#rapportagestructuur)

[4.5 Relaties met andere projecten
[10](#relaties-met-andere-projecten)](#relaties-met-andere-projecten)

[5 Projectplan [11](#projectplan)](#projectplan)

[5.1 Kenmerken projectplanning
[11](#kenmerken-projectplanning)](#kenmerken-projectplanning)

[5.2 Bijzondere aandachtspunten
[11](#bijzondere-aandachtspunten)](#bijzondere-aandachtspunten)

[5.3 Belangrijke risico's
[11](#belangrijke-risicos)](#belangrijke-risicos)

[5.4 Productbeschrijving
[11](#productbeschrijving)](#productbeschrijving)

[5.5 Planning [11](#planning)](#planning)

[5.5.1 Product breakdown en de hoofdlijnen (producten)planning met
go/nogo momenten
[11](#product-breakdown-en-de-hoofdlijnen-productenplanning-met-gonogo-momenten)](#product-breakdown-en-de-hoofdlijnen-productenplanning-met-gonogo-momenten)

[5.5.2 Detailplanning 2025
[11](#detailplanning-2025)](#detailplanning-2025)

[5.5.3 Planning 2026 en 2027
[11](#planning-2026-en-2027)](#planning-2026-en-2027)

[6 Projectbeheersing [12](#projectbeheersing)](#projectbeheersing)

[6.1 Kenmerken projectbeheersing
[12](#kenmerken-projectbeheersing)](#kenmerken-projectbeheersing)

[6.2 Quality Assurance [12](#quality-assurance)](#quality-assurance)

[6.3 Risicomanagement [12](#risicomanagement)](#risicomanagement)

[6.3.1 Risicomatrix [12](#_Toc184119110)](#_Toc184119110)

[6.3.2 Risicolog [12](#risicomatrix)](#risicomatrix)

[6.4 Testen [12](#_Toc184386560)](#_Toc184386560)

[6.5 Configuratiemanagement [12](#section-4)](#section-4)

[6.6 Communicatie [12](#section-5)](#section-5)

[7 Bijlagen [13](#bijlagen)](#bijlagen)

# Voorwoord

In de stuurgroep is meermalen stil gestaan met welke technische
voorzieningen we invulling willen geven aan de realisatie van de
werkomgeving van de toekomst. Uitkomst van die discussie was dat voor de
korte termijn we via een aanbesteding bij leveranciers standaard
componenten van de markt gaan aanschaffen vanuit de filosofie van 'best
of breed' en een componentsgewijze opbouw van de oplossing zodat we zo
min mogelijk leveranciersafhankelijkheid hebben en dat we op later
moment de aangeschafte en/of (her)gebruikte componenten relatief
makkelijk kunnen vervangen.

Het volgt tevens het advies op van AcICT over het programma BSW waarbij
zij aangeven:

*"Werk parallel aan een plan B voor die gevallen dat de conclusie ten
aanzien van het inzetten van Microsoft 365 negatief is. Wij adviseren u
ook om met prioriteit in EU-verband te investeren in (open source)
alternatieven voor de langere termijn met een hoger niveau van digitale
veiligheid.".*

Dit projectplan betreft een Proof of Concept (PoC) rondom de
mogelijkheden van Open Source. Dit mogelijk ter vervanging van
componenten, maar ook als mitigerende maatregel voor een aantal benoemde
risico's.

De PoC heeft een exploratief karakter. Door Open Source initiatieven te
installeren en te beproeven kunnen we vertrouwen, ervaring en kennis
opbouwen dat ons gaat helpen met het definiëren van verdere stappen.

# 1 Projectdefinitie

## 1.1 Projectdoel

Het doel van open BSW is om als Proof of Concept een uitwerking van
Beter Samen Werken (BSW) functionaliteiten in te richten die de
autonomie van de overheid versterkt met Open Source.

## 1.2 Gewenst projectresultaat

#### 1.2.1 Werkende PoC

Het project richt een omgeving met geselecteerde applicaties in waaraan
de volgende eisen worden gesteld:

-   Werkend en werkbare uitwerking van BSW door maximaal hergebruik van
    Open Source oplossingen met opensourcewerken is neergezet.

-   Functionaliteit voor

    -   Tekst verwerking, spreadsheets en presentaties

    -   chat en bellen

    -   mail en agenda

    -   videobellen

    -   bestanden delen

-   Geïntegreerde samenwerkfunctionaliteit om gelijktijdig in documenten
    te werken, hier over te kunnen communiceren en deze op te slaan.

#### 1.2.2 Rapportage

Het project stelt rapportage op met de volgende inhoud:

-   Evaluatie van de beproeving, ervaringen en relatie tot de eisen in
    BSW met rapportage over de vergelijkingen met andere
    samenwerksoftware.

-   Nadere selectie van projecten om specifiek te beproeven, met analyse
    op de bruikbaarheid, risico's en verhouding tot de rest van het BSW
    project.

-   Aandachtspunten voor bredere ingebruikname waaronder implementatie,
    beheer en doorontwikkeling

#### 1.2.3 Bijdrage aan mindset wijziging

Minder hard maar niet onbelangrijk is dat het project daar waar mogelijk
de mindset wil beïnvloeden door:

-   Bij betrokkenen de boodschap laten landen dat we in staat zijn om
    binnen het Rijk delen van kantooromgeving met behulp van Open Source
    kunnen realiseren.

-   Verhoogde acceptatie van Open Source.

-   Enthousiasme en sponsorschap voor vervolgstappen

## 1.3 Gewenste einddatum

Einddatum van het project is: 1-8-2025.

## 1.4 Projectscope

-   Het uitproberen van een werkend samenwerkingssysteem naar de doelen
    van BSW als Proof Of Concept (PoC).

-   PoC bevat alle gangbare en geavanceerde maatregelen voor
    informatiebeveiliging maar word niet actief beveiligd.

-   Functionaliteit vergelijkbaar met:

    -   Microsoft Office: word processing, spreadsheets en presentaties

    -   Microsoft Teams: chat en bellen

    -   Microsoft Exchange: mail en agenda

    -   Cisco Webex: videobellen

    -   Microsoft SharePoint: bestanden delen

-   Geïntegreerde samenwerkfunctionaliteit om gelijktijdig in documenten
    te werken, hier over te kunnen communiceren en deze op te slaan.

-   Ervaring opdoen met de technische kant van deze applicaties en
    hierover bevinding vast te leggen als opmars naar eventuele pilots.

Volgende applicaties zijn in scope van het werkende samenwerkingssysteem
van deze PoC:

### [OpenDesk](https://gitlab.opencode.de/bmi/opendesk/info): Duitse kantoorsysteem

Dit project van [ZenDiS](https://zendis.de/) (Duitse ministerie voor
Binnenlandse Zaken) is een volledig alternatief voor Microsoft 365 suite
van Microsoft.

Het brengt Open Source projecten samen in een groot project waar ze
worden geïntegreerd. ZenDiS huurt de ontwikkelaars van de projecten in
om met elkaar te integreren en houd controle op het geheel. Dit maakt
dat bestaat uit losse componenten die vervangen kunnen worden.

Buiten applicaties bevat OpenDesk ook onderliggende infrastructuur zoals
inloggen met single-sign-on, gebruikersmanagement, uniforme MFA,
enzovoorts.

### [LaSuite](http://lasuite.numerique.gouv.fr/): Franse kantoorsysteem

Dit project van [DINUM](https://www.numerique.gouv.fr/dinum/) (Franse
ministerie voor Binnenlandse Zaken) tracht net als OpenDesk Open Source
oplossingen te koppelen en er een uniforme schil omheen te maken.
LaSuite is echter meer gericht op het (ook) centraal aanbieden van
werkpleksoftware en diensten 'as a service' of de onderliggende diensten
'as a service'.

### [Tchap](https://tchap.beta.gouv.fr/) en Luxchat: Franse en Luxemburgse ambtenaren communicatie app

Tchap project van DINUM biedt veilige chat en telefoneren voor alle
400.000+ Franse ambtenaren. Op het zelfde protocol is Luxchat gebouwd
van de Luxemburgse overheid.

Infrastructuren die onder de apps liggen kunnen ook door andere
applicaties gebruikt worden.

### [Common ground](https://vng.nl/rubrieken/onderwerpen/common-ground): overheidssoftware voor Nederlandse wettelijke taken

Dit door Nederlandse gemeentes en de VNG ontwikkelde systemen die
Nederlandse wettelijke taken uitvoeren. Bijvoorbeeld OpenZaak
zaaksysteem bied flexibele standaard API's voor verscheidene interfaces
en kan koppelen met meerdere documentsystemen volgens de
ZaakGerichtWerken standaard; OpenWebConcept en OpenWoo bieden content
workflows volgens de Woo; en Haven biedt Cloud standaarden voor de
Nederlandse context.

### [LEOS](https://joinup.ec.europa.eu/collection/justice-law-and-security/solution/leos-open-source-software-editing-legislation): samenwerksysteem voor wetsontwikkeling

Dit project van de Europese Commissie (DG Digit) is specifiek ontwikkeld
om tussen departementen samen te kunnen werken op wetsontwikking.

Met ondersteuning van de OSPO word er samengewerkt met de ontwikkelende
en opdrachtgevende overheden wiens projecten we hergebruiken. Dit zijn
onder andere: het Bundesministerium des Innern und für Heimat (BMI),
Zentrum für Digitale Souveränität der öffentlichen Verwaltung; direction
interministérielle du numérique, Free Software Unit; het OSPO van de
Europese Commissie; en de VNG.

## 1.5 Niet in scope

Niet in scope:

-   PoC is niet gekoppeld met bestaande systemen. Wel pad naar
    koppelingen uitgewerkt.

-   PoC is niet bedoeld om de schaal van BSW aan te kunnen, moet goed
    werken voor enkele gebruikers. Wel pad naar schaling uitgewerkt.

-   Geen of beperkte functionaliteit die van o.a. RvIHH kan worden
    hergebruikt volgens BSW zonder publieke documentatie:

    -   Document generator

    -   Zoek en Vind

    -   Tijdelijk dossier systeem

    -   Digitale handtekening

    -   Laksysteem

    -   RMA

    -   Website, email, social media en chatarchivering

-   Functionele evaluatie met eindgebruikers vind niet plaats.

-   Daadwerkelijk gebruik en actieve ondersteuning van de applicaties

-   Het treffen van security- en privacy maatregelen die o.a.
    noodzakelijk zijn om de beproefde applicaties en de omgeving aan het
    security beleid van de Rijksoverheid te laten voldoen.

-   Voldoen aan operationele eisen zoals beschikbaarheid, performance,
    ondersteuning, back-up, etc.

## 1.6 Stakeholders en hun belangen

Zie Programmaplan.

## 

# 3 Projectkaders

## 3.1 Aanpak

### 3.1.1 Methodische aanpak

Project wordt uitgevoerd op basis van:

-   [PRINCE2](https://www.axelos.com/certifications/propath/prince2-project-management)

-   [IPMA](https://www.ipmacertificeren.nl/ipma-c)

-   [Professional Scrum with
    Kanban](https://www.scrum.org/assessments/professional-scrum-with-kanban-certification)

-   [Opensourcewerken](https://www.digitaleoverheid.nl/overzicht-van-alle-onderwerpen/open-source/)

> Onder opensource werken wordt verstaan: netwerkorganisatie, maximale
> publieke transparantie, community, agile. Voor de administratie wordt
> [github](https://github.com/MinBZK/mijn-bureau/blob/main/openbsw/index.md)
> gebruiken: [🧑‍🏭 Kanban bord · Open BSW
> 📂](https://github.com/orgs/MinBZK/projects/22/views/1). Informatie
> over de status binnen de repository is publiekelijk toegankelijk.
>


### 3.1.2 Beheer

Team werkt DevOps en er is geen beheer ingeregeld tijdens de PoC. Er zal
geen incidentmanagement of ander onderdeel van [ITIL Service
Management](https://www.axelos.com/certifications/itil-service-management)
worden ingericht.

## 3.2 Producten

Zie paragraaf 1.2.

## 3.3 Tijd

> Dit project heeft een doorlooptijd van 9 maanden en is gestart op
> 1-12-2024.

## 3.5 Capaciteit

Technisch projectleider, security infra engineer en full stack engineer
zullen vanuit het [Rijks ICT
Gilde](https://www.rijksorganisatieodi.nl/rijks-ict-gilde) worden
betrokken.

## 3.6 Projecttoleranties

Bij dreigende overschrijding van onderstaande toleranties zal de
exceptie procedure in werking treden:

| Onderdeel   | Bedrag                                             |
|-------------|----------------------------------------------------|
| Geld        | +10%                                               |
| Tijd        | +1 maand                                           |
| Organisatie | Capaciteitstekort dat projectdoel in gevaar brengt |
| Kwaliteit   | Afgesproken resultaat kan niet worden gehaald      |
| Informatie  | Niet van toepassing                                |


## 3.7 Randvoorwaarden

-   PoC maakt gebruik van Open Source zoals dat geleverd wordt door
    partijen die genoemd zijn onder 2.6.

-   Verbetering en ideeën vanuit de werkgroep en anderen betrokkenen
    zullen worden verzameld en mogelijk worden gerealiseerd in de PoC
    voor zover dat nodig is voor het doel.

### Uitgangspunten

-   Partijen die kennishouder zijn van de Open Source software die
    onderdeel zijn van deze PoC zijn tijdig beschikbaar voor hulp en
    vragen
    ([EU](https://interoperable-europe.ec.europa.eu/collection/justice-law-and-security/solution/leos-open-source-software-editing-legislation),
    [La Dinum](https://www.numerique.gouv.fr/dinum/),
    [ZenDis](https://zendis.de/)).

-   Open Source componenten worden in de browser gedraaid. Er is geen
    afwijkende werkplek nodig.

-   Het project gebeurt zo veel mogelijk volgens en opensourcewerken.

-   Volgens kernprincipes digitale overheid : hergebruik, open
    standaarden, en open source.

-   Hergebruikt open source van overheden: van de Franse en Duitse open
    source samenwerksoftware en andere overheidssoftware zoals van de
    VNG en Europese Commissie.

-   Werkt waar mogelijk samen met andere overheden en geeft indien
    opportuun verbeteringen terug.

-   Geïntegreerd en voelt als 1 applicatie.

-   Houd volledige controle over alle gegevens, informatie en processen.

-   Draait op een Haven infrastructuur en kan daarmee op alle
    compatibele (eigen) clouds werken.

-   Past opensourcewerken volledig toe en draagt bij aan gebruikte
    projecten.

-   Werkt samen met een brede verscheidenheid aan stakeholders binnen de
    overheid, vergelijkbare projecten en bedrijven.

# 4 Governance 

## 4.1 Governance programmaplan

Zie Programmaplan.

## 

## 4.2 Projectbesturing

### 4.2.1 Kernteam

Het kernteam van het project bestaat uit:

| Rol                                                     | Wie                     | Taken, bevoegdheden, verantwoordelijkheden |
|---------------------------------------------------------|-------------------------|--------------------------------------------|
| Product Owner                                           | Boris       | Backlogmanagement                            |
| Scrum master                                            | Rik                | Toepassen en coachen van Professional Scrum with Kanban |
|                                                         |
| Project manager                                         | Rik                | In lijn met het Programma: managen van het project      |
| CIO/Architect                                           | Peter              | Advies                                                  |
| Engineer 1                                              | Berry        | Realisatie PoC alsmede technisch architect              |
| Engineer 2                                              | Eric  | Realisatie PoC                                          |



### 4.2.2 Werkgroepen

Doel van de werkgroep is om:

-   Concrete Ideeën voor toepassing van open source te verzamelen

-   Bij te dragen door te helpen met technische integratie aspecten

-   Vanuit hun omgeving pilots te definiëren en na te gaan hoe die
    technisch vorm kunnen worden gegeven

-   Medewerkers te stimuleren om onderdeel uit te maken van teams die
    bijdragen aan de realisatie van open source project

Deelnemers: Technisch en inhoudelijk betrokken medewerkers uit de brede
organisatie, waar onder SSC-ICT, Logius, Koop en digitale
beleidsdirecties. Het betreft vrijwillige deelname.

## 4.3 Medezeggenschap

Niet van toepassing.

## 4.4 Rapportagestructuur

Voortgangsrapportage vind plaats middels
[FCC](https://digitalesamenleving.fortes-online.com/).

## 4.5 Relaties met andere projecten

| Project of onderdeel | Relatie                                                                       |
|----------------------|-------------------------------------------------------------------------------|
| BSW                  | Project maakt hier onderdeel van uit                                          |
| La Dinum             | Project onderzoekt verdere samenwerking met het Franse Open Source initiatief |
| ZenDis               | Project onderzoekt verdere samenwerking met het Franse Open Source initiatief |

# 5 Projectplan 

## 5.1 Kenmerken projectplanning 

-   Project management conform Prince2

-   Agile, [Professional Scrum with
    Kanban](https://www.scrum.org/assessments/professional-scrum-with-kanban-certification)

-   Open Source

## 5.2 Bijzondere aandachtspunten 

Er zijn verzoeken ontvangen voor het starten van pilots. Hier wordt
momenteel actief aan gewerkt. Zodra overeenstemming wordt bereikt over
de inhoud, impact van deze pilots zal een nieuwe versie van de PiD
worden aangeboden.

## 5.3 Belangrijke risico's

plaatje verwijderd

## 5.4 Productbeschrijving

Zie paragraaf 1.2.

## 5.5 Planning 

> Zie [FCC](https://digitalesamenleving.fortes-online.com/).

### 5.5.1 Product breakdown en de hoofdlijnen (producten)planning met go/nogo momenten

| 1   | Organisatie en informatie                               |
|-----|---------------------------------------------------------|
| 1.1 | Samenwerkomgeving ingericht                             |
| 1.2 | Werkgroep ingericht                                     |
| 1.3 | Kernteam ingericht                                      |
| 1.4 | Github ingericht                                        |

| 2   | PoC uitvoeren                                           |
| 2.1 | Infrastructure bij Digi Lab obv Haven                   |
| 2.2 | TChap                                                   |
| 2.3 | OpenDesk                                                |
| 2.4 | LaSuite                                                 |
| 2.5 | Command Ground elementen                                |
| 2.6 | PoC opgeruimd                                           |

| 3   | PoC uitvoeren                                           |
| 3.1 | Evaluatie van de beproeving                             |
| 3.2 | Nadere selectie van projecten om specifiek te beproeven |
| 3.3 | Aandachtspunten voor bredere ingebruikname              |

### 5.5.2 Detailplanning 2025

> Zie [GitHub](https://github.com/orgs/MinBZK/projects/22/views/1)

### 5.5.3 Planning 2026 en 2027

> Nog niet van toepassing.

# 6 Projectbeheersing 

## 6.1 Kenmerken projectbeheersing 

| Onderdeel                                                                      | Bedrag                                                                                                             |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Geld                                                                           | Wordt op programma niveau beheerst                                                                                 |
| Tijd                                                                           | Daily Kanban, GitHub en FCC                                                                                        |
|                                                                                |
| Organisatie                                                                    | Daily Kanban                                                                                                       |
| Kwaliteit                                                                      | Daily Kanban, demo, Pull Request procedure, Prettier, vier ogen principes, Definition of Ready, Definition of done |
| Informatie                                                                     | Opbouw van de verschillende rapporten gebeurt in Github op basis van Mark Down files.                              |
| Project documentatie conform PRINCE2 vind plaats in de samenwerkingsruimte BSW |

## 6.2 Quality Assurance

Zie [Definition of Done in
GitHub](https://github.com/MinBZK/mijn-bureau/blob/main/openbsw/Definition%20of%20Done.md)

## 6.3 Risicomanagement 

[]{#_Toc184119110 .anchor}Team volgt agile werkwijze waarbij gestreefd
wordt de feedback loop zo kort mogelijk te maken en risico hoger te
prioriteren. Risico's en maatregelen worden dagelijks besproken door het
projectteam tijden de Daily Kanban.

### 6.3.1 Risicomatrix

Team volgt de standaard risico matrix met op de assen kans en effect.

### 6.3.2 Risicolog

[]{#_Toc184386560 .anchor}Administratie vindt plaats binnen
[FCC](https://digitalesamenleving.fortes-online.com/projects/#14694dd8-37a2-4cf7-bab7-77dc0d3a44ae/P2Project/219638?SetReturnAdrs=false&OpenedInMain=true)

## 6.4 Testen

Vier ogen principes geïmplementeerd middels pull requests met expliciete
controle doordat goedkeuring vereist is van de teamleden voor een merge
van een voorgestelde wijziging mogelijk wordt. Objecten die niet
opgeslagen worden in de github repository -- zoals dit plan -- worden
middels het Kanban bord in de kolom vier ogen afgestemd op uitvoering.
Verder wordt zoveel mogelijk gebruik gemaakt van geautomatiseerde tools
om kwaliteit te controleren en die ingebouwd te borgen.

## 6.5 Configuratiemanagement 

Via git als impliciet onderdeel van gitHub.

## 6.6 Communicatie 

Project zal actief gebruik maken van communicatie medewerkers op
programma niveau.

# 7 Bijlagen
