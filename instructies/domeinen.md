# Domeinen: lat, vaktaal en AI-verdeling (versie 1.1)

Waar: `~/.claude/systeemprompt/domeinen.md`. Niet geïmporteerd: Claude leest het in Code bij een leerblok of op
verzoek (regel in `~/.claude/CLAUDE.md`).
Versie 1.1, 2026-11-11: kop over het model herschreven, regel voor een domein dat ontbreekt, en twee
correcties (BCG als bron van de 19 procentpunt; transcriptie bij Kennismanagement van U naar T).
Lengte: 32.739 tekens, 433 regels. Geen limiet: het bestand laadt niet standaard.

---
# Domeinen: lat, vaktaal en AI-verdeling

Versie 1.1, 2026-11-11. Opgesteld met Claude Opus 5.5; het bewijs gaat over modellen tot medio 2026. In
gebruik met Claude Opus 5.5 en Claude Fable 5.2; voor geen van beide is de verdeling apart gemeten. Volgende
herziening: 2027-05-09, of eerder als Claude op een model draait dat deze kop niet noemt. Herzien met de herzieningsprompt (`herzieningsprompt.md`).

Bron: fase 3 van het project claude-preferences (fasebestanden met alle bronnen en bronnotities; niet in deze repo). Veel claims zijn daar als "niet nagelezen" gemarkeerd: de onderzoekers zagen alleen een
samenvatting. Wetgeving is grotendeels niet in de wettekst gelezen; dit is geen juridisch advies.

Legenda AI-verdeling: **U** voert uit (aantoonbaar zelf, met gemeten kwaliteit), **T** ondersteunt onder
toezicht (een persoon stuurt, controleert en is verantwoordelijk), **N** (nog) niet. Bewijs: **M** meting,
**MV** meting door een vendor, **S** gepubliceerde standaard, **P** praktijkverslag, **O** mening,
**A** afwezigheid van bewijs. Een claim van een leverancier over zijn eigen product is O, tenzij er een
meting onder ligt.

Gebruik in een leerblok: lees alleen deze kop en de sectie van het domein. "Wat AI hier kan" komt uit de
AI-verdeling, "wat ik zelf moet beheersen" uit de laatste lijst per domein. Kies het domein dat het best past; noem het als het onderwerp tussen twee domeinen valt. Past geen domein, zeg dat en geef de verdeling als eigen inschatting, zonder cijfers uit een ander domein.

Over alle domeinen heen: AI voert uit waar een test, schema of vaste definitie het antwoord objectief
bevestigt, en ondersteunt onder toezicht waar dat criterium ontbreekt. Gesprekken, besluiten, vertrouwen en
wettelijke verantwoordelijkheid blijven bij de mens. Het sterkste bewijs is vaak oud (GPT-4, 2023 tot 2025)
en komt uit andere contexten.

## Strategie en analyse

**Lat.**
- Benoemt beslissing, beslisser, succescriterium en scope vóór de analyse.
- Antwoord in de eerste een of twee zinnen; daarna de onderbouwing (Pyramid Principle).
- Een toetsbare hypothese met wat haar weerlegt; laat haar vallen als de feiten tegenspreken.
- Bij een aanbeveling: wat waar moet zijn, en de minst zekere voorwaarde eerst toetsen.
- MECE ontleden; zeggen welke takken niet worden uitgewerkt.
- Strategie begint bij de diagnose van de kernuitdaging; zegt wat niet gebeurt; noemt bij elk voordeel waarom concurrenten het niet kunnen kopiëren.
- Schattingen vanuit een referentieklasse, opgeknipt in schatbare factoren, met kansen of bandbreedtes.
- Sterkste tegenargument en premortem bij grote besluiten; elke sectie eindigt met een so what.

**Vaktaal.** Governing thought: de ene kernboodschap. SCQA: situatie, complicatie, vraag, antwoord.
MECE: geen overlap, geen gaten. Issue tree: vraag ontleed tot toetsbare deelvragen. Day One Hypothesis:
beste voorlopige antwoord, om te verwerpen. Action title: titel die een conclusie is. So what: implicatie
voor de beslissing. Where to play / how to win: de twee kernkeuzes. Trade-off: bewust iets niet doen.
Base rate / outside view: hoe vaak dit in vergelijkbare gevallen gebeurt. Pre-mortem: stel dat het mislukt
is, waarom? Jagged frontier: grillige grens tussen taken waar AI helpt en waar het schaadt.

**Schijnkwaliteit.** Een doel ("marktleider worden") als strategie. Vijf tot tien strategische pijlers
zonder keuze. Best practices als voordeel. Een ingevulde SWOT of 2x2 zonder conclusie. Een lijst met het
label MECE die overlapt. Kopjes als "Marktanalyse". "Kan" en "mogelijk" zonder kans. Schatting alleen op het
eigen plan. Gepolijst rapport met verzonnen bronnen (Deloitte Australië 2025).

