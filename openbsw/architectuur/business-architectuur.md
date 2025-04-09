# Business doel

MijnBureau heeft tot doel de ministeries en ook voor daaraan verbonden
agentschappen, inspecties en uitvoeringsinstellingen, evenals Hoge Colleges van
Staat, provincies en gemeenten in staat te stellen om werkprocessen van
ambtenaren te ondersteunen die geheel of gedeeltelijk afhankelijk zijn van een
goede informatiehuishouding, met een digitale werkomgeving. Dit willen we op een
gestandaardiseerde en autonome manier kunnen aanbieden, zodat MijnBureau een
belangrijke bijdrage zal leveren aan de modernisering van de
informatiehuishouding en de digitale autonomie van de overheid. Verder willen we
met MijnBureau de ambtenaren ondersteunen met een geavanceerd en
toekomstbestendig werkomgeving, en deze staat zou uiterlijk op de middellange
termijn moeten worden bereikt.

## Business principes

Om MijnBureau kostenefficiënt te ontwikkelen, zijn er een aantal
businessprincipes opgesteld die erop gericht zijn complexiteit en kosten in
balans te brengen. Deze principes dienen als leidraad om strategische
beslissingen te maken die zowel de effectiviteit als de financiële gezondheid
van MijnBureau waarborgen. Door systematisch complexiteit te reduceren, kunnen
processen worden gestroomlijnd, wat leidt tot aanzienlijke kostenbesparingen
zonder in te boeten op kwaliteit of innovatie

### Economische efficiëntie

Bij het selecteren en exploiteren van een componenten voor MijnBureau moeten
altijd de aspecten van economische efficiëntie en andere aspecten zoals
duurzaamheid, toegankelijkheid, etc. in acht worden genomen. Als het verwachte
voordeel onevenredig laag is in vergelijking met de kosten, dan moeten er
alternatieven worden gezocht.

### Beschikbaarheid, vertrouwelijkheid en integriteit

Beschermingsbehoeften worden doorgaans maximaal ingesteld voor de doelen van
beschikbaarheid, vertrouwelijkheid en integriteit, maar het toepassen van het
maximale niveau op alles kan leiden tot onnodige inspanningen, met name met
betrekking tot beschikbaarheid. Het bereiken van buitensporige beschikbaarheid
vereist vaak redundante technische componenten, wat kostbaar kan zijn. Daarom is
het cruciaal om de beschermingsdoelen grondig te bespreken en te evalueren. Als
ononderbroken bedrijfsactiviteiten cruciaal zijn, moet een "hoog" niveau van
beschikbaarheid worden geïmplementeerd op applicatieniveau, wat de betrokken
kosten rechtvaardigt. Als dit niet zo is, kan gekeken worden naar lagere
beschikbaarheid.

### Standaarden

Sluit aan bij wereldwijde standaarden zonder af te wijken van vastgestelde eigen
normen. Door gebruik te maken van gestandaardiseerde processen, interfaces en
data-uitwisselingsformaten wordt goede samenwerking tussen partijen mogelijk,
wat cruciaal is voor het bereiken van efficiëntie digitale werkomgeving.

## Samenwerking

MijnBureau wordt gecreëerd in een collaboratieve samenwerking waarbij wordt
samengewerkt met ministeries, gemeenten, provincies, uitvoeringsorganisaties,
collega-organisaties in andere landen en relevante open-source gemeenschappen.
De softwarebasis is samengesteld uit bestaande open source ecosystemen.

Nederland heeft in december 2024 een intentieverklaring getekend met Duitsland
en Frankrijk, ondertekend door CIO Rijk namens de staatssecretaris van BZK, om
de betrokkenheid en samenwerking op het gebied van autonome digitale
werkomgeving te formaliseren met onze Franse en Duitse collega's.

