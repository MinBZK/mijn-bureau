# Technology architectuur

De technologiearchitectuur beschrijft de architectuurelementen voor de opbouw en
exploitatie van de IT-infrastructuur. Het definieert de basis waarop applicaties
kunnen worden gekozen, geïntegreerd en geëxploiteerd en vormt daarmee de basis
van de technische implementatie.

Als basis platform voor MijnBureau wordt een
[haven](https://haven.commonground.nl/) compliant Kubernetes distributie
verwacht. Implementatie op andere CNCF-certified Kubernetes distributies moet
ook makkelijk mogelijk zijn.

## Introductie

MijnBureau is een op Kubernetes gebaseerde, open-source en cloud-native digitale
werkpleksuite. Het is ontworpen om functionele componenten te kunnen vervangen
door uw eigen gehoste oplossing, zoals identiteitsbeheer en portal, die vaak al
in organisaties aanwezig zijn.

MijnBureau wordt in eerste instantie opgebouwd uit componenten van LaSuite en
OpenDesk op een fit-for-purpose manier. De suite kan ingericht worden om te
werken met bestaande Identity systemen van de organisatie of de suite kan zelf
een identity systeem uitrollen.

Het platform zal open-source componenten samenbrengen tot één systeem, met als
groot verschil ten opzichte van andere oplossingen dat het meer flexibiliteit
biedt aan organisaties om componenten te verwisselen en te integreren met hun
bestaande systemen, waar dit realistisch is.

### Componenten

Tijdens de Proof of concept van OpenBSW zijn veel componenten van onze partners
beproeft. We stellen voor om een agile procedure te volgen waarbij we eerst een
minimal viable product maken van MijnBureau met de volgende functies

| Function            | Functional Component | Code                                             | Upstream Documentation                                        |
| ------------------- | -------------------- | ------------------------------------------------ | ------------------------------------------------------------- |
| Chat                | Element              | [v1.127](https://github.com/element-hq/synapse/) | [documentation](https://element-hq.github.io/synapse/latest/) |
| Portal              | Bureaublad           | [1.0.1](https://github.com/MinBZK/bureaublad)    |                                                               |
| Identity management | KeyCLoak             | [26.1.4](https://github.com/keycloak/keycloak/)  | [Documentation](https://www.keycloak.org/documentation)       |

Daarna kunnen we de volgende componenten bekijken en toevoegen in de volgorde
die gewenst is en de meeste waarde creëert.

| Function                                     | Functional Component                                                       |
| -------------------------------------------- | -------------------------------------------------------------------------- |
| File management                              | [Nextcloud Files](https://nextcloud.com/files/)                            |
| File management                              | [Drive](https://github.com/suitenumerique/drive)                           |
| Notes                                        | [Docs](https://github.com/suitenumerique/docs/tree/v2.6.0)                 |
| Spreadsheet, presentation & document editing | [Collabora Online](https://www.collaboraonline.com/collabora-online/)      |
| Email, Agenda & Tasks                        | [OX App Suite](https://www.open-xchange.com/products/ox-app-suite)         |
| Cases                                        | [OpenZaak](https://github.com/open-zaak/open-zaak)                         |
| Spreadsheet & More                           | [Grist](https://www.getgrist.com/)                                         |
| Video calling                                | [Meet](https://github.com/suitenumerique/meet)/[Jitsi](https://jitsi.org/) |
| AI Assistant                                 | [OpenWebUI](https://docs.openwebui.com/)                                   |
| AI LLM Modellen                              | [ollama](https://ollama.com/)                                              |

Hoewel niet alle componenten perfect geschikt zijn voor gebruik in containers,
is een van de doelstellingen van het project om de applicaties af te stemmen op
best practices op het gebied van containerontwerp en -gebruik. Als tussentijds
blijkt dat een component toch niet geschikt is kunnen we deze vervangen door een
ander component.

Microservice-gebaseerde technologieën moeten worden gebruikt waarvoor open
source-componenten beschikbaar zijn met een open source licentie. Permissieve
licenties hebben de voorkeur.

Projecten van de Cloud Native Computing Foundation krijgen voorrang. Projecten
met een hogere maturiteit dienen voorrang te krijgen, in de volgorde
'Graduated', 'Incubating' en 'Sandbox'. Zodra projecten worden stopgezet
("gearchiveerd"), MOET er een alternatieve implementatie worden gezocht.

Het is essentieel om zowel hoge snelheid als hoge betrouwbaarheid tegelijkertijd
te implementeren. Deze aanpak vereist volledige automatisering, waarbij alleen
beslissingen over releases handmatig worden genomen. Handmatige configuraties
worden op geen enkel moment uitgevoerd.

Om een hoge kwaliteit te waarborgen hebben we voor een component een aantal non
functionele eisen neergezet. Deze zijn indicatief zodat er een bepaalde
verwachting gezet is.

| non functional           | Level                                                                             |
| ------------------------ |-----------------------------------------------------------------------------------|
| Functionele geschiktheid | product voldoet aan 90% van vereiste functies die verwacht worden door gebruikers |
| Compatibiliteit          | Ondersteunt laatste versie van 3 browsers (Firefox, edge & chrome)                |
| Gebruiksvriendelijkheid  | SUS-score minimaal 75 uit gebruikers onderzoek                                    |
| Gebruiksvriendelijkheid  | Minder dan 5% fouten bij kritieke taken                                           |
| Gebruiksvriendelijkheid  | Maximaal 30% langer dan benchmark                                                 |
| Gebruiksvriendelijkheid  | Minimaal wettelijke WCAG-score                                                    |
| Beveiliging              | Maximaal 5 kritieke kwetsbaarheden per release                                    |
| Onderhoudbaarheid        | Minimaal 80% testdekking                                                          |
| Onderhoudbaarheid        | Heeft mogelijkheid tot gebruik van open metrics, logs en traces                   |

## Deployment

De operationele omgevingen voor MijnBureau moeten volledig automatisch
aangemaakt kunnen worden. Conform de architectuur worden Kubernetes Pods, en
bijbehorende componenten uitgerold als applicaties met behulp van Infrastructure
as code (IaC) zoals Helm Charts, CDK8S of Kubernetes operator. Voor MijnBureau
moet 1 standard systeem gekozen worden. Op langere termijn kan er support komen
voor meerdere IaC mogelijkheden. De IaC moeten als onderdeel van de applicatie
worden gezien en moeten tevens via de CI/CD-pipeline worden getransporteerd en
gecontroleerd. De installatie stap kan handmatig gebeuren maar het moet ook
mogelijk om om dit op een GitOPS manier te doen met tools zoals flux of ArgoCD.

Als onderlaag wordt een haven compliant Kubernetes cluster verwacht. Voor nu
gaan we ervan uit dat deze kunnen worden afgenomen van leveranciers.

Alle services waarvoor voldoende reken-, opslag- en netwerkbronnen beschikbaar
zijn, MOETEN automatisch kunnen worden gestart als MijnBureau geïnstalleerd of
geüpgraded wordt.

Voor Haven compliant Kubernetes cluster zijn een aantal vereisten vastgelegd.
Als een organisatie kiest voor een andere CNCF compliant Kubernetes cluster hou
er dan rekening mee dat de volgende vereisten nodig zijn voor MijnBureau:

1. Er moet een Container Storage Interface (CSI) beschikbaar zijn met een
   standaard storage class
2. Er moet een IngressController beschikbaar zijn die netwerk toegang geeft
3. Er moeten AMD64 containers deployed kunnen worden.
4. Er moeten load balancers voor UDP zijn
5. Er moet een certificate manager beschikbaar zijn
6. (optioneel) GPUs voor AI modellen

MijnBureau gebruikt veel verschillende technologieën zoals caching, databases,
object storage, AI modellen, transactionele email & Queues. Deze kunnen deployed
worden als service bij een provider, maar mijnBureau kan ook zelf deze
componenten deployen. Als MijnBureau zelf de componenten uitrolt moet dit
mogelijk zijn zonder operators te gebruiken voor de componenten zodat het
mogelijk is om MijnBureau uit te rollen zonder admin rechten op het hele
cluster.

## Operations

De operations en development van een applicatie beschrijven hoe een applicatie
van source code naar operation wordt gebracht. Er zijn 8 fases:

1. planning: beschrijving van functie van de toepassing
2. programmeren: maken van code voor programma en lokaal testen
3. bouwen: Opbouwen van artefacten en automatisch testen
4. test: verdere accessability en integratie testen.
5. release: publiceren van artifact
6. uitrollen: beschikbaar maken van product in productie
7. operations: live operation
8. monitoren: meten van latency, load etc.

fase 3 tot 8 zijn volledig geautomatiseerd. Uitzonderingen zijn testen die niet
geautomatiseerd kunnen worden en de manuele trigger van het uitrollen van het
product.

Gezien het grote aantal componenten en de daaruit voortvloeiende mogelijke
combinaties, is automatisering essentieel, zowel wat betreft de snelheid van het
implementatieproces, als de betrouwbaarheid. Alleen geautomatiseerde installaties
kunnen worden gereproduceerd en herhaald. Om goed te meten hoe de software
delivery van MijnBureau gaat, worden DORA metrics bijgehouden voor MijnBureau in
de omgevingen.

Zelfs complexe technologieën moeten snel en betrouwbaar kunnen worden
geïmplementeerd, ongeacht de operator. Er wordt gebruik gemaakt van gevestigde
standaardtechnologieën. Veilig beheer MOET eenvoudig mogelijk zijn. Security by
default MOET makkelijk mogelijk zijn.

Om een hoge kwaliteit te waarborgen hebben we voor het development en operations
team een aantal non-functionele eisen neergezet. Deze zijn indicatief zodat er
een bepaalde verwachting gezet is. Iedere operator is natuurlijk vrij om zijn
eigen SLA af te spreken met zijn afnemers. Wij hebben voor nu de volgende
gekozen.

| non functional                      | Level                                                  |
| ----------------------------------- | ------------------------------------------------------ |
| beschikbaar Performance efficiëntie | responstijd van gemiddelde 300ms (p95)                 |
| Performance                         | Kan 1000 verzoeken per seconde                         |
| Betrouwbaarheid                     | support (9 tot 5, exclusief weekend)                   |
| Betrouwbaarheid                     | MTBF 1 week                                            |
| Betrouwbaarheid                     | MTTR 8 uur                                             |
| Betrouwbaarheid                     | Beschikbaarheid 98%                                    |
| Betrouwbaarheid                     | RPO 4 uur                                              |
| Betrouwbaarheid                     | RTO 8 uur                                              |
| Beveiliging                         | Alle containers moeten gescande worden op kwetsbaarheden |
| Onderhoudbaarheid                   | Heeft declaratieve monitoring en alerting              |

Voor observability doeleinde moeten dashboards gemaakt worden die voldoende
informatie geven over de suite.

## Applicaties

Onder applicaties verstaan we een of meer microservices, geïmplementeerd als
container, die samenwerken om een functionaliteit te verzorgen. Het configureren
van deze applicaties moet flexibel genoeg zijn om bij verschillende
overheidsorganisaties te kunnen draaien en kan via verschillende infrastructure
as code mogelijkheden geïnstalleerd worden. Dit kunnen HelmCharts zijn maar zou
ook door middel van CDK8S kunnen gebeuren.

Alle infrastructure as code (IaC) MOET versioned en signed zijn zodat
gevalideerd kan worden dat het de correcte IaC is.

De containers zouden ontwikkeld kunnen zijn volgens de
[Twelve-Factor APP](https://12factor.net/). Alleen 1 process zou moeten bestaan
in een container en er zouden geen additionele applicaties beschikbaar moeten
zijn binnen de container. Idealiter wordt een statisch binair bestand gebruikt
als applicatie in een container. Een minimale omgeving is ook toegestaan, maar
probeer deze wel te minimaliseren.

De IaC tool die gebruikt wordt voor de installatie van MijnBureau (Helm of
CDK8s) combineert de containers met configuratie bestanden en code om een
complete applicatie neer te zetten. Voor Helm charts kan men HelmFiles gebruiken
om alle applicaties te combineren tot 1 suite, Voor CDK8s kan een eigen yaml
ingelezen worden in de applicatie. Hierdoor wordt het hele MijnBureau geleverd
door een configurable infrastructure as code systeem en kan deze geautomatiseerd
geïnstalleerd en geüpdate worden, maar ook goed geversioned. Het moet in de
configuratie mogelijk zijn om applicaties aan of uit te zetten, maar ook om
alternatieve applicaties mee te geven die al beschikbaar zijn binnen de
organisatie die dezelfde gestandaardiseerde interface ondersteund als de
originele tool.

Een applicatie moet volledig beschikbaar zijn naar installatie. Dit betekent dat
ook het netwerk zoals ingress, services en load balancer, maar ook certificaten
en storage geregeld moet worden door de infrastructure as code implementatie.

Ook moet er in de Infrastructure as code effort zitten in de security, dit
betekent dat er vanuit gegaan moet worden dat er een deny all network policy is,
en dat alle componenten expliciet toegang tot elkaar moeten krijgen. Verder moet
er continue gescand worden of de infrastructure as code security best practices
handhaaft zodat het risico op security incidenten laag blijft. Er zijn vele
tools beschikbaar die dit kunnen doen. Het team mag zelf kiezen welke security
scanning tool ze prefereren.

Verder moet de IaC getest worden met een tool zoals
[conftest](https://www.conftest.dev/) of soortgelijk om aan te tonen dat de
correcte manifesten gegenereerd worden en er voldaan kan worden aan security
policies.

Alle artefacten zoals container images zijn opgeslagen in een repository die
publiekelijke beschikbaar is. Iedere week moeten en security checks gedaan
worden op deze artefacten.

## uitrol van suite

Zodra er een nieuwe release gemaakt wordt van de suite worden voor alle
containers een software bill of material gemaakt. Dit kan in het SPDC of
CyclonDX formaat. De SBOM moet gesigned zijn.

Het uitrol process MOET volledig geautomatiseerd mogelijk zijn door middel van
gitops. Ook moet een rollback mogelijk zijn. De rollout wordt door een service
provider gedaan.

DataStorage kan gedaan worden door Kubernetes, maar het product moet flexibel
genoeg zijn om externe DataStorage te gebruiken. Een voorbeeld hiervan is een
Database as a Service. Als de keuze gemaakt wordt om een Kubernetes externe
service af te nemen moet een platform team ervoor zorgen dat deze resources
beschikbaar zijn en goed geconfigureerd voordat de suite uitgerold kan worden.
Bij de suite wordt er vanuit gegaan dat alle externe services goed
geconfigureerd zijn.

## Security

Een groot deel van MijnBureau bestaat uit infra code en het uitrollen van
containers. Hieronder zijn een aantal zaken waar rekening mee gehouden moet
worden voor security.

- Tijdens het plannen moet een Threat Analysis gedaan worden voor ieder gekozen
  component
- Tijdens het ontwikkelen moeten Secure Coding practices gehandhaafd worden
- Static Application Security Testen moet gedaan worden op de gekozen
  componenten bij iedere nieuwe versie
- Dynamic Application Security Testing moet gedaan worden op de gekozen
  componenten bij iedere nieuwe versie
- Artefacten moeten gesigned worden door een vertrouwd systeem
- container security scans moeten uitgevoerd worden en CVE's moeten worden
  vastgelegd op 1 centrale plek.
- infra code wordt gescand op kwetsbaarheden

Door alle infra code en artefacten te signen en te controleren zorgen we ervoor
dat geen ongeaccepteerde code in het systeem komt. Je houdt natuurlijk nog wel
de afhankelijkheid van de Supply chain van de componenten. Zolang deze
componenten ook gescand worden kan het risico gemanaged worden.

Verder maken we gebruik van gespreide beschermingsmaatregelen die het risico op
security incidenten verminderd. Als men bijvoorbeeld een ongewenste library in
de code heeft gebruikt, zorgt de virtualisatie en netwerklaag laag van
Kubernetes ervoor dat deze er niet zomaar uit kan springen en andere applicaties
beïnvloeden. Het is hiervoor wel belangrijk om een veilig Kubernetes cluster in
te richten, er zijn binnen Kubernetes vele mogelijkheden om applicaties veiliger
te draaien, denk hierbij aan AppArmor, runtimeclasses, podsecuritystandard en
netwerk policies.

Het Concept van gespreide bescherming zit in alle aspecten van MijnBureau. Een
kwetsbaarheid in een aspect moet gestopt worden door een ander aspect.

Voor het bijhouden van geheimen zoals database wachtwoorden wordt geadviseerd om
een secret manager te gebruiken zodat de geheimen ook makkelijk geroteerd kunnen
worden. Er kan ook gekozen worden voor de Kubernetes secrets, maar dit heeft
niet de voorkeur.

Als MijnBureau geïnstalleerd wordt door een service provider is het belangrijk
om een aantal zaken goed te controleren. de verantwoordelijkheid ligt hiervoor
bij de Service Provider.

Wij raden de volgende maatregelen aan:

1. Een penetration test moet gedaan worden na de installatie
2. Git Signatures worden gecontroleerd bij de rollout
3. Configuratie wordt vastgelegd in een auditable git systeem
4. Infra code wordt gescand op kwetsbaarheden
5. Patches worden snel uitgevoerd zonder service interrupties
6. Het cluster is geaudit volgens standaarden
7. Audit logs worden buiten het cluster opgeslagen
8. Tijdens het draaien van de applicatie worden de configuratie en applicaties
   gescand. Het resultaat wordt gelogd en waar nodig alerts gegenereerd.
9. De logging informatie van de applicaties wordt naar een SIEM gestuurd voor
   analyze.
10. Web Application Filters moeten toegepast worden op alle access points van
    MijnBureau
11. BackUp en Restore systeem moet opgezet worden, inclusief disaster recovery
    plan
12. Rate Limiting

## Lees verder

- [Business architectuur](business-architectuur.md)
- [Informatiearchitectuur](informatie-architectuur.md)

Of keer terug naar de [hoofdpagina](index.md)
