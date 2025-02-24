# Pilot Voorstel OpenBSW
De laatste 2 maanden hebben we een Proof of Concept (PoC) gedaan. Deze PoC had een exploratief karakter, hierdoor neemt de PoC nog een aantal aspecten niet mee die wel belangrijk zijn voor het aanbieden van samenwerk diensten. Voorbeelden hiervan zijn toegankelijkheid normen, security & privacy normen, gebruikers input en transparantie richtlijnen. Ook heeft de PoC nog geen uitwerking om te voldoen aan de architectuur van BSW. In de pilot willen we deze aspecten wel meenemen. 

# Voorstel
Het voorstel is om extra budget beschikbaar te stellen voor pilots onder OpenBSW waarbij we geselecteerde producten uittesten met gebruikersgroepen. Het resultaat aan het einde van de pilot is het volgende
* Een adviesrapport van het product voor gebruik in Nederlandse samenwerk software suite
* Een rapport aan welke wet- en regelgeving het product voldoet en welke stappen genomen moeten worden als hij nog niet voldoet.
* Een samenvattingsrapport die de ervaringen van gebruikers beschrijft
* Een rapport die de uitwerking beschrijft naar het voldoen aan architectuur van BSW
* Een rapport die de WCAG oplevert

In de pilot willen we gebruikers toegang gaan geven tot geselecteerde producten uit de Proof of Concept. Hierbij is het belangrijk dat de producten neergezet wordt zodat ze aan de wet- en regelgeving die van toepassing is voldoen. Verder willen we kijken of het product binnen de BSW architectuur past en welke stappen nodig zijn als deze nog niet past.

Met het extra budget creëren we een pilot team. Ook gebruiken we het budget voor het afnemen van computers bij overheidsdatacenters en kunnen we Enterprise licenties (van open source producten) inkopen waar dit nodig is om de doelen van de pilot te behalen.

Ons voorstel voor het pilotproject is om de tijd en middelen vast te zetten, terwijl we de scope flexibel houden. De producten die geprioriteerd worden, kunnen we per product via een nota afstemmen met de stuurgroep, zodat we de nodige flexibiliteit behouden. In deze nota beschrijven we bevindingen van de PoC en beschrijven we ontwikkel, UX-onderzoek, security en operations werkzaamheden.  Zowel het team als de stuurgroep kunnen voorstellen doen voor pilot producten.

Voorbeelden van producten kunnen zijn:
* Chat (Element synapse)
* Office (Collabora + NextCloud)
* Video Bellen (Jitsi/Meet)
* Notities (Docs)
* Mail (OpenXChange)
* AI Interface (OpenWebUI)
* Projectmanagement (OpenProject)
* Kennismanagement (XWIki)

# Kaders
Om het onderzoek waardevol te houden moeten voor alle pilot producten kaders aangehouden worden waarbij Open Strategische Autonomie (OSA) erg belangrijk is voor OpenBSW. Voor de producten gaan we uit van volledige autonomie en volledig open. Hierbij houden we de volgende kaders aan

* Product draait op Rijksdatacenter
* Containerisatie boven Virtualisatie
* Opensource tenzij methodiek
* Product installatie & Beheer wordt declaratief opgezet 
* Product installatie & Beheer wordt opensource ontwikkeld 
* Informatie-uitwisseling gebeurt met open standaarden
* Product is integreerbaar met OpenID Connect voor gebruiker authenticatie
* Zero trust functionaliteit

# Wet en regelgeving
Voor producten die onder beter samenwerken vallen zijn een aantal belangrijke wet en regelgeving waarmee rekening gehouden moet worden. Bij de pilot projecten houden we deze wet en regelgeving aan.

* AVG (GDPR): Privacywetgeving die de verwerking van persoonsgegevens reguleert
* Wet Digitale Overheid: Regels voor identificatie en gegevensuitwisseling
* BIO2: Informatie & cyber beveiliging regelgeving
* AI-Act: AI-systemen wetgeving
* Forum Standaardisatie: Standaarden vastgelegd
* Archiefwet: Levenscyclus van overheidsinformatie
* Wet Open Overheid: Transparantie wetgeving
* Wet Digitale Overheid: Veilige, toegankelijke en betrouwbare digitale communicatie
* NIS2: Cyber beveiliging
* NSCS: basis richtlijnen cyber security

# Kwaliteitsnormen
Om waarde te leveren aan gebruikers moeten de producten aan de kwaliteit eisen voldoen die vergelijkbaar zijn aan concurrerende systemen. Dit betekent dat het product gebruiksvriendelijk, onderhoudbaar, veilig en functioneel geschikt moet zijn.

Dit betekent dat we minimaal deze eisen neerleggen voor de producten die we pilotten

* Functionele geschiktheid
  * 90% van vereiste functies verwacht door gebruikers beschikbaar
* Performance efficiëntie
  * Responsetijd van gemiddelde 300ms (p95)
  * Kan 1000 verzoeken per seconden aan (+-750 Gebruikers)
* Compatibiliteit
  * Ondersteund laatste versie van 3 browsers (firefox, edge & chrome)
* Gebruiksvriendelijkheid
  * SUS-score minimaal 75 uit gebruikers onderzoek
  * Minder dan 5% fouten bij kritieke taken
  * Maximaal 30% langer dan benchmark
  * Minimaal wettelijke WCAG score
* Betrouwbaarheid (9 tot 5, exclusief weekend)
  * MTBF minimaal 1 week
  * MTTR minder dan 8 uur
  * Beschikbaarheid 98%
  * Gebruik CI/CD pipeline voor geautomatiseerde en reproduceerbare releases
* Beveiliging
  * Maximaal 2 kritieke kwetsbaarheden per release, opgelost binnen 72 uur.
  * Alle containers moeten gescanned worden op kwetsbaarheden 
* Onderhoudbaarheid
  * Heeft mogelijkheid tot gebruikt van open metrics, Logs en traces
  * Deployments moeten worden beheerd via declaratieve configuratie
  * Minimaal 80% testdekking
  * Heeft declaratieve monitoring en alerting 
* Overdraagbaarheid
  * Applicaties moeten eenvoudig te deployen zijn op meerdere Kubernetes systemen
  * Product wisselt informatie uit via open standaarden zodat we `best of breed` kunnen handhaven
  * Software kan deployen op on-prem kubernetes en bij cloud providers
