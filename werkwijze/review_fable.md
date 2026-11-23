# Eindreview claude-preferences

> Verwijzingen naar `5_data`, `4_logs`, `test_v2.md`, `redteam_fable.md` en andere projectbestanden wijzen naar het
> volledige werkarchief en staan niet in deze repo. Namen van klanten en organisaties zijn weggehaald of vervangen.

Versie 1, 2026-11-10. Model: Claude Fable 5.2 in een Code-sessie in de desktop-app, werkmap deze
projectmap (niet Fable 5.1 in een claude.ai-chat, zoals `2_staat\voortgang.md` noemt). Prompt:
`7_overdracht\prompt_review_fable.md`. In de projectmap is niets gewijzigd, behalve dat dit bestand is
toegevoegd.

Gelezen: `README.md`, `CLAUDE.md`, `1_spec\`, `2_staat\`, `3_besluiten\`, `7_overdracht\` (alle bestanden),
`8_instructies\v1\` en `v2\` (alle bestanden), `5_data\fase1`, `fase2` en `fase4` volledig, `fase3a` tot en
met `fase3c` op samenvatting, kopjes en de rijen van de steekproef, `test_v2.md` en de acht Word-outputs.
Niet gelezen: de bronnotities in `5_data\onderzoek\` en de bundel met bestaand onderzoek.

Buiten de map alleen-lezen gecontroleerd, omdat de sessie op de eigen machine draaide: de vier geplaatste
bestanden en de drie kopieën in een tweede map (sha256), de koppen van die kopieën, en de
transcripten van run 1, 1r, 2 en 7 onder `~/.claude/projects/`.

Nagerekend (sha256, eerste acht tekens, van de tekst onder ---): kern 2.1 `2ba89305` (6.093 tekens,
54 regels), `domeinen.md` `760c878d` (32.387 tekens, 432 regels), `~/.claude/CLAUDE.md` `6849a0d2`
(669 tekens), projectmap-`CLAUDE.md` `27efc49b` (3.663 tekens), herzieningsprompt `6ec1498b`. Geplaatst en
kopie zijn in alle gevallen byte voor byte gelijk aan `8_instructies\v2\`. Kern 2.0, gereconstrueerd door
de zin uit B36 terug te zetten, geeft `f90bc56f`: het verschil tussen 2.0 en 2.1 is exact één zin. De
accountinstructie v1 telt 7.750 tekens en 29 regels.

## 1. Oordeel

Het project heeft gedaan wat het moest doen, met drie gaten. Aangetoond is het volgende:

- De kern laadt in beide omgevingen.
- De vier geplaatste bestanden en de drie kopieën zijn byte voor byte gelijk aan v2 (nagerekend).
- Kern 2.0 en 2.1 verschillen exact één zin.
- Elke regel in `kern.md` en `claude-md.md` is herleidbaar tot een besluit.

Er zijn geen kritieke fouten gevonden. De drie belangrijkste bevindingen:

1. **De test bewijst minder dan B38 zegt.** "Lat hoger, 5 tegen 4" hangt aan één punt van T4, dat binnen
   v2 zelf wisselt en op een niet-geverifieerde wetslezing rust. "Leerinstructie hoger" is per constructie
   waar. Wat standhoudt: v2 is niet slechter dan v1, en T1 is in claude.ai gerepareerd.
2. **Drie kernregels werken anders dan bedoeld.** De afsluitregel houdt in Code geen vragenlijsten tegen
   (2 van 2 runs). "Zwakste claims" is een vast kopje geworden (7 van 10 antwoorden). De memory-regel
   botst met de app en met B33.
3. **Het spoor heeft twee gaten bij live instellingen.** De oude `CLAUDE.md` van de projectmap is
   overschreven zonder kopie, en de opgeschoonde memory is nergens vastgelegd of gecontroleerd.

## 2. Fouten

Ernst: kritiek, groot of klein. Status: geverifieerd in de bestanden, of inferentie.

| # | Ernst | Bestand en plek | Wat er mis is | Bewijs | Status | Voorstel |
|---|---|---|---|---|---|---|
| 1 | Groot | `5_data\test_v2.md`, Samenvatting en Vergelijking; B38 | "Lat hoger" is niet aangetoond. Het ene punt verschil komt alleen uit T4 (run 12: 2, run 18: 1). Run 16, dezelfde kern plus de labelzin, haalt dat punt ook niet en scoort gelijk aan v1. T2 en T3 scoren gelijk. | Run 16: "ik kan de exacte regels [...] niet bevestigen". | Geverifieerd | Oordeel bijstellen naar "niet lager"; T2 en T4 drie keer per variant draaien als "hoger" moet blijven staan. |
| 2 | Groot | `8_instructies\v2\testset.md`, T4, eerste punt onder Goed | Het beslissende criterium rust op een wetslezing die het project niet in de wettekst las. Het beloont een stellige claim (run 12, bron MKB Servicedesk) boven "niet te bevestigen", wat de kern juist vraagt. | `sessieverslag_fase3a.md`: "wettekst, ledennummering en de wijziging per 1 juli 2026 komen uit secundaire bronnen." | Geverifieerd | Art. 11.7 lezen op wetten.overheid.nl en acm.nl, daarna het criterium vastzetten. |
| 3 | Groot | `8_instructies\v2\kern.md`, Afsluiting, eerste regel | "Heeft de omgeving een eigen afsluiting, volg die" werkt niet in Code: beide T2-runs met v2 zetten twee of drie vragen in het bericht. Het is afgerond als "bijvangst", terwijl B26 erop leunt. | Transcript run 2 (sessie be507fd7): het bericht eindigt op "2. Heb je al iemand gesproken die over budget beslist [...]?" | Geverifieerd | Code-regel in `claude-md.md`, zie verbetering 1. |
| 4 | Groot | `kern.md`, Eerlijkheid, laatste regel | De voorwaarde uit v1 is bij het inkorten verdwenen; de zin leest als altijd doen. 7 van de 10 v2-antwoorden op T2 tot en met T8 hebben een eigen kopje "Zwakste claims" (runs 2, 4, 5, 12, 14b, 15, 16). Fase 4 sectie 6 vroeg "in de tekst zelf, geen eigen kopje". | v1: "Zijn die er niet, voeg dan geen kunstmatige twijfel toe." | Geverifieerd | Vervangende zin, zie verbetering 2. |
| 5 | Groot | `kern.md`, laatste regel; B33; `5_data\fase4_analyse_plan.md` sectie 9 | Drie lagen zeggen iets anders over regels in memory. De kern zegt "geen regels". De app vraagt in Code werkafspraken juist op te slaan (soort "feedback"). B33 laat een regel bewust in lokale memory staan. Ook is nergens vastgelegd wat "klantgegevens" zijn. | Fase 4: "de kernregel over memory spreekt ze niet tegen". | Tekst geverifieerd; effect op gedrag is inferentie | Vervangende zin, zie verbetering 3. |
| 6 | Groot | `1_spec\randvoorwaarden.md`, Klaar; `2_staat\voortgang.md` | Het doel "memory bevat alleen wat Claude echt helpt" heeft geen Klaar-criterium en geen bewijs. claude.ai-memory is niet gecontroleerd, lokale memory is uitgesteld. | Voortgang: "eindstand niet door Claude gecontroleerd". | Geverifieerd | Uitvoer van stap 16 of een nieuwe export bewaren in `8_instructies\v2\bron\`; de lokale wijziging als open punt in `verbeterpunten.md`. |
| 7 | Groot | `7_overdracht\sessieverslag_plaatsen.md` | De bestaande `CLAUDE.md` van de projectmap is overschreven zonder kopie. De workflow vroeg eerst te tonen wat er stond. Het verslag zegt dat de oude tekst terug te halen is, maar in de map staan alleen fragmenten. | Zoeken op "verankert" geeft twee citaten, geen volledige tekst. | Geverifieerd | Oude versie uit de back-up van de externe schijf halen en bewaren als `8_instructies\v1\claude-md-projectmap.md`. |
| 8 | Groot | `8_instructies\v2\claude-md-projectmap.md`, Lat voor dit project | Zes van de acht punten overlappen met de domeinregels in de kern, tegen `<lagen>`: "Geen regels die al in de kern staan". Daarnaast staat een bedrijfsbesluit als vaste instructie, afgeleid uit wat het bestand zelf "inferenties" noemt. | Kop van het bestand: "uit fase 3b en 3c [...]; inferenties". | Tekst geverifieerd; dat Claude het besluit niet meer toetst is inferentie | Zie verbetering 7. |
| 9 | Klein | `8_instructies\v2\claude-md.md`, regel 1 | "Deze regels" staat onder de kop "Alleen in Claude Code" en kan alleen op de vier Code-regels slaan; B25 bedoelt ook de kern. De voorrang is niet getest. | `test_v2.md`: "niet uitgevoerd; geen score". | Geverifieerd; het misleesrisico is inferentie | "... de kern of deze regels tegen ..." (+11 tekens) en de controle alsnog draaien. |
| 10 | Klein | `claude-md.md`, regel 3; `8_instructies\v2\domeinen.md`, kop | "Beoordeeld op model: Claude Opus 5.5" suggereert dat de verdeling over Opus 5.5 gaat; het bewijs betreft oudere modellen. "Nieuwer model" is onbepaald voor een model uit een andere lijn, zoals Fable 5.2 in deze review. | Fase 3a, rij Slides: "Claude Opus 4.1 47,6%". | Geverifieerd | Kop: "Opgesteld met Opus 5.5; bewijs over modellen tot medio 2026". Regel: "ander model" (2 tekens korter). |
| 11 | Klein | `claude-md.md`, regel 2 | De regel wordt letterlijk gevolgd bij routine: beide T1-runs in Code met v2 eindigen met een voorbehoud, de run zonder instructie niet. | Run 1r: "Ik heb deze commando's niet op jouw machine uitgevoerd." | Geverifieerd | "Verifieer wat je bouwt of wijzigt met een test of commando ..." (+23 tekens). |
| 12 | Klein | `domeinen.md`, steekproef | Ruim 35 cijfers en oordelen vergeleken met fase 3: twee wijken af. (a) Strategie, Kwantitatieve analyse: "19 procentpunt" staat achter GDPval en hoort bij BCG. (b) Kennismanagement, Transcriptie: bewijs "A", terwijl fase 3c een meting met circa 11% fouten noemt. Al in fase 3 aanwezig: het oordeel U voor transcriptie zonder meting, tegen de eigen legenda, en twee reeksen voor dezelfde Vectara-bron (tot "meer dan 10%" en tot 24,2%). De kop telt 32.337 tekens; geteld 32.387. | Fase 3a regel 135: "BCG: taak buiten de frontier gaf 19 procentpunt minder". | Geverifieerd | Transcriptie nu naar T zetten (de pilot leunt op interviews in Nederlands vakjargon); de rest bij de eerste herziening. |
| 13 | Klein | `test_v2.md`, run 8 | 3 van 7 moet 4 van 7 zijn: punt 7 (geen eigen vragenlijst) is gehaald. Het vergelijkingspunt telt dan 13 punten, niet 12. | Run 8 bevat geen vraag aan de gebruiker. | Geverifieerd | Corrigeren; geen gevolg voor de score. |
| 14 | Klein | `test_v2.md`, Opzet en run 1r | De scoreregel is achteraf gemaakt en niet consequent toegepast: de losse vette regel "Opmerkingen" boven vijf punten telt als lijstinleiding. | `test_v2.md`: "Een losse vette regel boven een blok tekst geldt hier als kopje". | Geverifieerd (transcript 284cd4ee: geen `##`, wel die regel) | Criterium vastleggen als "geen regel die als kop dient, in welke opmaak ook". |
| 15 | Klein | `testset.md`, T7 | "Leerinstructie hoger (2 tegen 0)" is per constructie waar: het faalgeval is "geen leerblok". De test toont naleving, geen leerwinst. In claude.ai is de leerinstructie niet getest. | T7: "Omgeving: Claude Code." | Geverifieerd | "Nageleefd" schrijven in het oordeel; T7 ook in claude.ai draaien. |
| 16 | Klein | `testset.md`; kop van `kern.md` | De teststand is niet te reproduceren. De labelzin staat nergens meer. `testset.md` is op de testdag om 12:07 gewijzigd, tussen het opslaan van blok A (10:36) en blok B (12:28), zonder versieregel. | Kop testset: "Versie 1, 2026-11-09". | Geverifieerd (zoekopdracht, bestandsdatum); wat er wijzigde is niet te zien | Labelzin en de wijziging noteren in `test_v2.md`. |
| 17 | Klein | `7_overdracht\prompt_workflow.md`, stap Test | De herschrijving B36 schreef in `8_instructies\v2\` en `~/.claude/systeemprompt/`, mappen die de stap niet noemt. Dat gebeurde met akkoord, maar de workflow heeft geen pad voor herschrijven na zakken. T2 tot en met T8 zijn niet met 2.1 herhaald. | Workflow: "Schrijft in: 5_data\, 2_staat\, 7_overdracht\, 3_besluiten\." | Geverifieerd | Zie verbetering 10. |
| 18 | Klein | Fase 4 sectie 11; `testset.md`, Aanvullende controles | Twee geplande controles hebben geen uitkomst: `/doctor prompt-audit` komt na fase 5 nergens meer voor, en de voorrangscontrole is overgeslagen zonder besluit. | Zoeken op "prompt-audit" in `2_staat\`, `7_overdracht\` en `test_v2.md`: alleen fase 2. | Geverifieerd | Draaien, of als bewust niet gedaan noteren. |
| 19 | Klein | `8_instructies\v2\herzieningsprompt.md`, stap 2 en 6 | Negen domeinen in één sessie, terwijl B7 zegt dat dat te veel is en ronde C op een gebruikslimiet stopte. Stap 6 kopieert "met de bestaande kop erboven", zodat versie en datum in de kopie verouderen. | B7: "Negen domeinen zijn te veel voor een beurt". | Tekst geverifieerd; dat het misgaat is inferentie | Zie verbetering 6. |
| 20 | Klein | `kern.md`, eerste alinea, Lat en Afsluiting | "Domeinen" betekent eerst vier werkgebieden en daarna negen vakdomeinen, zodat "Daarbuiten" onbepaald is. Dubbel: "geen slotvragen" (Lat) en "na routinewerk geen" (Afsluiting). | Beide zinnen staan in de geplaatste tekst. | Geverifieerd | "Per vak:" boven de negen regels; de tweede vermelding vervalt in verbetering 4. |
| 21 | Klein | Koppen en staat | Verouderd of onjuist: `claude-md.md` kop "(bestaat nu niet)"; README "nog niet uitgevoerd"; voortgang noemt de review "Fable 5.1" in een claude.ai-chat; kern 2.0 telde 5.990 tekens, niet 5.992; `5_data\~$g_open_runs.docx` is een Word-lockbestand; de fase 4-tabel zegt "uit projectmappen halen" waar B31 twee mappen ongewijzigd laat. | Nageteld en nagelezen. | Geverifieerd | Opruimen vóór archiveren. |

### Herleidbaarheid en overige toetsvragen

- **Regels zonder grond:** geen. Twee regels hebben alleen het voorstel uit de bundel als grond (op de
  citaten in fase 4 vertrouwd). "Houd je standpunt vast" laat in T8 geen verschil zien: v1 zonder die
  regel houdt ook stand. "Verifieer met een test of commando" overlapt volgens fase 4 zelf deels met de app.
- **Randvoorwaarden:** de lengte klopt (6.093 tekens, marge 1.657). De werkgrens van 7.750 is wel de
  lengte van v1 zelf, geen gedocumenteerde limiet. De kern bevat geen verwijzingen die alleen in Code
  bestaan.
- **`reasoning_extraction`:** in de geplaatste teksten staat geen woord rond denkwerk (gezocht op denk,
  redene, think, stap voor stap, reasoning; alleen "met redenen", "think-aloud" en "Kleurendenken").
  Alleen T6 bevat het, met opzet.
- **Stijlregels:** ook de antwoorden zonder instructie bevatten geen em-dash. Die regel laat in deze
  steekproef dus geen verschil zien.

## 3. Verbeteringen

| # | Laag of onderdeel | Voorstel | Verwachte winst | Kosten | Prioriteit |
|---|---|---|---|---|---|
| 1 | `claude-md.md` | Nieuwe regel: "Zet in een Code-sessie geen vragenlijst in het bericht: een vraag hoort alleen in de afsluiting van de app." | Neemt het enige gemeten defect van v2 in Code weg (fout 3). | +110 tekens | Hoog |
| 2 | Kern, Eerlijkheid | Laatste regel wordt: "Is een dragende claim onzeker, noem dan hoogstens twee met hun check, in de lopende tekst; een onderbelicht risico alleen als het speelt." | Geen vast kopje meer en kortere antwoorden. v2 is in Code nu 48 tot 75% langer dan zonder instructie (T2: 915 tegen 523 woorden; T3: 339 tegen 229). In claude.ai is v2 juist 23 tot 30% korter dan v1. | +6 tekens | Hoog |
| 3 | Kern, memory | "... : geen to-do's, klantgegevens of regels die overal gelden." | Kern, app, `claude-md.md` regel 4 en B33 zeggen dan hetzelfde. | +18 tekens | Hoog |
| 4 | Kern, Afsluiting | Eerste regel wordt: "Stel aan het eind alleen een vraag als het antwoord mijn volgende stap verandert, hoogstens drie; een aanbod om meer te doen is geen vraag. Met een leerblok is de oefening de enige vraag. Heeft de omgeving een eigen afsluiting, dan staat een vraag alleen daar." | 8 van de 10 v2-antwoorden eindigen nu met vragen, deels aanbiedingen ("Wil je naast de mail een belscript [...]?"). | +41 tekens. Met 2 en 3 samen komt de kern op 6.158, marge 1.592 (B25 vraagt 1.500). | Middel |
| 5 | `claude-md.md` | Voorrang (+11), verificatie (+23), "ander model" (2 korter). | Lost fout 9, 10 en 11 op. | Met verbetering 1 samen 811 tekens | Middel |
| 6 | Herzieningsprompt | In drie rondes van drie domeinen, zoals fase 3. Wetsartikelen in de wettekst lezen of als niet gelezen markeren. Een U alleen met een meting. De kop van de kopie bijwerken. | Voorkomt afbreken op een limiet en dat niet-gelezen claims opnieuw doorschuiven. | 15 minuten | Middel |
| 7 | Bedrijfs-`CLAUDE.md` | Projectlat terugbrengen tot wat niet in de kern staat (risicoscore, eval set door de specialist, OR, AVG en AI Act). Het bedrijfsbesluit naar het besluitenlog van het stuurdocument, als hypothese met stopcriterium. | Geen dubbele regels die uiteen kunnen lopen; Claude blijft de aanname toetsen. | Naar schatting 600 tekens minder | Middel |
| 8 | Onderhoud memory | De kwartaalcontrole (B33) heeft geen herinnering; alleen 2027-05-09 staat in de agenda. Een terugkerende afspraak zetten, eerste keer februari 2027, met stap 16 van `prompt_claude_ai_memory.md` als controle. | Zonder aanleiding gebeurt de controle niet; zo raakte de memory eerder vervuild (fase 1: 9 van 38 items). | 5 minuten | Middel |
| 9 | Testset, volgende versie | Drie runs per prompt. Elke Code-run een eigen lege map. Outputs als markdown uit het transcript. Scoren in een verse chat zonder variantnamen. Toevoegen: een dubbelzinnige opdracht (toetst "vraag vooraf [...] en wacht"), T7 in claude.ai, de voorrangscontrole en een lengtecriterium. | Maakt de ongeteste regels toetsbaar en scheidt de scorer van de schrijver van de kern. | Naar schatting 1,5 uur per testronde | Middel |
| 10 | Workflow-prompt, volgende versie | Versieregel en wijzigingslog in de kop. "Klaar als" op kwaliteit in fase 3: wat in een instructie belandt, is in de primaire bron gelezen, met een maximale lengte per domein. Plaatsen: eerst een kopie van een bestaand doelbestand. Test: regels voor weigeringen, voor hertest na herschrijven en voor memory met bewijs. Elke regel die fase 4 als standaardgedrag schrapt, krijgt een testprompt. | Fase 4 schrapte vijf regels als standaardgedrag; de enige die toevallig werd getest, bleek nodig (B36). | 1 uur | Laag, pas bij hergebruik |
| 11 | Archiveren | R5 bevestigen vóór het verplaatsen: de kopieën, de herzieningsprompt en het archief staan op de externe schijf, de schijf met de Warning. | De geplaatste bestanden staan op C:, het spoor niet. | 10 minuten | Hoog |

De woordtellingen komen uit de Word-outputs, inclusief codeblokken, per run geteld.

## 4. Herscoring van de test

Gescoord met de criteria uit `8_instructies\v2\testset.md`. Voor de Code-runs 1, 1r, 2 en 7 is de
opmaak gecontroleerd in het transcript in plaats van in de Word-output.

| Run | Prompt en variant | Score in `test_v2.md` | Herscoring | Reden bij verschil |
|---|---|---|---|---|
| 1 | T1 Code, v2.0 | 0 | 0 | Transcript: drie `##`-koppen. |
| 1r | T1 Code, v2.1 | 2 | 1 | Geen `##`, wel de losse vette regel "Opmerkingen" boven vijf punten en een voorbehoud; 240 woorden tegen 198 zonder instructie. Volgens de eigen regel in `test_v2.md` zou dit 0 zijn. Het oordeel "minstens gelijk" blijft staan, want het vergelijkingspunt is 0. |
| 7 | T1 Code, zonder instructie | 0 | 0 | Naar de letter: het bericht eindigt op een aanbod als vraag. |
| 11r | T1 claude.ai, v2.1 | 2 | 2 | |
| 17 | T1 claude.ai, v1 | 2 | 2 | "Kort" is ruim genomen: 306 woorden. |
| 2 | T2 Code, v2 | 1 (5 van 7) | 1 (5 van 7) | |
| 5 | T2 Code, v2 met label | 1 (6 van 7) | 1 (6 van 7) | |
| 8 | T2 Code, zonder instructie | 1 (3 van 7) | 1 (4 van 7) | Punt 7 is gehaald. |
| 3, 6, 9 | T3, alle varianten | 2, 2, 2 | 2, 2, 2 | |
| 4 | T7 Code, v2 | 2 | 2 | Onder voorbehoud: het leerblok telt vier punten van twee tot drie zinnen, dus "hoogstens zes regels" is zo niet te toetsen. |
| 10b | T7 Code, zonder instructie | 0 | 0 | Naar de letter; zie fout 15. |
| 12 | T4 claude.ai, v2 | 2 | 2 | Onder voorbehoud van fout 2. |
| 16 | T4 claude.ai, v2 met label | 1 | 1 | |
| 18 | T4 claude.ai, v1 | 1 | 1 | |
| 13, 19 | T5 | 2, 2 | 2, 2 | |
| 14b, 20b | T6 zonder de denkwerkzin | 1, 1 | 1, 1 | |
| 15, 21 | T8 | 2, 2 | 2, 2 | |