Ons doel is om een softwaresuite samen te stellen met een installatie laag die
niet alleen geschikt is voor de Rijksoverheid, maar ook herbruikbaar en
aanpasbaar is voor mede-overheden en de gehele publieke sector. Voor een
efficiënte ontwikkeling van MijnBureau is samenwerking met ervaren partners
cruciaal. We kijken daarbij naar de Franse en Duitse collega's, diverse eigen
instellingen zoals gemeenten en uitvoeringsorganisaties, en organisaties zoals
SURF die al geavanceerde componenten gebruiken die binnen MijnBureau kunnen
worden toegepast.

Verschillende overheidsorganisaties zoals SSC-ICT, DICTU en RvIHH beschikken
over uitgebreide kennis op het gebied van beheer en informatiehuishouding, die
we willen inzetten om te voldoen aan de geldende wet- en regelgeving en om
bestaande processen te hergebruiken. Samen met de levendige open-source
gemeenschap en bedrijven die open-source diensten aanbieden, kunnen we een
voortreffelijk product creëren.

### Project structuur

Het voorgestelde projectstructuur voor OpenBSW is opgesplitst in 3 niveaus:

- **Strategisch niveau**

  - Doel: Bepaal de strategie, visie en lange termijn doelen van het project.
  - Leden: vertegenwoordigers van de rijksoverheid, uitvoeringsorganisaties,
    provincies, gemeenten en belangrijke stakeholders.
  - Verantwoordelijkheden:
    - Beslist over de toewijzing van middelen en prioritering van projecten.
    - Zorgt voor afstemming met politieke en financiële doelstellingen.
    - Faciliteert een open communicatie- en besluitvormingsproces.

- **Tactisch niveau**
  - Doel: Ontwerpen van specifieke sub-componenten en bewaken van
    projectvoortgang.
  - Leden: Projectmanagers en solution architect
  - Verantwoordelijkheden:
    - Vertalen van strategische doelen naar concrete plannen en roadmaps.
    - Toezicht houden op project control mechanismen zoals tijdslijnen en
      budgetbewaking.
    - Coördineren van communicatie tussen het strategische en operationele
      niveau.
    - Architectuur principes van MijnBureau bewaken
- **Operationeel niveau**
  - Doel: Implementeren en testen van projectcomponenten.
  - Leden: Technische teams, productontwikkelaars, testers, en
    gebruikerservaringsexperts.
  - Verantwoordelijkheden:
    - Implementeren van sub-componenten in het MijnBureau systeem.
    - Zet in op continue integratie en deployment (CI/CD) voor efficiënte
      updates.
    - Faciliteren van feedback loops via een productbord, een architectuurbord,
      en een gebruikerservaringsbord.
    - Het product-, architectuur-, en gebruikerservaringsbord dienen als
      adviesorganen die voortdurend communiceren met alle deelprojecten en
      ondersteunen bij iteratieve verbeteringen.

### Fases

MijnBureau zal bestaan uit meerde componenten, voor ieder component zullen we
fases doorlopen.

- Planning – verzameling van vereisten
- Constructie – transformatie van vereisten naar dienstverlening
- Exploitatie – levering van diensten in overeenstemming met de toepasselijke
  service level agreements

## Architectuur principes

In de dynamische wereld van softwareontwikkeling vormen architectuurprincipes de
hoeksteen van een effectief en robuust systeemontwerp. Deze principes bieden
richtlijnen die ervoor zorgen dat een systeem niet alleen voldoet aan de huidige
eisen, maar ook flexibel genoeg is om toekomstige uitdagingen aan te gaan. Ze
fungeren als een leidraad voor zowel ontwikkelaars als stakeholders, en
bevorderen een gemeenschappelijk begrip en consistente besluitvorming tijdens de
levenscyclus van het softwareproject.

1. **Conformiteit met Wet- en Regelgeving**. Zorg ervoor dat het systeem voldoet
   aan alle relevante wettelijke en regelgevende vereisten. Voorbeelden hiervan
   zijn AVG, BIO2, Archiefwet en forumstandaardisatie richtlijnen.
