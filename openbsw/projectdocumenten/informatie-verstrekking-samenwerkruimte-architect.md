### Applicatiedienst Samenwerkruimte

Een van de kernonderdelen van de Digitale Werkomgeving is de
applicatiedienst Samenwerkruimte. De Samenwerkruimte is voornamelijk
bedoeld om gezamenlijk informatieobjecten te bewerken (meestal in een
documentvorm, zoals een tekstbestand, presentatie of spreadsheet).

Naast de mogelijkheden om gezamenlijk aan informatieobjecten te werken,
biedt de Samenwerkruimte tal van voorzieningen om online te vergaderen
en interactief te communiceren (zowel via videobellen als chat). Deze
voorzieningen kunnen ter ondersteuning van het samenwerken of op
zichzelf staand worden toegepast.

## Cloud Soevereine oplossingen 

Voor een cloud-soevereine oplossing is het essentieel dat organisaties
volledige controle hebben over waar hun producten worden gehost en waar
hun data wordt opgeslagen. Dit garandeert dat externe partijen geen
toegang hebben zonder expliciete toestemming als er voor gekozen word om
op eigen data centers te hosten. Een dergelijke aanpak voorkomt ook dat
de data onderhevig is aan juridische regelingen van buitenlandse
overheden, die documenten of informatie mogelijk kunnen doorsturen en
analyseren via inlichtingendiensten

Om dit te realiseren, kan men kiezen voor open-sourceoplossingen,
waarmee volledige controle wordt behouden over waar de applicaties
draaien en hoe data wordt opgeslagen. Alternatief kan men gebruikmaken
van diensten van bedrijven die opereren binnen lokale juridische kaders
en de vereiste functionaliteiten bieden.

### Invulling van samenwerkruimte architectuur

In onderstaande tabel zijn de functies toegelicht zoals gedefinieerd in
de BSW architectuur voor applicatiedienst Samenwerkruimte.

  ------------------------------------------------------------------------------------------------------
  Functie                                        Omschrijving
  ---------------------------------------------- -------------------------------------------------------

  channel.virtual.collaboration                  Kanaal voor het groeperen van activiteiten, documenten,
                                                 chatsessies, taken en andere hulpmiddelen voor het
                                                 samenwerken binnen teams.

  task handling.collaboration                    Digitaal planbord voor het registreren, documenteren,
                                                 aanwijzen en opvolgen van taken.

  meeting room.virtual.collaboration             Digitale omgeving voor het houden van online
                                                 vergaderingen.

  chat.meeting room.collaboration                Uitwisseling van (persistente) korte (tekst)berichten
                                                 tussen deelnemers van een vergadering.

  library.shared content.collaboration           Bibliotheek voor het onderbrengen van (links naar)
                                                 gedeelde informatie/informatieobjecten voor generieke
                                                 ondersteuning van werkprocessen.

  streaming.video.collaboration                  Registratie en distributie van videobeelden van
                                                 deelnemers aan een online vergadering.

  streaming.audio.collaboration                  Registratie en distributie van geluid van deelnemers
                                                 aan een online vergadering.

  recording.video&audio.collaboration            Vastleggen van beeld en geluid van een online
                                                 vergadering.

  chat.worker.collaboration                      Uitwisseling van rechtstreekse (persistente) korte
                                                 (tekst)berichten tussen deelnemers in de
                                                 samenwerkruimte.

  file engine.collaboration                      Opslag van bestanden in de samenwerkruimte.

  version handling.collaboration                 Bijhouden van versies om gebruikerswijzigingen te
                                                 traceren, verschillen te tonen en indien gewenst terug
                                                 te draaien.

  representation creation.data object            Duplicatie van een bestand richting een formele dienst
                                                 voor Informatieobjectbeheer, zodat het volledig onder
                                                 het regime van deze dienst

  administration.channel.virtual.collaboration   Beheer van virtuele samenwerkkanalen.

  ------------------------------------------------------------------------------------------------------

Voor invulling van de functionele architectuur requirements zijn
meerdere (open source) oplossingen beschikbaar voor samenwerk. Er zijn
producten die een totaaloplossing bieden, en er zijn producten die delen
van de requirements kunnen invullen en zelf samengevoegd kunnen worden
tot een totaalpakket.

