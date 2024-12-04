# OpenBSW

Proof of Concept van een uitwerking van Beter SamenWerken functionaliteiten
in te richten die de autonomie van de overheid versterkt met open source.

## Uitgangspunten

- Volgens [kernprincipes digitale overheid](https://www.rijksoverheid.nl/documenten/rapporten/2023/12/22/geactualiseerde-werkagenda-waardengedreven-digitaliseren-2024):
  hergebruik, open standaarden, en open source.
- Hergebruikt open source van overheden: van de Franse en Duitse open source
  samenwerksoftware en andere overheidssoftware zoals van de VNG en
  Europese Commissie.
- Werkt waar mogelijk samen met andere overheden en geeft indien opportuun
  verbeteringen terug.
- Geïntegreerd en voelt als 1 applicatie.
- Houd volledige controle over alle gegevens, informatie en processen.
- Draait op een Haven infrastructuur en kan daarmee op alle compatibele
  (eigen) clouds werken.
- Past opensourcewerken volledig toe en draagt bij aan gebruikte projecten.
- Werkt samen met een brede verscheidenheid aan stakeholders binnen de
  overheid, vergelijkbare projecten en bedrijven.
- Sluit aan bij andere beleidsdoelstellingen uit de werkagenda en onder andere
  programma’s Digitale Gemeenschapsgoederen, Open Source, Open op Orde,
  Grenzeloos Samenwerken en Data bij de Bron.

## Gewenste eindresultaten

- Werkend en werkbare uitwerking van BSW door maximaal hergebruik van
  open source oplossingen met opensourcewerken is neergezet.
- Evaluatie van de beproeving, ervaringen en relatie tot de eisen in BSW met
  rapportage over de vergelijkingen met andere samenwerksoftware.
- Nadere selectie van projecten om specifiek te beproeven, met analyse op de
  bruikbaarheid, risico’s en verhouding tot de rest van het BSW project.
- Aandachtspunten voor bredere ingebruikname waaronder implementatie,
  beheer en doorontwikkeling.

## Project scope en afbakening

- Het uitproberen van een werkend samenwerkingssysteem naar de doelen van
  BSW als Proof Of Concept (PoC).
- PoC is niet gekoppeld met bestaande systemen. Wel pad naar koppelingen
  uitgewerkt.
- PoC is niet bedoeld om de schaal van BSW aan te kunnen, moet goed werken
  voor enkele gebruikers. Wel pad naar schaling uitgewerkt.
- PoC bevat alle gangbare en geavanceerde maatregelen voor
  informatiebeveiliging maar word niet actief beveiligd.
- Functionaliteit vergelijkbaar met bekende kantoorsoftware
- Geïntegreerde samenwerkfunctionaliteit om gelijktijdig in documenten te
  werken, hier over te kunnen communiceren en deze op te slaan.
- Geen of beperkte functionaliteit die kan worden hergebruikt
  volgens BSW zonder publieke documentatie.

## Beoogde projecten voor hergebruik

### [OpenDesk](https://gitlab.opencode.de/bmi/opendesk/info): Duitse kantoorsysteem

Dit project van ZenDiS (Duitse ministerie voor Binnenlandse Zaken) is een volledig
alternatief voor Microsoft 365 suite van Microsoft.

Het brengt open source projecten samen in een groot project waar ze worden
geïntegreerd. ZenDiS huurt de ontwikkelaars van de projecten in om met elkaar te
integreren en houd controle op het geheel. Dit maakt dat bestaat uit losse
componenten die vervangen kunnen worden.

Buiten applicaties bevat OpenDesk ook onderliggende infrastructuur zoals inloggen
met single-sign-on, gebruikersmanagement, uniforme MFA, enzovoorts.

### [LaSuite](http://lasuite.numerique.gouv.fr/): Franse kantoorsysteem

Dit project van DINUM (Franse ministerie voor Binnenlandse Zaken) tracht net als
OpenDesk open source oplossingen te koppelen en er een uniforme schil omheen
te maken. LaSuite is echter meer gericht op het (ook) centraal aanbieden van
werkpleksoftware en diensten ‘as a service’ of de onderliggende diensten ‘as a
service’.

### [Tchap en Luxchat](https://vng.nl/rubrieken/onderwerpen/common-ground): Franse en Luxemburgse ambtenaren communicatie app

Tchap project van DINUM biedt veilige chat en telefoneren voor alle 400.000+
Franse ambtenaren. Op het zelfde protocol is Luxchat gebouwd van de
Luxemburgse overheid.

Infrastructuren die onder de apps liggen kunnen ook door andere applicaties
gebruikt worden.

### [Common ground](https://vng.nl/rubrieken/onderwerpen/common-ground): overheidssoftware voor Nederlandse wettelijke taken

Dit door Nederlandse gemeentes en de VNG ontwikkelde systemen die
Nederlandse wettelijke taken uitvoeren. Bijvoorbeeld OpenZaak zaaksysteem bied
flexibele standaard API’s voor verscheidene interfaces en kan koppelen met
meerdere documentsystemen volgens de ZaakGerichtWerken standaard;
OpenWebConcept en OpenWoo bieden content workflows volgens de Woo; en
Haven biedt Cloud standaarden voor de Nederlandse context.

### [LEOS](https://joinup.ec.europa.eu/collection/justice-law-and-security/solution/leos-open-source-software-editing-legislation): samenwerksysteem voor wetsontwikkeling

Dit project van de Europese Commissie (DG Digit) is specifiek ontwikkeld om
tussen departementen samen te kunnen werken op wetsontwikking.

## Business case

Dit project is een begin om de kennis op te bouwen die nodig is om een
werkomgeving aan te bieden waarmee voldaan kan worden aan het beleid en de
[verplichtte Exit strategie](https://open.overheid.nl/documenten/ronl-734f947ec6465e4f75a56bed82fe64a1135f71a8/pdf). Dit is een essentiële eerste stap in een begrip krijgen
van de mitigatiemogelijkheden rondom de risico’s van de SaaS transitie van onze
ICT-systemen.

## Betrokken partijen

Voor het borgen en opbouwen van interne kennis die nodig is om verdere
beslissingen te nemen wordt samengewerkt door de organisaties die aan de lat
staan voor BSW en hun interne ICT dienstverleners.

Met ondersteuning van de OSPO word er samengewerkt met de ontwikkelende en
opdrachtgevende overheden wiens projecten we hergebruiken. Dit zijn onder
andere: het Bundesministerium des Innern und für Heimat (BMI), Zentrum für
Digitale Souveränität der öffentlichen Verwaltung; direction interministérielle du
numérique, Free Software Unit; het OSPO van de Europese Commissie; en de
VNG.

Daarnaast wordt er ontwikkeld samen met een grote groep collega’s uit de
organisaties die gebruik maken van BSW, zo hebben we een breed klankbord en
kunnen aannames snel worden getest. De digitale beleidsdirecties worden
betrokken gedurende het gehele proces.

## Projectaanpak

De kern van het project is een ‘werkgroep’ van bevlogen technisch aangelegde
collega’s die de organisatie begrijpen en sturing kunnen geven en af en toe bij
kunnen dragen, bijgestaan door een projectteam dat vol gaat voor het afleveren
van een sterk resultaat. Tevens zal er een klankbord opgezet worden van niet
technische medewerkers die moeten werken met de oplossingen en deze kunnen
beoordelen op gebruiksvriendelijkheid en in hoeverre de beproefde applicaties in
het werk kunnen voorzien.

Met het oog op het strategisch en langere termijn belang is het belangrijk te
trachten de verkenning en ontdekkingen te laten doen door interne medewerkers
die bekend zijn met de organisatie en de kennis binnen de organisatie kunnen
verder brengen.

Aangezien BSW een bredere reikwijdte heeft dan een ICT dienstverlener wordt de
PoC in eerste instantie opgezet op bij een relatief onafhankelijke partij. Deze
laatste heeft de capaciteit en ontwikkelmethode om dit snel op te kunnen zetten.
Belangrijk is wel dat tenminste RvIHH en SSC-ICT betrokken zijn. Dit met
betrekking tot de verbinding met de bestaande systemen, kennis van zaken en
kennisopbouw.