2. **Gebruik van standaarden**. Implementeer gevestigde marktstandaarden om
   interoperabiliteit, beveiliging en innovatie te bevorderen. Voorbeelden
   hiervan zijn WebDav, CalDav en OpenID Connect.
3. **Digitale Autonomie & Leveranciersonafhankelijkheid**. Beheer en controle
   gegevens binnen geografische en juridische grenzen en minimaliseer
   afhankelijkheid van specifieke leveranciers of fabrikanten om flexibiliteit
   en keuzevrijheid te behouden. Voorbeelden zijn open data formaten zoals ODF.
   Indien mogelijk dient uitsluitend softwarecomponenten te bevatten waarvoor
   functioneel vergelijkbare producten beschikbaar zijn.
4. **Maximaliseer Hergebruik**. Bevorder het hergebruik van bestaande
   componenten en technologieën om efficiëntie te verbeteren en kosten te
   reduceren. Dit betekent dat tijdens het planning process goed gekeken moet
   worden naar mogelijke componenten die al bestaan voordat nieuwe componenten
   gemaakt worden. Als men iets nieuws maakt, probeer dan aan te sluiten bij
   bestaande standaarden tijdens de implementatie.
5. **Security by design**. Implementeer veilige configuraties en beveiliging als
   standaarduitgangspunt binnen het systeemontwerp. Beveiliging moet in iedere
   fase van de ontwikkeling meegenomen worden, Niet alleen in de ontwerpfase.
6. **Gebruikersgerichte Ontwikkeling**. Betrek gebruikers in het proces om een
   hoge bruikbaarheid en acceptatie te verzekeren. Denk hierbij aan User
   Experience onderzoeken zoals functionele geschiktheid en SUS-scores.
7. **Container native & Beheerbaar**. Adopteer een container-native ontwerp om
   optimale schaalbaarheid en flexibiliteit te bereiken. Alle componenten dienen
   beschikbaar te zijn als container-images en de implementatie moet
   plaatsvinden op containerplatforms. Hiermee wordt niet alleen de efficiëntie
   van de resource-allocatie verbeterd, maar ook de portabiliteit en het beheer
   van applicaties vergemakkelijkt. Dit container-georiënteerde benadering
   ondersteunt snelle uitrol- en updatecycli, waardoor de infrastructuur beter
   aansluit bij dynamische zakelijke behoefte
8. **Gebruik van open source software en open source samenwerkingsmodel**.
   Adopteer een open source werkmethodologie om innovatie te stimuleren en
   gemeenschapsbijdrage te bevorderen. Open source-alternatieven voor huidige
   producten moeten worden geïdentificeerd en onderdeel worden van MijnBureau om
   digitale autonomie strategy te versterken.

## Requirements

Bij het ontwikkelen van een effectieve solution-architectuur is het essentieel
om een duidelijk beeld te hebben van de requirements, ofwel de vereisten. Deze
vereisten fungeren als de fundamentele bouwstenen voor het ontwerp en de
implementatie van een systeem. Ze beschrijven wat een systeem moet doen en welke
functionaliteiten nodig zijn om aan de behoeften van de belanghebbenden te
voldoen.

### Functionele requirements

Het Proof of Concept-voorstel van OpenBSW benoemt noodzakelijke
functionaliteiten. Deze zijn als volgt:

1. Tekstverwerking, spreadsheets en presentaties
2. Chat
3. E-mail en agenda
4. Videobellen
5. Delen van bestanden

Verder blijkt uit de architectuur van BSW dat er nog belangrijke
functionaliteiten moeten worden toegevoegd, met name op het gebied van
informatie huishouding. Dit vereist de implementatie van een zaaksysteem waarin
we de bovengenoemde functionaliteiten kunnen bundelen tot één samenhangend
geheel.