Het gebruik van een totaaloplossing of het samenstellen van een eigen
oplossing heeft beide zijn voor- en nadelen, afhankelijk van de
behoeften en de gewenste mate van controle en flexibiliteit. Een
totaaloplossing biedt een geïntegreerde set van tools die naadloos met
elkaar samenwerken. Dit maakt implementatie en beheer eenvoudiger, maar
kan tegelijkertijd beperkingen opleveren als het gaat om maatwerk of het
vervangen van individuele componenten.

Een voorbeeld van een totaaloplossing is **Nextcloud**, een platform dat
functies biedt voor bestandsbeheer, samenwerking, agenda\'s en
videoconferenties in één pakket. Het voordeel van zo'n oplossing is dat
alles binnen hetzelfde ecosysteem draait, waardoor configuratie en
onderhoud relatief eenvoudig blijven. Echter, deze aanpak kan minder
flexibel zijn als specifieke componenten niet volledig voldoen aan de
eisen van een organisatie.

Aan de andere kant kan men ervoor kiezen om meerdere gespecialiseerde
componenten samen te voegen tot een eigen oplossing. Zo kan bijvoorbeeld
**LibreOffice** worden ingezet voor documentbewerking, **Open-Xchange**
voor e-mail en groupware, en **Jitsi** voor veilige videoconferenties.
Deze aanpak biedt meer controle en flexibiliteit, omdat je alleen de
tools kiest die perfect aansluiten bij jouw behoeften. Het nadeel
hiervan is dat de integratie en het onderhoud van verschillende systemen
complexer kunnen zijn en meer technische kennis vereisen.

Bij de keuze tussen een totaaloplossing en een zelf samengestelde
oplossing is het belangrijk om factoren zoals schaalbaarheid, kosten,
onderhoud, beveiliging en juridische eisen mee te nemen in de afweging.
Organisaties die waarde hechten aan eenvoud en een kant-en-klare
oplossing, zullen vaak kiezen voor een totaaloplossing. Daarentegen zijn
organisaties met specifieke eisen of een sterke focus op maatwerk eerder
geneigd om losse componenten samen te voegen tot een gepersonaliseerd
ecosysteem.

Hieronder staat een tabel met een aantal componenten die kunnen worden
gebruikt om te voldoen aan de functies van een samenwerkingsruimte en
tegelijkertijd een cloud-soevereine oplossing te bieden. Deze lijst is
niet uitputtend, maar geeft een indicatie van de mogelijkheden voor
cloud-soevereine oplossingen.

  ---------------------------------------------------------------------------------------------------------------

  Product        Files   Audio         Video         Chat   Kalender   Contacten   Mail   Office          Taken
                         conferentie   Conferentie                                        (spreadsheat,   
                                                                                          presentaties en 
                                                                                          text            
                                                                                          documenten)     
  -------------- ------- ------------- ------------- ------ ---------- ----------- ------ --------------- -------

  NextCloud      X       X             X             X      X          X           X      X               X

  Libreoffice                                                                             X               

  Open-Xchange                                              x          x           x                      X

  Jitsi meet             x             x                                                                  

  Matrix                 X             X             X                                                    

  OpenDesk       X                     X             X      X          X           X      X               x

  LaSuite        x       x             x             X                                    x               

  Mattermost                                         X                                                    

  OpenOffice                                                                              X               
  
  ---------------------------------------------------------------------------------------------------------------

## Samenwerkruimte Oplossing bij Duitse en Franse overheid

De Duitse en Franse overheid zijn bezig met soevereine samenwerkruimtes
waarbij ze beide een eigen strategie volgen.

De Duitse overheid maakt een totaalpakket genaamd OpenDesk. Opendesk kan
per organisatie geïnstalleerd worden. Opendesk bestaat uit meerdere
opensource componenten. De duitse overheid maken gebruik van contractors
en open source contributors om de opensource componenten aan te passen
zodat deze geschikt is voor de duitse overheid en zetten Europese
aanbestedingen uit om deze software te hosten voor organisaties.

De Franse overheid maak een systeem genaamd LaSuite. LaSuite wordt
aangeboden aan alle overheden als SaaS oplossing. Het enige wat de
overheidsorganisaties moeten doen is hun identity provider koppelen aan
de overkoepelende identity provider. In LaSuite zitten een aantal open
en closed source producten. De franse hebben zelf een team van engineers
die de software aanpast en uitrolt en monitored. Momenteel maken ze ook
zelf componenten omdat ze een betere ervaring wilde leveren dan wat
office 365 levert.