**AI-verdeling.**

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Probleemdefinitie met de klant | N; voorbereiding T | GDPval sluit interpersoonlijke taken uit (M, A, 2025-10) |
| Hypothesen en ideeën | T | P&G, 776 professionals: individu met AI evenaart team zonder (M, 2025-04) |
| Desk research | T | Verzonnen bronnen bij Deloitte (P, 2025-10) |
| Kwantitatieve analyse | T | GDPval: modellen verzinnen soms data of rekenen fout (M, 2025-10). BCG: buiten de frontier 19 procentpunt minder correct (M, 2023-09, GPT-4) |
| Synthese en storyline | T, eerste versie bijna U | BCG, 758 consultants: binnen de frontier circa 40% betere kwaliteit (M, 2023-09) |
| Slides en documenten | U voor drafts; T voor de klantversie | GDPval: beste model 47,6% gelijk of beter dan experts (M, 2025-10) |
| Prognose kort en data-rijk | T, bijna U | ForecastBench: systemen gelijk aan superforecasters (M, 2026-07) |
| Prognose lang en oordeelzwaar | N | A |
| Aanbeveling, besluit, stakeholders, implementatie | N | A |

**Zelf beheersen.** Het probleem met de klant scherp krijgen en context leveren (prestatie daalt met minder
context). Per taak inschatten of die binnen de frontier ligt. Elke bron en elk getal voor de klant narekenen
(verantwoordelijkheid). Review inplannen: met review slinkt de tijdwinst tot 1,1 tot 1,4x (GDPval).
Tegenspraak organiseren, want assistenten buigen naar je mening. Eigen inschatting van AI-winst meten,
niet voelen (METR 2025: 20% sneller gevoeld, 19% trager gemeten, tools van begin 2025). AI-geletterdheid
(AI Act art. 4).

## Ondernemerschap: positionering, propositie, prijs

**Lat.**
- Eerst het alternatief zoals de klant het ziet (niets doen, Excel, een interne medewerker), dan het onderscheid.
- Elke waardeclaim met een bewijsvorm; best-fit klanten met waarneembare kenmerken (sector, omvang, aanleiding).
- Eén smal beachhead-segment; past de tekst ook op de concurrent, dan is het geen positionering.
- Aannames als falsifieerbare hypothesen met een vooraf vastgesteld stopcriterium; weinig, gefundeerde pivots.
- Valideren met gedrag en commitment (geld, tijd, reputatie), niet met meningen; opgegeven betalingsbereidheid ligt gemiddeld 21% te hoog.
- Prijs vanaf economische waarde voor de klant, met de economic buyer gekwantificeerd vóór de offerte; drie opties die verschillen in werkvorm, niet in uren.

**Vaktaal.** Competitive alternative: wat de klant zonder jou zou doen. ICP: kenmerken van klanten die de
waarde het sterkst ervaren. Beachhead: eerste smalle segment. Positioning statement: "For ... who ...,
unlike ...". Commitment / advancement: de klant geeft iets op en zet een stap. Value-based pricing: prijs
vanaf klantwaarde; cost-plus is het tegendeel. WTP: betalingsbereidheid. Hypothetical bias: opgegeven WTP
te hoog. Anchoring: de eerste prijs kleurt de rest. Productized service: vaste scope, proces en prijs.
Retainer, fixed fee, outcome-based fee.

**Schijnkwaliteit.** "Betrouwbare partner", "maatwerk", "ontzorgen". Een featurelijst als
waardepropositie. "Gevalideerd" na enthousiaste gesprekken. Lean-taal zonder hypothese of stopcriterium.
"Wat zou u betalen?" als prijsbewijs. Synthetische respondenten als WTP-bewijs. Een "waardegebaseerd"
voorstel met urenspecificatie. Positioneringstekst die volledig door AI is geschreven (gelijkvormiger).

**AI-verdeling.** Geen meting in B2B-dienstverlening; alles overgedragen uit andere contexten.

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Markt- en concurrentieonderzoek | T | Losse AI-oordelen inconsistent (M, 2025) |
| Segment- en ICP-keuze | T | Geaggregeerde AI-oordelen benaderen experts, losse niet (M, 2025) |
| Discovery-gesprekken | N; voorbereiding T | Synthetische respondenten: WTP vaak onjuist (M, 2026-04) |
| Interviews coderen | T | Kappa 0,84 maar minder diepgang; verwart hypothetisch met ervaren (M, 2025-2026, medisch) |
| Positionerings- en messagingdrafts | U voor drafts; T voor de keuze | Hogere koopintentie, maar homogenisering (M, 2023-2024) |
| Prijs vaststellen en onderhandelen | T; onderhandelen N | AI-agents sluiten toegeeflijke deals (M, 2025-09) |
| Go/no-go | N; input T | 640 Keniaanse ondernemers: geen gemiddeld effect, sterken beter, zwakken slechter (M, RCT, 2023) |

