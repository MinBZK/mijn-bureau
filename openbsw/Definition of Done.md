# Definition of Done:

1. Code Kwaliteit

- Code is gereviewd en goedgekeurd door minimaal 1 repository member
- Code voldoet aan de [google style guidelines](https://google.github.io/styleguide/)
- Unittests zijn geschreven voor alle nieuwe of aangepaste code, met een dekking van ten minste 80%
- Code wordt door sonarcloud geanalyseerd op problemen
- Alle code review comments zijn beantwoord of gesloten
- Code wordt door een linter, formatter en typechecker gehaald, de specifieke tools kunnen per repo gekozen worden

2. Documentatie

- Bevindingen van PoC word gedocumenteerd op de [evaluatie pagina](openbsw/evaluatie.md)
- Eigen gemaakte Functionaliteiten zijn gedocumenteerd in de github repository, bij voorkeur in een markdown file.
- Documentatie wordt door een formatter gehaald, de specifieke tool kan per repo gekozen worden

3. Testen

- Testen draaien in de Continuous Integration github action
- Alle unit-tests, integratietests en end-to-end-tests slagen
- Er wordt voldaan aan de acceptatiecriteria die in de taak zijn gedefinieerd en deze zijn getest.

4. Compliance

- Er zijn geen gevonden CVSS v4.0 >= 9.0 security issues onopgelost gebleven.
- Er is een automatische licentie check gedaan op de gebuikte software componenten
- Er is een Software Bill of Materials gemaakt voor iedere release
- Er wordt een automatische accessibility check gedaan
