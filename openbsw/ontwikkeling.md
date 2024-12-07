# Ontwikkeling

Tijdens het ontwikkelen houden we een aantal standaarden aan zodat we zorgen voor een open en transparantie en traceerbaar systeem.

## Commit messages

In softwareontwikkeling is het handhaven van duidelijke en consistente commitberichtconventies cruciaal voor effectieve samenwerking, codebeoordeling en projectbeheer. Commit berichten dienen als een vorm van documentatie, die ontwikkelaars helpt de wijzigingen die door elke commit worden geïntroduceerd te begrijpen zonder de code diff uitgebreid te hoeven analyseren.

Voor projecten die wij beheren moet een commit-bericht aan de volgende regels voldoen:

- De onderwerpregel (eerste regel) MAG niet langer zijn dan 50 tekens
- De onderwerpregel MOET in de gebiedende wijs staan (imperative mood)
- Een zin MOET een hoofdletter als eerste woord hebben
- De onderwerpregel MAG niet eindigen met een leesteken
- De lengte van de hoofdregel MOET beperkt zijn tot 72 tekens
- De hoofdtekst MOET door een lege regel gescheiden worden van de onderwerpregel als deze wordt gebruikt
- De hoofdtekst MOET worden gebruikt om uit te leggen wat en waarom, niet hoe.
- De hoofdtekst KAN eindigen met een ticketnummer
- De onderwerpregel KAN een ticketnummer bevatten in de volgende indeling

\<ref\>-\<ticketnumber\>: onderwerpregel

## Pull Requests

we maken altijd een pull request om wijzigingen in een repository voor te stellen en hieraan samen te werken. Deze wijzigingen worden voorgesteld in een branch, wat ervoor zorgt dat de standaardbranch alleen voltooid en goedgekeurd werk bevat.

Voor projecten die wij beheren moet een pull request aan de volgende regels voldoen:

- Zorg dat de title in een paar woorden duidelijk beschijft wat de PR bereikt
- Gebruik een actiegerichte stijl in je PR
- Referentie gerelateerde problemen of taken met een #\<nummer>
- Vermijd redundantie

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
