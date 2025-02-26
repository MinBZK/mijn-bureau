# Werkafspraken

## Bijeenkomsten en rituelen

Het OpenBSW team heeft een op Kanban geinspireerde werkwijze met de volgende rituelen:

* Dagelijkse meeting
* Wekelijkse demo waarna we de prioriteiten doorspreken

Wat we hebben beproeft en wat we hebben geleerd schrijven we op in [de evaluatie](evaluatie.md).

### Agenda voor dailies en vrijdag sync:

1. Standup
2. Nieuwe oplossingen
3. Prioriteren backlog
4. Wat is er nog meer? Demo's, onderwerpen uit de stand-up, etc.

Bij dailies is de tijd beperkt. De tijd die rest na afloop van de standup (timebox: 15 min) kan dan aan andere punten worden besteed. Op vrijdag volgen we alle onderdelen van de agenda.

# Kwaliteitsafspraken

Tijdens het ontwikkelen houden we een aantal standaarden aan zodat we zorgen voor een open en transparantie en traceerbaar systeem.

## Definition of Ready:

1. Beschrijving
   * De taak heeft een beschrijving van het probleem of de gewenste functionaliteit in een `Intro` kop.
2. Acceptatie criteria
   * Duidelijke en meetbare acceptatie criteria zijn opgesteld en gedocumenteerd in `Acceptatie Criteria` kop.
3. Schatting
   * De taak heeft een schatting in de vorm van punten gekregen.
4. Prioriteit
   * De prioriteit en eventuele afhankelijkheden met andere taken zijn aangegeven. 
   * De prioriteit wordt bepaald door de locatie in de backlog. Bovenaan is hoge prioriteit, onderaan is lage prioriteit.
5. Techniek
   * Complexe onderdelen zijn geanalyseerd via een refinement en beschreven onder `Implementation Details`.

## Definition of Done:

1. Code Kwaliteit
   * Code is gereviewd en goedgekeurd door minimaal 1 repository member
   * Code voldoet aan de [google style guidelines](https://google.github.io/styleguide/)
   * Unittests zijn geschreven voor alle nieuwe of aangepaste code, met een dekking van ten minste 80%
   * Code wordt door sonarcloud geanalyseerd op problemen
   * Alle code review comments zijn beantwoord of gesloten
   * Code wordt door een linter, formatter en typechecker gehaald, de specifieke tools kunnen per repo gekozen worden
2. Documentatie
   * Bevindingen van PoC word gedocumenteerd op de [evaluatie pagina](openbsw/evaluatie.md)
   * Eigen gemaakte Functionaliteiten zijn gedocumenteerd in de github repository, bij voorkeur in een markdown file.
   * Documentatie wordt door een formatter gehaald, de specifieke tool kan per repo gekozen worden
3. Testen
   * Testen draaien in de Continuous Integration github action
   * Alle unit-tests, integratietests en end-to-end-tests slagen
   * Er wordt voldaan aan de acceptatiecriteria die in de taak zijn gedefinieerd en deze zijn getest.
4. Compliance
   * Er zijn geen gevonden CVSS v4.0 >= 9.0 security issues onopgelost gebleven.
   * Er is een automatische licentie check gedaan op de gebuikte software componenten
   * Er is een Software Bill of Materials gemaakt voor iedere release
   * Er wordt een automatische accessibility check gedaan

## Commit messages

In softwareontwikkeling is het handhaven van duidelijke en consistente commitberichtconventies cruciaal voor effectieve samenwerking, codebeoordeling en projectbeheer. Commit berichten dienen als een vorm van documentatie, die ontwikkelaars helpt de wijzigingen die door elke commit worden geïntroduceerd te begrijpen zonder de code diff uitgebreid te hoeven analyseren.

Voor projecten die wij beheren moet een commit-bericht aan de volgende regels voldoen:

* De onderwerpregel (eerste regel) MAG niet langer zijn dan 50 tekens
* De onderwerpregel MOET in de gebiedende wijs staan (imperative mood)
* Een zin MOET een hoofdletter als eerste woord hebben
* De onderwerpregel MAG niet eindigen met een leesteken
* De lengte van de hoofdregel MOET beperkt zijn tot 72 tekens
* De hoofdtekst MOET door een lege regel gescheiden worden van de onderwerpregel als deze wordt gebruikt
* De hoofdtekst MOET worden gebruikt om uit te leggen wat en waarom, niet hoe.
* De hoofdtekst KAN eindigen met een ticketnummer
* De onderwerpregel KAN een ticketnummer bevatten in de volgende indeling

\<ref\>-\<ticketnumber\>: onderwerpregel

## Pull Requests

we maken altijd een pull request om wijzigingen in een repository voor te stellen en hieraan samen te werken. Deze wijzigingen worden voorgesteld in een branch, wat ervoor zorgt dat de standaardbranch alleen voltooid en goedgekeurd werk bevat.

Voor projecten die wij beheren moet een pull request aan de volgende regels voldoen:

* Zorg dat de title in een paar woorden duidelijk beschijft wat de PR bereikt
* Gebruik een actiegerichte stijl in je PR
* Referentie gerelateerde problemen of taken met een #\<nummer>
* Vermijd redundantie

## Code Reviews

Code reviews zijn een belangrijk kwaliteits aspect van ontwikkelen. Al het werk wat we opleveren moet gereviewd worden door iemand binnen of buiten het team.

Als een auteur een Pull Request heeft klaarstaan mag deze reviewed worden. Als de auteur dit niet wilt zal hij de `Draft` pull request gebruiken in github.

Voor iedere Pull Request moet de auteur een duidelijke beschrijving toevoegen en een gerelateerde issue toevoegen als die bestaat.

De Auteur labeled de Pull Request correct.

Standaard word het mijn-bureau team toegekend als reviewer. Als een auteur een specifieke reviewer wilt voegt hij deze zelf toe. Deze person moet dan reviewen voordat de Pull Request gemerged mag worden.

Als een reviewer commentaar heeft geplaatst op een pull request antwoord de auteur hier altijd op, waarbij hij het gesprek kan sluiten als hij het commentaar accepteert met een bericht 'geaccepteerd'. Hetzelfde kan gebeuren door de reviewer, als hij het antwoord van de auteur voldoende vindt.

zodra de reviewer alles goed vindt kan hij de pull request approven. Het is aan de auteur om de pull request te mergen.

## Repositories

Op iedere repository volgen we trunk-based git branch strategie.

Op iedere repository gebruiken we sonarcloud voor kwaliteit en security checks.

In iedere repository zetten we formatting tools op zodat code conventies gehonoreerd worden.

## Deployment

Als we tools deployen gebruiken we bij voorkeur de Kubernetes van digilab.

Deze Kubernetes gebruikt flux voor deployment en sops for security encryption. Wij zullen ons aanpassen aan deze tools. Ook zorgen we ervoor dat geen secrets gecommit worden naar een repository tenzij dit encrypt is.

# Communicatie

We gebruiken een aantal tools om met elkaar en de omgeving te communiceren. Iedere tool heeft zijn eigen doel.

Voor asynchrone communicatie gebruiken we [mattermost](https://digilab.overheid.nl/chat). Groeps chats moeten voor iedereen beschikbaar zijn tenzij er zwaarwegende redenen zijn. In Mattermost is een team genaamd mijn-bureau waar meerdere kanalen beschikbaar zijn voor discussies. Als we onze eigen tooling hebben die betrouwbaar genoeg is stappen we over op die tool. 

Voor project management gebruiken we [github projects](https://github.com/orgs/MinBZK/projects/22). Dit project moet publiekelijk beschikbaar zijn. Als we onze eigen tooling hebben die betrouwbaar genoeg is stappen we over op die tool

Voor vastlegging gebruiken we Github Repositories onder de organisatie [MinBZK](https://github.com/orgs/MinBZK/repositories). Alle repositories die in beheer zijn van [mijn-bureau](https://github.com/orgs/MinBZK/teams/mijn-bureau/repositories) moeten publieklijk beschikbaar zijn. De repositories zijn:

* [github mijn-bureau](https://github.com/MinBZK/mijn-bureau) voor documentatie.
* [github lasuite basis](https://github.com/MinBZK/LaSuiteBasis) voor infra van basis componentent La Suite
* [github opendesk](https://github.com/MinBZK/opendesk) voor infra opzet van oplossing OpenDesk
* [github leos](https://github.com/MinBZK/leos) voor bouwen en infra van Legislation Editing Open Software (LEOS)
* [github grist](https://github.com/MinBZK/grist) voor infra opzet van oplossing Grist (onderdeel van LaSuite)
* [github docs](https://github.com/MinBZK/docs) voor infra opzet van oplossing Docs (onderdeel van LaSuite)
* [github meet](https://github.com/MinBZK/meet) voor infra opzet van oplossing Meet (onderdeel van LaSuite)
* [github ai-assistant](https://github.com/MinBZK/ai-assistant) voor infra opzet van oplossing AI assistant (onderdeel van LaSuite)
* [github ai-webservices](https://github.com/MinBZK/ai-webservices) voor infra opzet van oplossing AI webservices (onderdeel van LaSuite)
* [github chat](https://github.com/MinBZK/chat) voor infra opzet van oplossing Chat Meet (onderdeel van LaSuite)
* [github keycloak-theme](https://github.com/MinBZK/keycloak-theme) voor keycloak theme (onderdeel van LaSuite)
* [github la-suite basis](https://github.com/MinBZK/la-suite-basis) voor infra opzet van Identity provider en andere basis compontent (onderdeel van LaSuite)
* [github mijn-bureau portal](https://github.com/MinBZK/mijn-bureau-portal) voor portal software
* [github office](https://github.com/MinBZK/office) voor infra opzet van office (onderdeel van LaSuite)
* [github plausible](https://github.com/MinBZK/plausible) voor infra opzet van portal analytics
* [github vault](https://github.com/MinBZK/vault) voor infra opzet van pasword manager

Voor formele communicatie wordt de Rijksoverheid email gebruikt.

Voor video conferencing wordt de Rijksoverheid versie van Webex gebruikt binnen het team. Meetings buiten het team worden gehouden is de meest handig tool die beschikbaar voor de externe stakeholders. Als we onze eigen tooling hebben die betrouwbaar genoeg is stappen we over op die tool.
 
