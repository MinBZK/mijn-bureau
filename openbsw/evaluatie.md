# OpenBSW evaluatie

Er worden **technische** beproevingen gedaan van oplossingen zoals LaSuite & OpenDesk. Hieronder worden de bevindingen bijgehouden. Elke evaluatie kan op verschillende niveaus gedaan worden, namelijk:

- Proof of Concept: demobaar product maar geen security, reliability, backups, schalen en monitoring
- Pilot: werkbaar maken voor kleine gebruikersgroep, schaalbaarheid en monitoring wordt nog niet meegenomen
- Productie: Werkbare omgeving voor grote groep mensen die voldoet aan de meeste eisen zoals security, reliability etc.

Tijdens de evaluatie kijken we naar een aantal componenten. De mate waar we ernaar kijken ligt aan het niveau waarop we de evaluatie doen. Deze componenten komen uit de ISO 25010.

- Security
- Maintainability
- Flexibility
- Reliability
- Compatibility

Zoals u ziet worden er nog geen rekening gehouden met functionele geschiktheid of Prestatie-efficiëntie. Dit komt mede omdat we nog geen requirements beschikbaar hebben waaraan de producten moeten voldoen. Ook houden we nog geen rekening met Prestatie-efficiëntie omdat dat in deze fase van het project nog geen belang heeft.

## Termen

We houden een lijst van termen bij. Dit doen we zodat iedereen dezelfde definities en interpretaties gebruikt voor termen en het vermijd verwarring.