**Zelf beheersen.** Kiezen welk AI-advies past (zonder domeinkennis schaadt AI-advies). Meerdere oordelen
aggregeren in plaats van één AI-oordeel volgen. De zoekrichting sturen tegen gelijkvormigheid. Echte kopers
spreken; betalingsbereidheid uit offertes en pilots. Prijs, onderhandeling en go/no-go dragen. AVG bij
opgenomen interviews; geen gedeelde prijsalgoritmen met concurrenten.

## Sales, dienstverlening en RevOps

**Lat.**
- Kwalificeert op pijn in geld, tijd of risico en spreekt de economic buyer vóór het voorstel.
- Implicatievragen (wat kost dit, wie merkt het, wat als niets verandert) vóór de oplossing.
- Elk gesprek legt een advance vast: een concrete, gedateerde stap van de koper.
- "Why change" vóór "why us"; "no decision" als grootste risico; een twijfelende koper minder opties.
- Een voorstel bevat geen nieuwe informatie; geen gratis ontwerpwerk, wel een betaalde diagnose.
- Outreach met een controleerbare aanleiding en hypothese, via een kanaal dat mag (art. 11.7 Telecommunicatiewet).
- Pipelinestadia met exit criteria op koperacties; delivery gemeten op afgesproken uitkomsten.

**Vaktaal.** Discovery: situatie, probleem, impact en beslisproces vóór een oplossing. Economic buyer:
wie het geld vrijmaakt. Champion: interne ambassadeur. Buying group / DMU. Paper process: inkoop, juridisch,
verwerkersovereenkomst. Implication en need-payoff question. Advance vs continuation. Up-front contract:
vooraf doel, tijd, uitkomsten inclusief "nee". Mutual action plan. No decision. Trigger event. Exit criteria.
Win rate. Pipeline coverage (de vuistregel 3x is mening). NRR / GRR: omzetbehoud. Soft opt-in.
SPF / DKIM / DMARC: e-mailauthenticatie.

**Schijnkwaliteit.** Outreach met alleen naam en bedrijf ingevuld. Koude bulkmail aan benoemde Nederlandse
contactpersonen "omdat het B2B is". Een uitgewerkt voorstel na het eerste gesprek. Een volle pipeline zonder
economic buyer of klantstap. Closing-technieken en korting als sluitmiddel. Dashboards met opens en MQL's.
Een volledig ingevuld CRM vol aannames. AI SDR-claims over geboekte meetings.

**AI-verdeling.**

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| ICP, prospectonderzoek, triggers | T | Alleen vendorclaims (O, A) |
| Outbound copy | T | 100.000 koude mails: AI 4,1% reply tegen mens 5,2%, meer spamflags (P, 2026-04) |
| Discovery-gesprek zelf | N; voorbereiding en notulen T | 69% van B2B-kopers toetst AI-inzichten bij een verkoper (M, Gartner 2026-05) |
| Voorstel en scoping | T | GDPval: losse deliverables 47,6% gelijk of beter (M, 2025-10) |
| Prijs, onderhandeling, closing | N | A |
| Transcriptie en CRM-logging | U; interpretatie T | A (algemene kennis van spraakherkenning) |
| Klantenservice bestaande klanten | T | 5.172 agents: +15% opgelost per uur, vooral nieuwkomers (M, 2025-02) |

**Zelf beheersen.** Discovery, onderhandeling, closing en accountrelatie zelf voeren: kopers toetsen bij een
mens, en onthulde AI verlaagt vertrouwen. Kwalificatie, scope, prijs en forecast per deal. Outbound zelf
redigeren. Weten wie gemaild of gebeld mag worden (art. 11.7 Tw: e-mail alleen met toestemming, bestaande
klant of daarvoor gepubliceerd adres). SPF, DKIM en DMARC op het eigen domein. AVG bij prospectlijsten en
opgenomen gesprekken. Een AI-chatbot die met prospects praat als AI laten melden (AI Act art. 50).

## Software (Python, SQL, Git)

**Lat.**
- Kleine, enkelvoudige changes (circa 100 regels redelijk); refactoring en gedragswijziging apart.
- Tests in dezelfde change, in CI; een bug eerst reproduceren met een falende test; `git bisect` om de oorzaak te vinden.
- Tests beoordeeld op asserties en mutation testing; coverage alleen als zoeklamp.
- Een change goedkeuren zodra die de code health verbetert; feit gescheiden van voorkeur ("Nit:").
- Leesbaar boven slim; type hints op publieke grenzen; domeinlogica als pure functies, I/O aan de randen.
- Dependencies vast in een lockfile met hashes (`pylock.toml`, PEP 751), in een virtual environment.
- SQL vanuit het query plan (`EXPLAIN ANALYZE`) en de index; alleen nodige kolommen; keyset pagination; constraints voor integriteit; geparametriseerde queries.
- Atomic commits met het waarom; lokale historie mag je herschrijven, gedeelde nooit; trunk-based met kortlevende branches.

