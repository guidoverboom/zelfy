# AI Agent Instructies

**Lees dit document altijd als eerste voordat je een taak uitvoert.**

**1. Project Scope & Fase**
1a. Dit document houdt de ontwikkelingsfase van het project bij. Huidige status: **[Exploratiefase]**. De agent monitort actief op indicatoren (zoals vastgestelde tech-stacks, de start van productie-ontwikkeling, geformuleerde stabiele project-scope) die erop wijzen dat we de exploratiefase voorbij zijn, en kaart dit aan de gebruiker aan om vervolgens dit document en de instructies te updaten.
1b. In deze opstartfase verwachten we een proactieve, iteratieve houding. Proefcode of experimentele componenten worden bij voorkeur in afzonderlijke submappen geïsoleerd (bijv. `concepten/` of `prototypes/`).
1c. Documenteer gemaakte technologische of architecturale ontwerpkeuzes logisch en direct in `docs/action_log.md` (of apart in `docs/architecture_decisions.md`) naarmate we knopen doorhakken.
1d. Blijf strikt binnen de aangewezen projectmap en pas niets daarbuiten aan zonder instemming.

**2. Documentatie, Logs & Archivering**
2a. Er is een helder onderscheid tussen de documentatie in de map `docs/`, zorg dat deze áltijd proactief netjes afgestemd en up-to-date gehouden wordt:
    - **`changelog.md`**: Uitsluitend logboek van wijzigingen in de code/applicatiestructuur.
    - **`action_log.md`**: Chronologisch overzicht van alle breed ondernomen activiteiten (overleggen, planvorming, code-aanpassing). *Elk item dat in de changelog wordt gezet, komt zodoende ook áltijd in andere bewoording terug in deze action log.*
    - **`bestandenbeheer.md`**: Leg expliciet uit waartoe mappen en bestanden dienen en houd de genoteerde structuur hierin accuraat.
    - **`description.md`**: De meest actuele projectbeschrijving/visie.
2b. Indien een `implementation_plan.md` of `walkthrough.md` klaar, behandeld of niet meer actief is, moet deze altijd als procedure worden opgeslagen in de map `archief/` met het voorvoegsel `[yymmdd]-` (bijv. `260418-implementation_plan.md`).

**3. Workflow & Communicatie**
3a. **Timestamps:** Elk antwoord dat je geeft aan de gebruiker is een belangrijk oriëntatiepunt en *moet* te allen tijde eindigen met een timestamp (de actuele verwerkingstijd).
3b. Voer de "afronden" actie en genereer een Workflowy-overzicht UITSLUITEND uit wanneer de gebruiker hier expliciet om vraagt (bijv. middels de trigger "afronden").
    - Verwijs in het opgestelde overzicht naar momenten en verwerkingen middels de timestamps uit de eerdere antwoorden (regel 3a).
    - Geef in het overzicht een gedetailleerde samenvatting van acties sinds de vorige afronding.
    - Plaats dit lijstje ALTIJD in een raw tekst codeblok (`text`) waarbij je geneste bullets inspringt met een tab (`\t`) of dubbele spaties, ten behoeve van foutloze 1-klik Workflowy kopiëring.
    - Geef het de titel ("Sessie focus: [titel]"), noem welke AI en/of tool je bent, en voeg de URL/gespreks-id toe.
    - **Let op:** Synchroniseren/pushen naar GitHub als onderdeel van de afronding mag alléén worden gedaan/voorgesteld indien je hebt vastgesteld dat er in deze projectmap inmiddels daadwerkelijk een gekoppelde GitHub omgeving of repository bestaat.
3c. Controleer je output en documentatie altijd proactief op onbedoelde taal-glitches en overbodige herhalingen (zoals problemen met Engelse stopwoorden in de zinsbouw, bijv. "the the the"). Zorg voor foutloos, professioneel en vloeiend Nederlands in alle interactie.
3d. **Gespreksinitiatie:** Controleer bij de allereerste interactie in een nieuwe sessie of gesprek altijd proactief het bestand `docs/actielijst.md` en geef de gebruiker een korte reminder van de daarop geopende items en (indien van toepassing) een GitHub configuratie-status.

**4. Veiligheid & Databeheer**
4a. Bij acties die bulkdata migreren of data-opschoning vereisen (zoals API-acties of het overschrijven van JSON structuur), zul je de gebruiker in je pre-implementatie áltijd eerst een plan of instructie voorleggen om veilig lokaal een back-up of dump van deze brondata te maken, alvorens agressieve calls of filesaves écht plaatsvinden.
