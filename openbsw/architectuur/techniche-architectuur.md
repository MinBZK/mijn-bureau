# Technology architectuur (TODO, nog niet af)

Deze suite, MijnBureau, is opgebouwd uit dezelfde componenten als LaSuite en
OpenDesk op een fit-for-purpose manier met als doel om de beste samenwerksuite
voor ambtenaren en medewerkers te bieden. De suite is ingericht om te werken met
de bestaande login systemen van de organisatie of systeem binnen MijnBureau.

Het platform zal open-source componenten samenbrengen tot één systeem, met als
groot verschil dat we meer flexibiliteit willen bieden aan organisaties om
componenten te verwisselen en te integreren met hun bestaande systemen, waar dit
realistisch is.

## Selectie en rechtvaardiging

### Componenten

Tijdens de Proof of concept zijn veel componenten van onze partners beproeft. De
volgende mogelijke component zijn hieruit gekomen

| Function            | Functional Component |
| ------------------- | -------------------- |
| Chat                | Element Synapse      |
| Notes               | Docs                 |
| Portal              | Bureaublad           |
| Identity management | Keycloak             |

We follow an agile procedure so not all features are added yet. The following
features are envisioned to be added

| Function                                     | Functional Component                                                  | Component Version | Upstream Documentation |
| -------------------------------------------- | --------------------------------------------------------------------- | ----------------- | ---------------------- |
| File management                              | [Nextcloud Files](https://nextcloud.com/files/)                       |                   |                        |
| Spreadsheet, presentation & document editing | [Collabora Online](https://www.collaboraonline.com/collabora-online/) |                   |                        |
| Email, Agenda & Tasks                        | [OX App Suite](https://www.open-xchange.com/products/ox-app-suite)    |                   |                        |
| Cases                                        | [OpenZaak](https://github.com/open-zaak/open-zaak)                    |                   |                        |
| Spreadsheet & More                           | Grist                                                                 |                   |                        |
| Video calling                                | Meet/Jitsi                                                            |                   |                        |
| AI Assistant                                 | OpenWebUI                                                             |                   |                        |

### Scalability and Performance

Functionele geschiktheid • 90% van vereiste functies verwacht door gebruikers
beschikbaar Performance efficiëntie • responstijd van gemiddelde 300ms (p95) •
Kan 1000 verzoeken per seconden aan (+-750 Gebruikers) Compatibiliteit •
Ondersteund laatste versie van 3 browsers (Firefox, edge & chrome)
Gebruiksvriendelijkheid • SUS-score minimaal 75 uit gebruikers onderzoek
Operationeel • Minder dan 5% fouten bij kritieke taken • Maximaal 30% langer dan
benchmark • Minimaal wettelijke WCAG-score • Betrouwbaarheid (9 tot 5, exclusief
weekend) • MTBF minimaal 1 week • MTTR minder dan 8 uur • Beschikbaarheid 98% •
RPO

- RTO • Gebruik CI/CD-pipeline voor geautomatiseerde en reproduceerbare releases
  Beveiliging • Maximaal 2 kritieke kwetsbaarheden per release, opgelost binnen
  72 uur. • Alle containers moeten gescande worden op kwetsbaarheden

Onderhoudbaarheid • Heeft mogelijkheid tot gebruikt van open metrics, Logs en
traces • Deployments moeten worden beheerd via declaratieve configuratie •
Minimaal 80% testdekking • Heeft declaratieve monitoring en alerting

## Lees verder
- [Business architectuur](business-architectuur.md)
- [Informatiearchitectuur](informatie-architectuur.md)

Of keer terug naar de [hoofdpagina](index.md)