**Vaktaal.** Code health. CL / PR. Nit: niet-blokkerend reviewpunt. Hyrum's Law: elk waarneembaar gedrag
wordt een afhankelijkheid. Mutation testing. Flaky test. Idempotent. Pure function. Technical debt. Lockfile.
Query plan. Sargable: predicate dat een index kan gebruiken. Keyset pagination. Transaction isolation / ACID.
N+1 query. Parameterized query. Golden rule of rebasing. Atomic commit. Conventional Commits / SemVer.
Trunk-based development, feature flag, CI.

**Schijnkwaliteit.** 100% coverage zonder zinvolle asserties. Een grote change met "fix stuff". Slimme code.
Smaakdiscussies in review. Tests die alleen lokaal draaien. `requirements.txt` zonder pins als
"reproduceerbaar". Interfaces en factories voor één implementatie. Type hints met `Any` overal. Opgeschoonde
historie door gedeelde branches te force-pushen.

**AI-verdeling.**

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Requirements met stakeholders | N; uitschrijven T | Geen benchmark meet dit (A) |
| Architectuur en ontwerp | T; zelfstandig N | Minder refactoring, meer duplicatie sinds AI (MV, GitClear 2020-2024) |
| Nieuwe code, afgebakende taak met tests | U | METR: 50%-horizon circa 12 tot 16 uur, 80%-horizon circa 1 tot 3 uur (M, 2026) |
| Naar productie zonder review | T | AI-PR's 1,7x zoveel bevindingen (MV, 2025-12); 0 van 15 test-geslaagde PR's direct mergebaar (M, 2025-08) |
| Schema-ontwerp, tests schrijven | T; schema zelfstandig N | A |
| Debugging, reproduceerbare bug | U | SWE-bench Pro onafhankelijk circa 55 tot 62% (M, 2026) |
| Debugging, productiebug zonder reproductie | T | A |
| Refactoring en migraties | T | Google: circa 80% van migratiewijzigingen door AI, met review (MV, 2025-01) |
| Security review | N | Veracode: securityfout in 45% van de taken (MV, 2025-07); verzonnen packages 5 tot 20% |
| Git-routine | T | A |
| Conflicten, history rewrite, force push | N | Onomkeerbaar (A, P) |
| CI/CD en deployment | T | DORA: meer AI hangt samen met meer instabiliteit (M, survey, 2025) |

**Zelf beheersen.** Scope en acceptatiecriteria vaststellen. Tests en verwachte resultaten formuleren of
controleren: automatisch geslaagd is niet mergebaar. Datamodel en architectuur kiezen. Elke AI-change
reviewen, klein houden. Security: injectie, XSS, secrets, bestaat het package echt. Zelf code lezen en
debuggen; leren met uitleg, niet met volledige delegatie (RCT: 17 procentpunt minder begrip, vooral bij
debugging; Anthropic 2026-01). Destructieve acties goedkeuren. Eigen productiviteit meten. AVG, licenties en
bij een installeerbaar product de meldplicht uit de Cyber Resilience Act.

## Data-analyse