Daarnaast zijn in het Proof of Concept enkele extra functionaliteiten getest,
gebaseerd op componenten uit OpenDesk en LaSuite. Deze hebben potentieel
interessante functies die niet direct noodzakelijk zijn, maar die wel extra
waarde of verbeteringen kunnen bieden en een andere manier van werken kunnen
creëren dan nu gebruikelijk is. Deze 'nice-to-have' functionaliteiten kunnen de
gebruikerservaring verrijken of het systeem aantrekkelijker maken voor
gebruikers. Enkele voorbeelden zijn:

- Gezamenlijke Notities
- Spreadsheet+
- Kennismanagement
- Projectmanagement

Het team heeft zelf ook twee extra functionaliteiten uitgetest en toegevoegd als
potentieel interessante functies:

- AI Interface: OpenWebUI
- Wachtwoord beheer: Vaultwarden

Het is essentieel dat de noodzakelijke functionaliteiten worden gerealiseerd om
het fundament van de oplossing te verzekeren en te voldoen aan de kritieke eisen
van het originele OpenBSW projectvoorstel. Deze basisfunctionaliteiten zijn
onmisbaar voor het succes van het project. Tegelijkertijd biedt de implementatie
van potentieel interessante functies een scala aan mogelijkheden om het systeem
verder te verbeteren en de gebruikerservaring te verrijken. Door strategisch te
investeren in deze optionele functies kan de organisatie niet alleen voldoen aan
de huidige behoeften, maar ook anticiperen op toekomstige wensen en innovaties
stimuleren.

### Wet- en regelgeving

In de hedendaagse digitale wereld is naleving van wet- en regelgeving een
cruciaal onderdeel van IT-architectuur en -beheer. Organisaties moeten ervoor
zorgen dat hun IT-systemen en processen in overeenstemming zijn met de geldende
juridische verplichtingen en standaarden om zowel compliance als veiligheid te
waarborgen. Dit zijn de belangrijkste wet- en regelgeving waaraan de
IT-architectuur van MijnBureau aan moet voldoen.

- AVG (GDPR): Privacywetgeving die de verwerking van persoonsgegevens reguleert
- Wet Digitale Overheid: Regels voor identificatie en gegevensuitwisseling
- BIO2: Informatie & cyber beveiliging regelgeving
- AI-Act: AI-systemen wetgeving
- Forum Standaardisatie: Standaarden vastgelegd
- Archiefwet: Levenscyclus van overheidsinformatie
- Wet Open Overheid: Transparantie wetgeving
- Wet Digitale Overheid: Veilige, toegankelijke en betrouwbare digitale
  communicatie
- NIS2: Cyber beveiliging
- NSCS: basis richtlijnen cyber security

### Non-functionele requirements

De onderliggende infrastructuurtechnologie moet een veilige en betrouwbare
werking mogelijk maken. De aangeboden diensten moeten toegankelijk zijn voor
degenen die ze nodig hebben. Storingen als gevolg van serviceonderbrekingen,
bijvoorbeeld veroorzaakt door technische fouten, moeten worden geoptimaliseerd
met behulp van technische middelen om de impact te minimaliseren waar dit een
bedrijfsrisico vormt.

Bij het plannen, levering en exploitatie van componenten moet de BIO2 maatregel
worden toegepast. Verder moet MijnBureau het mogelijk maken om de verwerking van
gevoelige persoonsgegevens en digitale geclassificeerde informatie te bewerken.
Hiervoor moeten de wettelijk verankerde technische en organisatorische vereisten
voor gegevensbescherming en geheimhoudingsbescherming worden geïmplementeerd.

Toegankelijkheid is een belangrijk aspect van de werkplek. Iedereen moet de
tools kunnen gebruiken ongeachte persoonlijke beperkingen. Om dit te bereiken
willen we voldoen aan WCAG vereisten.

## Lees verder
- [Informatiearchitectuur](informatie-architectuur.md)
- [Technische architectuur](techniche-architectuur.md)

Of keer terug naar de [hoofdpagina](index.md)