| Term                                          | Beschrijving                                                                                                                                                                       |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ARM                                           | computer processor dat simpele instructies kan uitvoeren                                                                                                                           |
| Cloud Native                                  | Aanpak voor het ontwerpen, bouwen en uitvoeren van applicaties die de voordelen van cloud computing-modellen volledig benutten.                                                    |
| Container                                     | Een applicatie die samen met al zijn afhankelijkheden, bibliotheken, configuratiebestanden en runtime-omgeving is verpakt in één enkele, portable formaat                          |
| Container registry                            | Een gecentraliseerde opslagplaats waar containers worden opgeslagen                                                                                                                |
| [DINUM](https://www.numerique.gouv.fr/dinum/) | La direction interministérielle du numérique, Franse overheids instantie                                                                                                           |
| Helm chart                                    | Een pakket met vooraf gedefinieerde Kubernetes resource configuraties die gebruikt kunnen worden om applicaties en services te installeren en te beheren op een Kubernetes-cluster |
| Kubernetes                                    | Systeem voor het automatisch uitrollen, schalen en beheren van container toepassingen                                                                                              |
| [LaSuite](https://lasuite.numerique.gouv.fr/) | samenwerk software die door de franse overheid aangeboden wordt                                                                                                                    |
| LEOS                                          | Oplossing voor het aanpassen van juridische teksten in AkomaNtoso XML-formaat                                                                                                      |
| opencode                                      | git platform voor het hosten van code door de duitse overheidwas                                                                                                                   |
| [OpenDesk](https://opendesk.eu/)              | samenwerk software die door de duitse overheid aangeboden wordt                                                                                                                    |
| SaaS                                          | Software as a Service, De oplossing wordt via het internet beschikbaar gemaakt                                                                                                     |
| [ZenDiS](https://zendis.de/)                  | Zentrum Digitale Souveränität, duitse overheids instantie                                                                                                                          |

## Evaluatie LaSuite

Momenteel worden de evaluatie van LaSuite gedaan op **Proof of concept** niveau.

### Intro

[LaSuite](https://lasuite.numerique.gouv.fr/) is de merknaam voor een groep van SaaS oplossingen die aangeboden worden door de franse overheid (DINUM) aan alle overheidsmedewerkers zoals uitvoering instanties, provincies, gemeentes, ministeries, scholen etc. De meeste applicaties zijn opensource, maar niet allemaal. Het doel is een meer efficiënte, simpele en soevereine samenwerk oplossing.

De basis van de oplossing is een Identiteits- en toegangsbeheer systeem waarbij alle overheden aangesloten zijn genaamd [ProConnect](https://github.com/numerique-gouv/proconnect-documentation). De producten worden beschikbaar gesteld over het internet en alle overheids medewerkers kunnen inloggen via het identiteits systeem en direct interdepartmental samenwerk op alle aangeboven tools.

### Componenten

LaSuite bestaat uit de componenten:

| Product          | Type                      | Onderliggend product         | source code                                                     |
| ---------------- | ------------------------- | ---------------------------- | --------------------------------------------------------------- |
| Tchap            | Chat                      | Matrix+element               | ?                                                               |
| France Transfer  | File transfer             | custom java applicatie       | https://github.com/numerique-gouv/francetransfert               |
| Webinar          | Video webinars            | BigBlueButton                | https://github.com/numerique-gouv/b3desk                        |
| WebConf          | Video Meetings            | jitsi                        | ?                                                               |
| Resana           | Office suite              | Interstis  (niet opensource) | ?                                                               |
| AudioConf        | Bellen                    | ?                            | ?                                                               |
| Grist            | Collaborative spreadsheet |  grist                       | https://github.com/numerique-gouv/helm-charts/tree/main/charts  |
| Docs             | Notities                  |  BlocNote.js                 | https://github.com/numerique-gouv/impress                       |
| Messaging        | MailBox & Calander        | ?                            | ?                                                               |

Onze Franse collegas vertelde dat ze van plan zijn de technology onder Webinar en WebConf te vervangen door [liveKit](https://github.com/livekit/livekit) - [source code](https://github.com/numerique-gouv/meet).

> Bovenstaande lijst is nog niet gevalideerd door onze Franse collegas en heeft dus nog wat onzekerheid.

### Bevindingen

De documentatie van LaSuite is moeilijk te vinden. Ook is lastig te achterhalen welke software precies draait onder de applicaties. Uiteindelijk hebben we alle repositories op github moeten analyseren die onder DINUM vallen.

Alle componenten van LaSuite worden SaaS aangeboden. Er is geen informatie beschikbaar om de volledige suite te hosten. Bij een aantal producten zijn helm charts beschikbaar die we kunnen gebruiken om die applicaties op kubernetes te installeren. We zullen dus de componenten apart moeten bekijken.

## Evaluatie OpenDesk

Momenteel worden de evaluatie van OpenDesk gedaan op **Proof of concept** niveau.

### Intro

openDesk is de aanpasbare kantoor- en samenwerkingssuite. Deze oplossing is grotendeels samengesteld door de duitse overheid. ZenDiS is de organisatie die de tool ontwikkeld. OpenDesk combineerd veel open-source producten in deze oplossing en integreert ze met elkaar. De tool heeft een sterkefocus op data soevereiniteit en veiligheid. De suite heeft versie 1.0 gerelease in oktober 2024 en wordt op moment van schrijven (december 2024) door ongeveer 600 mensen gebruikt. Versie 1.1 wordt in december 2024 gereleased.

De sourcecode voor OpenDesk is volledige beschikbaar gemaakt op [opencode](https://gitlab.opencode.de/bmi/opendesk)

Voor de evaluatie hebben we de tool v1.0 geinstalleerd op https://portal.opendesk.apps.digilab.network/

### Componenten

OpenDesk bestaat uit veel componeneten. De hoofd componenten zijn:

| Product         | Type               | OpenSource product | source code                                                                                                                                        |
| --------------- | ------------------ | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| EMail           | Email              | Open-Xchange       | https://gitlab.opencode.de/bmi/opendesk/component-code/groupware/appsuite8                                                                         |
| Calendar        | Calender           | Open-XChange       | https://gitlab.opencode.de/bmi/opendesk/component-code/groupware/appsuite8                                                                         |
| Contacts        | Contacten          | Open-XChange       | https://gitlab.opencode.de/bmi/opendesk/component-code/groupware/appsuite8                                                                         |
| Files           | Office applicaties | Collabora          | [https://gitlab.opencode.de/bmi/opendesk/component-code/office/collabora](https://gitlab.opencode.de/bmi/opendesk/component-code/office/collabora) |
| Tasks           | Taken managen      |  Open XChange      | https://gitlab.opencode.de/bmi/opendesk/component-code/groupware/appsuite8                                                                         |
| Projects        | Project Beheer     |  OpenProject       | https://gitlab.opencode.de/bmi/opendesk/component-code/project-management/openproject                                                              |
| Knowledge       | Kennis beheer      |  XWiki             | https://gitlab.opencode.de/bmi/opendesk/component-code/knowledge-management/xwiki                                                                  |
| VideoConference | Video bellen       | Jitsi              | https://gitlab.opencode.de/bmi/opendesk/component-code/realtimecommunication/nordeck                                                               |
| Chat            | Chatten            |  Element + Matrix  | https://gitlab.opencode.de/bmi/opendesk/component-code/realtimecommunication/element                                                               |
| Portal          | Overzicht          | Univention         | https://gitlab.opencode.de/bmi/opendesk/component-code/crossfunctional/univention                                                                  |
| Deployment      | Helmfile           | Helm Charts        | https://gitlab.opencode.de/bmi/opendesk/deployment/opendesk                                                                                        |

Alle informatie kan gevonden worden op [opencode](https://gitlab.opencode.de/bmi/opendesk).

### Bevindingen

- OpenDesk is redelijk gedocumenteerd. Een aantal documenten zijn in een duits wat het opzetten van OpenDesk vertraagde. Maar met de huidige vertaal oplossingen was dit geen groot probleem.
- OpenDesk is makkelijk te installeren als Proof of concept op kubernetes omdat er alleen basis kubernetes componenten gebruikt worden.
- Er zijn heel veel helm charts wat het moeilijk maakt om alle opties te overzien.
- Een aantal opties leken nog niet goed te werken als we die aan zetten zoals ReadWriteMany storage.
- Alle containers worden momenteel uit de container registry gehaald van ZenDiS. Als we deze willen aanpassen zullen we onze eigen containers moeten bouwen of opties inbouwen in de OpenDesk Containers
- OpenDesk is een totaal pakket waarbij je componenten aan en uit kan zetten.
- Momenteel worden databases en storage componenten mee gedeployed in OpenDesk als containers, deze zou je bij voorkeur afnemen van je hosting provider zodat backup direct geregeld is

Tijdens overleg met onze duitse collegas bleek dat voor het opschalen een enterprise licentie genomen moet worden die extra componenten toevoegen. Ook was de migratie van versies nog niet perfect maar daar werkte ze nu hard aan.

## Evaluatie LEOS

Momenteel worden de beproevingen van LEOS gedaan op **Proof of concept** niveau.

### Intro

LEOS is een webtool ter ondersteuning van het opstellen van wetgeving in de EU met online samenwerking, versiebeheer en co-editing. De software is ontwikkeld onder de Europese Commissie.

We hebben versie 5.1.3 uitgeprobeerd. De deployment code is beschikbaar op https://github.com/MinBZK/leos en de website draait https://leos.apps.digilab.network/

De sourcecode van LEOS is te vinden op https://code.europa.eu/leos/core

### Bevindingen

Dit zijn de bevindingen voor LEOS.

#### Generiek

- Documentatie is duidelijk voor Proof of concept. Voor productie is er weinig informatie te vinden.
- Er wordt vermeld dat een aantal belangrijke componenten uit staat om ease of use te verbeteren, maar kan nergens vinden welke componenten dit zijn en hoe ik ze wel aan zet als we de volledige ervaring willen.
- Het is onduidelijk wat Annotate en LEOS met elkaar te maken hebben (er wordt wel in de documentatie naar Annotate gerefereerd als benodigd component)
- Leos lijkt niet Cloud Native ontwikkeld te zijn.
- Er is een OpenAPI spec beschikbaar wat fijn is.

#### Performance Efficiency

Het opstarten van LEOS heeft een relatief hoge hoeveelheid cpu en memory nodig. Wij gebruiken nu 0.3 cpu en 6Gi memory bij geen load. Bij deze specs duur het ongeveer 360 seconden om op te starten. Bij minder dan 3Gi memory start de applicatie niet.

#### Security

LEOS vereist java 8.0 (2014). Java 17 and Java 21 zijn momenteel de Long-Term-Support (LTS) varianten. Oracle geeft sinds 2019 geen public updates meer voor java 8.0. Wel is er een optie voor commericial klanten om updates te krijgen als ze een java 8 licentie afnemen.

#### Maintainability

Geen bevindingen

#### Flexibility

LEOS is opensource en kan naar wens aangepast worden.

LEOS support een aantal verschillende databases en kan met JDBC geconfigureerd worden.

LEOS kan integeren met een idendity provider in SAML formaat.

i18n wordt gesupport wat meerdere talen support mogelijk maakt, default Engels en frans.

#### Reliability

Geen bevindingen

#### Compatibility

LEOS gebruik open standarden zoals het AKN4EU AkomaNtoso XML format, dit maakt het makkelijk voor andere applicaties die deze standaard supporten om de data te gebruiken.

LEOS gebruikt SAML, ik zou graag ook OpenID Connect zien.