**Lat.**
- Het besluit en de actie per uitkomst vóór de eerste query.
- Metricdefinitie uitgeschreven (teller, noemer, venster, filters, eenheid) en de estimand: welk effect, voor wie, ten opzichte van wat.
- Confirmatoire analyse vooraf vastgelegd (hypothese, primaire metric, steekproef, stopregel); verkennend werk als verkennend gelabeld; power en MDE vooraf.
- De grain van elke tabel benoemd; na elke join rijtelling en uniciteit gecontroleerd en als test vastgelegd.
- Verdeling bekijken vóór samenvatten; een verrassend resultaat eerst als fout behandelen (Twyman's law); SRM checken.
- Causale vraag: DAG, confounders, identificatieargument.
- Een tweede redelijke specificatie draaien; effect met interval in de eenheid van het besluit; melden hoeveel analyses je bekeek.
- Reproduceerbaar: code in versiebeheer, vaste afhankelijkheden, geen handwerk in een spreadsheet.

**Vaktaal.** Grain: wat één rij voorstelt. Fact en dimension table, star schema. Fan-out: rijvermenigvuldiging
door een join. Staging / intermediate / marts. Semantic layer: centrale metricdefinities. Tidy data. Cohort.
Guardrail metric. Power / MDE. Confidence interval. p-waarde: onverenigbaarheid met een model, niet de kans
dat de hypothese klopt. SRM. Peeking / sequential testing. Garden of forking paths. Confounder. Simpson's
paradox. Regression to the mean. DAG / estimand. Goodhart's law.

**Schijnkwaliteit.** "Statistisch significant" als conclusie, of "niet significant, dus geen effect".
Segmenten kiezen tot iets significant is. Eén analyse als "de" uitkomst. Een A/B-test stoppen zodra hij
significant is. "Gebruikers van X blijven langer, dus X werkt". "Conversie steeg 12,347%" op 80 gebruikers.
Gemiddelden over scheve verdelingen. Vanity metrics. Een dashboard zonder eigenaar of drempel. Een
spreadsheet als pipeline. "Actieve klant" in drie varianten.

**AI-verdeling.**

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Vraag en besluit framen met stakeholders | N | Ambigue vragen: 8,67 tot 17% opgelost (M, BIRD-Interact 2025-10) |
| Metricdefinitie | T: AI stelt voor, mens legt vast | Semantic model tilt hetzelfde LLM van 57 naar 78% (MV, 2025) |
| Data cleaning en preparatie | T | Beste LLM 30,5% (M, 2024) |
| SQL op eenduidige vraag en gecureerd schema | U | Spider 2.0-Snow top 96,7 (M, leaderboard, 2026-11; veel labels fout) |
| SQL op rauw schema of ambigue vraag | T | Stil verkeerde resultaten, zoals nul rijen door een verkeerde enum-waarde (P) |
| Verkennende analyse | T | DABstep hard: 14 tot 37% (M, 2025-2026) |
| Toetskeuze, standaardscenario | U | Zes LLM's kozen in 20 scenario's de juiste toets (M, klein, 2025-10) |
| Modelleren en analysekeuzes | T | Grote spreiding tussen AI-analisten, stuurbaar via prompt (M, 2026-02) |
| Experimentontwerp | N | A |
| Interpretatie en causale claims | N | Ongegronde causale conclusies (M, 2025) |
| Communiceren, rapportages | T | Zelfde prompt, andere analyse (M, 2026) |

**Zelf beheersen.** Het besluit achter de vraag vaststellen met de opdrachtgever. Metricdefinities,
join-regels en enum-waarden vastleggen als contextbestand. Bepalen welke data in welk AI-systeem mag
(AVG: doelbinding, minimalisatie, verwerkersovereenkomst; persoonsgegevens in een chatbot kan een datalek
zijn). SQL en code controleren: rijtellingen, totalen tegen bekende cijfers, duplicatie. Een eigen kleine
evaluatieset met geverifieerde antwoorden. Analyseplan vóór AI draait. Statistische en causale geletterdheid.
De aanbeveling met onzekerheid verdedigen.

## AI-engineering (RAG en automatisering)

**Lat.**
- Error analysis op echte traces vóór metrics: circa 100 traces lezen, faalwijzen benoemen en tellen.
- Eén domeinexpert beslist over kwaliteit; binaire oordelen; rubric pas na het lezen van data.
- Een LLM-judge gevalideerd tegen menselijke labels (TPR, TNR), opnieuw na elke modelwissel.
- Begin met 20 tot 50 taken uit echte fouten; capability en regression evals apart; consistentie meten met pass^k.
- Retrieval apart meten (Recall@k, MRR) en eerst debuggen; BM25 als baseline, dan embeddings en reranker als meting dat rechtvaardigt; chunking is een hyperparameter.
- Onder circa 200.000 tokens: eerst alles in de prompt met caching (vendormening, meet het zelf).
- De eenvoudigste architectuur: workflow vóór agent, de API vóór een framework, multi-agent alleen voor parallel werk.
- Geen agent die privédata, onbetrouwbare input en een extern kanaal combineert; minimale rechten; output valideren.

**Vaktaal.** Chunking. Embedding / dense retrieval. BM25. Hybrid search. Reranker. Contextual Retrieval.
Recall@k / Precision@k. Metadata filtering. Prompt caching. Context engineering. Context rot / lost in the
middle. Eval set / golden set. Trace. Error analysis / failure taxonomy. LLM-as-judge. Criteria drift:
criteria veranderen door het beoordelen. Groundedness / faithfulness. pass@k / pass^k. Workflow vs agent.
MCP. Human-in-the-loop. Idempotency. Guardrail vs evaluator. Prompt injection / lethal trifecta. Excessive
agency.

**Schijnkwaliteit.** Generieke scores (ROUGE, helpfulness) op een dashboard in plaats van traces lezen.
Judge-score zonder kalibratie. Likert-schaal 1 tot 5. Rubric vooraf zonder data. Demo op zelf gekozen vragen.
Een agent voor een lineaire taak. Een framework als vakmanschap. Een vector database als vanzelfsprekend.
"95% detectie" als beveiliging. RAGAS-scores als eindoordeel.

**AI-verdeling.** Bij geen onderdeel is aangetoond dat AI het zelfstandig goed doet in een echte klantomgeving.

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Use case en eisen met de klant | N | A |
| Inventaris van bronnen en rechten | T | Wie wat mag zien is een besluit (S, OWASP) |
| Parsing en ingestie | T; bijna U voor nette pdf's | OmniDocBench-scores deels zelf gerapporteerd (M, MV, 2026) |
| Chunking, indexering, retrieval-tuning | T | Automatische tuning werkt op publieke sets (M, 2025-2026) |
| Code, prompts en pipelines | T | 80%-horizon veel korter dan 50%; 0 van 15 PR's mergebaar (M) |
| Eval set bouwen | T | Criteria drift (M, 2024) |
| LLM-as-judge draaien | T | Ruwe overeenstemming overschat judges 33 tot 41 punten (M, preprints 2025-2026) |
| Bronvast samenvatten | T, bijna U | Hallucinatie 1,8% tot meer dan 10% (MV, Vectara 2026) |
| Vragen beantwoorden in een rommelig domein | T | Juridische RAG-tools hallucineerden in meer dan 17% (M, 2025) |
| Agents onbewaakt | N | pass^8 onder 25% in retail (M, 2024-modellen) |
| Security | N | Geen model robuust tegen prompt injection (M, 272.000 aanvallen, 2026-03) |
| Governance, adoptie | N | A |

**Zelf beheersen.** Use case afbakenen, inclusief waar AI niet beslist. Rechtenmodel per document in de
retrieval. Tacit kennis van de klant-expert boven tafel krijgen en met die expert de eval set opstellen.
De judge kalibreren tegen menselijke labels. AI-code reviewen in stukken van ongeveer een uur mensenwerk.
Menselijke bevestiging vóór onomkeerbare of externe acties. Antwoorden in productie steekproefsgewijs
controleren: de organisatie staat in voor haar chatbot (Moffatt v. Air Canada). Per klant de AI Act-rol
(provider of deployer) en art. 50 (melden dat het AI is); DPIA, verwerkersovereenkomsten, inzage en wissing
per document. Gebruikers begeleiden.

## Kennismanagement (kennisborging bij vertrek en pensioen)

**Lat.**
- Begint bij een bedrijfsprobleem en een risicoscore: vertrekmoment maal vervangbaarheid (elk 1 tot 5); 20 tot 25 is direct actie.
- Per kennisdomein: expliciet, impliciet of tacit, en daarbij documenteren, interviewen of begeleid oefenen.
- Ook relatiekennis: wie kent wie, wie weet wat.
- Eén dominante strategie: codification of personalization.
- Elicitatie via concrete, recente incidenten en beslismomenten (cues, opties, wat een beginner mist), in meerdere korte sessies, met validatie door de expert. Experts laten in vrije uitleg circa 70% van hun beslissingen weg.
- Maanden tot jaren vóór vertrek beginnen, met een opvolger, een leerplan en guided experience.
- Per artikel eigenaar (rol), status, reviewdatum; kennis ontstaat en wordt bijgewerkt in het werk zelf.
- Meten op gebruik en uitkomst (hergebruik, time to proficiency, minder vragen aan de expert); geen quota; baten in vensters van 3 tot 36 maanden.

**Vaktaal.** Explicit / implicit / tacit knowledge. SECI. Deep smarts: ervaringsexpertise met oordeel.
K = I x EVA (Weggeman). Critical knowledge. Knowledge loss risk assessment. Single point of failure.
Kennisborging (knowledge retention). Knowledge audit / map. Knowledge elicitation. Cognitive task analysis
(CTA). Critical Decision Method (CDM): interview over één reëel incident in meerdere doorgangen. Knowledge
capture interview. Guided experience. After Action Review. Lessons identified vs learned. Time to
proficiency. Codification vs personalization. Community of practice. SME / knowledge owner. Content
lifecycle. Taxonomy / ontology. KCS. ISO 30401.

**Schijnkwaliteit.** Een lessons-learned-database met veel lessen die niemand raadpleegt (NASA). Artikelen
tellen of quota. Het exit interview als kennisoverdracht. De expert alles laten opschrijven. Een wiki vol
documenten zonder eigenaar of reviewdatum. Eerst het platform kiezen. Alles even grondig vastleggen. Een
kennisbank als opvolger. Een Teams-kanaal als community. Een ISO-certificaat als doel.

**AI-verdeling.**

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Kritieke kennis met vertrekrisico bepalen | N | A; 92% van organisaties legt het niet consequent vast (MV, APQC 2025) |
| Experts selecteren, vertrouwen opbouwen | N | AI-dreiging hangt samen met kennis verbergen (M, 2025) |
| Breed bevragen (wie weet wat) | T | 1.250 AI-interviews, alleen tevredenheid gemeten (MV, 2025-12) |
| Diepte-elicitatie van één specialist | T bij voorbereiding; zelfstandig N | AI vraagt slechter door; AI-ontologie miste veel kennis (M, klein, 2025-2026) |
| Transcriptie | T, met steekproef | Circa 11% fouten bij realtime transcriptie (M, niet nagelezen, 2025); Nederlands met jargon niet onderzocht |
| Interviews omzetten in artikelen en regels | T | Hallucinatie bij samenvatten 1,8 tot 24,2% (MV, 2026-05) |
| Taxonomie | T | Andere structuur per run (M, klein, 2025) |
| Validatie, onderhoud, kennishiaten, uitkomsten meten | N | A |
| Vragen beantwoorden uit de kennisbank | T | Helpt vooral nieuwkomers, nauwelijks ervaren krachten (M, 2025-02) |
| Communities en mentoring | N | Posts op Stack Overflow daalden 16 tot 25% na ChatGPT (M, 2024) |

**Zelf beheersen.** Bepalen welke kennis kritiek is. De specialist benaderen, vertrouwen opbouwen, angst
voor vervanging bespreken; de specialist profiteert zelf weinig van de assistent. Het diepte-interview zelf
voeren of de AI-interviewer bewaken en zelf doorvragen. Elicitatietechnieken (CDM, think-aloud, observatie).
Elke AI-uitwerking door de specialist laten valideren, met wie, wanneer en welke versie. Eigenaarschap en
vervaldatum beleggen. De opvolger begeleiden. Communities naast de assistent in stand houden.
AVG en DPIA bij interviewopnames; OR-instemming (WOR art. 27 lid 1 onder k en l); doelbinding, zodat
interviews niet voor beoordeling worden gebruikt (anders AI Act Bijlage III).

## Verandermanagement (adoptie van een tool of werkwijze)

Het effectbewijs voor veranderinterventies is dun: 3% van 563 studies gebruikte een cohortdesign.

**Lat.**
- Het probleem met feiten uit meerdere bronnen en per stakeholdergroep, vóór de oplossing.
- Readiness per team vóór de uitrol (werkdruk, concurrerende initiatieven, verandergeschiedenis), met een expliciet go/no-go.
- Impactanalyse per rol: wie wint, wie verliest, en hoe het verlies vooraf wordt gecompenseerd.
- Per doelgedrag Capability, Opportunity en Motivation (COM-B); een bundel interventies, compleet overgenomen.
- Eerst bright spots zoeken; ontwerpen met mensen van de werkvloer.
- Learning goals en performance goals; adoptie als waargenomen gedrag (hoeveel mensen, welke activiteiten, hoe vaak).
- Pilots tonen nut in het eigen werk; ervaren nut voorspelt gebruik het best.
- Resistance als informatie, inclusief de eigen bijdrage; uitleggen waarom het nu anders loopt dan de vorige keer.

**Vaktaal.** Change readiness. Readiness-overtuigingen: discrepancy, appropriateness, efficacy, principal
support, valence. Change fatigue. Sponsor. Change agent / recipient. Impact analysis. Resistance.
Sensemaking. Psychological safety. Distributive / procedural fairness. Episodic vs continuous change.
Kleurendenken (De Caluwé en Vermaak). COM-B / intervention functions. ADKAR. Adoption / usage / proficiency.
Perceived usefulness / ease of use (TAM, UTAUT). Behavioral intention: voornemen, geen gebruik. Bright spots /
small wins.

**Schijnkwaliteit.** "70% van de veranderingen faalt" (geen deugdelijke bron). Lewins drie stappen als
fundament. Kotter of ADKAR als bewezen recept. Prosci's "7x meer kans" (zelfrapportage van de verkoper).
Training gevolgd als adoptie. Een communicatieplan als change management. "80% wil de tool gebruiken" als
adoptie. Logins of geüploade documenten als adoptiemaat. "95% van de GenAI-projecten faalt".

**AI-verdeling.** Geen onderdeel haalt U binnen een echt veranderprogramma.

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Diagnose en readiness | T voor enquête en codering; oordeel N | Thema's uit open antwoorden 93,9% tegen 94,7% voor mensen (M, 2024) |
| Stakeholder- en impactanalyse | T | A |
| Sponsorcoalitie bouwen | N | A |
| Aanpak en interventies ontwerpen | T | O (vendorclaims) |
| Communicatieteksten | T | Bij veel AI-inbreng vond 40 tot 52% berichten van leidinggevenden oprecht, tegen 83% (M, 2025) |
| Sentiment uit open tekst | T, duidelijk zwakker | Kappa 0,49 tot 0,70 tegen 0,95 tussen mensen (M, 2025-2026); emotieherkenning op het werk verboden (S, AI Act art. 5) |
| Weerstandsgesprek zelf | N | Vermoeden van AI-hulp verlaagt waargenomen empathie (M, 2025) |
| Adoptie meten | T voor classificeren; verankeren N | Monitoring per werknemer valt onder WOR art. 27 (S) |
| OR-consultatie | N; adviesaanvraag voorbereiden T | Taak van de ondernemer (S, WOR art. 25 en 27) |

**Zelf beheersen.** Diagnose, readiness-oordeel en interventiekeuze. Sponsor zijn en change agents trainen.
Afzender zijn van belangrijke en relationele boodschappen. Weerstandsgesprekken voeren. Verlies vooraf
regelen. AI-output op feiten, toon en sentiment controleren. Beslissen wanneer AI-gebruik openbaar wordt.
De OR om advies en instemming laten vragen. Geen emotieherkenning; luisterinstrumenten AVG-proof.

## Loopbaan- en sollicitatiemateriaal

**Lat.**
- Elke cv-regel: resultaat, maatstaf met vergelijkingsbasis, eigen aanpak, beginnend met een actief werkwoord.
- Het bovenste derde adresseert de twee of drie zwaarste vacature-eisen in de termen van de vacature.
- Eén kolom, scanbaar; een tweede pagina is geen bezwaar.
- Ondernemersperiode als eigen rol met titel, scope en resultaat; de combinatie met een eigen bedrijf open benoemen (uren, beschikbaarheid, geen belangenconflict).
- Brief van hooguit één A4, met per eis een concreet bewijs en iets wat alleen over deze organisatie waar is.
- Per vacature-eis twee of drie STAR-voorbeelden in de ik-vorm, getoetst aan vervolgvragen.
- Alleen vaardigheden claimen die in een proefopdracht of vakvraag te demonstreren zijn.
- Geen salarishistorie noemen; onderhandelen vanuit benchmark en total compensation.
- Investeren in matig zwakke banden in de doelsector; een richting testen met kleine experimenten.

**Vaktaal.** ATS: database die filtert op criteria die mensen instellen. Parsing. Boolean search. Knockout
question. Recruiter screen. Hiring manager. Referral. Weak ties. Structured, behavioural, situational
interview. STAR(R). Probing. Impression management. Work sample / case interview. Achievement statement /
X-Y-Z-formule. Transferable skills. Elevator pitch. Portfolio. Salary benchmark / total compensation.
Nevenwerkzaamhedenbeding (art. 7:653a BW). NVP Sollicitatiecode.

**Schijnkwaliteit.** "75% van de cv's wordt door het ATS afgewezen" (salespitch, geen studie). "Recruiters
kijken 6 seconden" als beslistijd. Een hoge ATS-score uit een cv-checker. "Communicatief, analytisch,
resultaatgericht". "Verantwoordelijk voor ...". Design-cv met kolommen en skill-balkjes. Keyword stuffing.
Een generieke, ook AI-geschreven, brief. Een hiaat verbergen. Voorbereiding op "klik". STAR over "wij".
"CEO" van een eenmanszaak zonder omvang.

**AI-verdeling.** Het gestructureerde interview voorspelt werkprestatie het best (0,42; jaren ervaring circa
0,07).

| Onderdeel | Oordeel | Bewijs |
|---|---|---|
| Loopbaanrichting en positionering | N | A |
| Vacatures vinden en matchen | T | Geen meting aan kandidaatzijde (A) |
| Cv: taal, leesbaarheid, fouten | U | Schrijfhulp gaf 8% meer aannames (M, pre-LLM, 2025) |
| Cv afstemmen op de vacature | T | LLM-screeners verkiezen LLM-cv's (M, lab, 2025) |
| Motivatiebrief | T | Op maat gemaakte brieven verloren na LLM's hun signaalwaarde (M, 2025-11) |
| LinkedIn, outreach | T | Afgeleid (A) |
| Netwerken, referrals, referenties | N | A |
| Assessments en het gesprek zelf | N; oefenen T | AI-hulp tijdens het gesprek is fraude; werkgevers toetsen weer fysiek (P, 2025) |
| Salarisonderhandeling | T | LLM's adviseerden vrouwen een lager streefsalaris (M, lab, 2025-07) |

**Zelf beheersen.** Elke feitelijke bewering controleren, ook als AI schreef (misleiding kan ontslag op
staande voet rechtvaardigen; een vals diploma is valsheid in geschrifte). Richting en positionering kiezen.
Persoonlijk en verifieerbaar schrijven. Eigen bewijs van werk tonen (portfolio, cases, resultaten van het
bedrijf). Gesprek en assessments zelf voeren. Netwerk en referenties onderhouden. Salarisdoel onderbouwen met
cao of onafhankelijke data. Het nevenwerkzaamhedenbeding toetsen. Rechten tegenover werkgevers-AI
(AVG art. 15 en 22).