Van de 21 herscoorde runs wijkt één score af (1r) en één puntentelling (8). De uitkomst per prompt
verandert niet; wat verandert, is de lezing van het geheel (fout 1). B35 is verdedigbaar: run 14c laat
zien dat de prompt zelf de pauze geeft.

## 5. Niet gecontroleerd

- **claude.ai:** of het voorkeurenveld de kern 2.1 bevat, de eindstand van de memory, en welke tekst per
  run in het veld stond bij blok D tot en met F.
- **De bundel met bestaand onderzoek:** `audit.md`, `CLAUDE_md_update.md` en `evals.md`. Op de citaten in
  fase 1, 2 en 4 is vertrouwd, ook voor "B35 volgt `evals.md`".
- **De bronnen van fase 3:** `domeinen.md` is met de fasebestanden vergeleken, niet de fasebestanden met
  hun bronnen. De bronnotities zijn niet gelezen. De wetsinhoud (art. 11.7 Tw, WOR, AI Act) is niet
  geverifieerd.
- **"Alleen toevoegen" in `beslispunten.md`:** de map heeft geen versiebeheer. Het sessieverslag van de
  test meldt zelf herstelacties aan B35, B36 en B38.
- **De app-instructies van 3 en 9 november:** alleen via fase 2 tabel D en fase 4 sectie 9. Fout 5 is
  daarnaast getoetst aan wat de app in de reviewsessie meegaf; dat kan sindsdien gewijzigd zijn.
- **Niet gelezen:** de transcripten van de workflow-sessies en de `CLAUDE.md` van twee andere projectmappen.
- **Niet gemeten:** het effect van kern 2.1 op T2 tot en met T8, en het gedrag van de kern op een ander
  model dan Opus 5.5.

## 6. Open punten die een bevinding veranderen

De vragen hierover zijn op 2026-11-10 in het gesprek gesteld; de antwoorden zijn hier nog niet verwerkt.

- **Gebruik van een ander model dan Opus 5.5.** Zo ja, dan is fout 10 groot in plaats van klein en moet
  de kern op dat model één keer door T1, T2 en T7.
- **Back-up van de externe schijf.** Is de oude `CLAUDE.md` van de projectmap daaruit terug te halen, dan wordt fout 7
  klein.
- **Uitvoer van stap 16 van `prompt_claude_ai_memory.md`.** Is die bewaard, dan is fout 6 voor claude.ai
  met één bestand gesloten.
