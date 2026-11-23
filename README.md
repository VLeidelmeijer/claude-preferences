# claude-preferences

Een gelaagde set instructies voor Claude (claude.ai-chat en Claude Code), met de besluiten erachter en het bewijs
dat ze werken, voor zover dat bewijs reikt. Opgesteld in november 2026 voor Claude Opus 5.5 en Claude Fable 5.2.

## Over mij

Ik werk op het snijvlak van bedrijfskunde en techniek. Mijn werkgebieden: een eigen bedrijf in kennisborging
met een kennisbank en RAG, skill-opbouw en code (Python, SQL, Git), dienstverlening en acquisitie, en
loopbaanstrategie. Deze repo laat zien hoe ik AI inzet en stuur, niet alleen dat ik het gebruik.

## Wat het probleem was

Mijn oorspronkelijke instructie was één blok in het claude.ai-veld. Het laadde niet in Claude Code, waar ik
ongeveer 90% van mijn werk doe. Het bevatte labels als "MBB-niveau" in plaats van gedrag dat je kunt toetsen,
en een leerinstructie die tegen zichzelf in ging ("oefen het zelf" tegenover "houd de oplossing niet achter").

## Het resultaat in vier lagen

| Laag | Bestand | Waar het staat |
|---|---|---|
| Kern: dezelfde tekst in beide omgevingen | [`instructies/kern.md`](instructies/kern.md) | claude.ai-voorkeurenveld, en in Code via een import |
| Alleen voor Claude Code | [`instructies/claude-md.md`](instructies/claude-md.md) | `~/.claude/CLAUDE.md` |
| Per domein: lat, vaktaal, wat AI kan en wat ik zelf moet beheersen | [`instructies/domeinen.md`](instructies/domeinen.md) | `~/.claude/systeemprompt/domeinen.md`, gelezen bij een leerblok |
| Onderhoud van het domeinbestand | [`instructies/herzieningsprompt.md`](instructies/herzieningsprompt.md) | elke zes maanden of bij een nieuw model |

De ontwerpkeuzes in de kern:
- **Een lat in gedrag, geen label.** Vijf algemene regels en één regel per vak, zoals "koppel elke dragende claim
  aan iets wat haar kan weerleggen" en "betalingsbereidheid uit commitment, niet uit wat mensen zeggen te willen".
  Bij een test met en zonder label "MBB" scoorde het label niets extra (besluit B37).
- **Eerlijkheid boven gemak.** Geen claim in een cv of offerte die ik niet kan waarmaken; cijfers exact
  overnemen; een standpunt vasthouden tot ik nieuw bewijs geef.
- **Leren zonder de oplossing achter te houden.** Eerst het volledige antwoord, daarna een leerblok van hoogstens
  zes regels: wat AI hier kan, hoe ik het stuur en controleer, wat ik zelf moet beheersen.
- **Klein werk blijft klein.** Een feitelijke vraag krijgt geen kopjes, plan of slotvragen.

## Hoe het is gemaakt en getest

De workflow staat als sjabloon in [`werkwijze/workflow-sjabloon.md`](werkwijze/workflow-sjabloon.md): inventaris,
wat is veranderd, kwaliteitslat per domein onderzocht met bronnen en bewijssoort, analyse, uitwerken, plaatsen,
test, onafhankelijke review en red team.

| Stap | Uitkomst | Beperking |
|---|---|---|
| Test van v2 tegen de oude instructie ([`instructies/testset.md`](instructies/testset.md)) | v2 scoorde op elke prompt minstens zo hoog als de oude instructie. "Niet slechter" is wat de test draagt | Eén run per prompt. Mijn eerste conclusie "lat hoger" steunde op één punt en een niet-geverifieerde wetslezing; de review corrigeerde dat |
| Eindreview door een tweede model ([`werkwijze/review_fable.md`](werkwijze/review_fable.md)) | 21 bevindingen, geen kritieke, acht grote. Onder meer: de afsluitregel hield vragenlijsten in Code niet tegen en "zwakste claims" werd een vast kopje | Gebaseerd op bestanden en transcripten, niet op alle bronnen |
| Red team, twaalf aanvallen ([`werkwijze/redteam_uitkomsten.md`](werkwijze/redteam_uitkomsten.md)) | Zeven houden stand, vier falen gedeeltelijk, één op een klein punt. Geen verzonnen klant, cijfer of referentie. Ernstigste: een vreemde `CLAUDE.md` zette de chat om naar het Engels, en onder druk kwam een geschat cijfer met label op een cv | Eén run per aanval; claude.ai-aanvallen alleen benaderd; één aanval niet gedraaid |
| Hertest met v3 | Twee van de ernstigste aanvallen houden nu stand, één is verbeterd maar niet dicht | Eén run, alleen op Fable 5.2, niet op Opus 5.5 |

Wat niet bewezen is: een uitkomst van één run is een aanwijzing, geen kans. De leerinstructie is getest op
naleving, niet op leerwinst. De domeinbestanden steunen deels op bronnen die de onderzoekers alleen als
samenvatting zagen (gemarkeerd als "niet nagelezen"); wetgeving is niet in de wettekst gelezen en dit is geen
juridisch advies.

## De besluiten

[`besluiten/beslispunten.md`](besluiten/beslispunten.md) bevat de keuzes over de instructieset: wat is gekozen,
waarom, en welk alternatief is afgewezen. Het log is alleen toegevoegd, nooit herschreven; een later besluit
verwijst naar het eerdere (bijvoorbeeld B36 en B38 over de test, en B39 tot en met B42 over v3).

## Zelf gebruiken

1. Lees `instructies/kern.md` en `instructies/claude-md.md`.
2. Schrijf je eigen kern naar het model van `kern.md`: jouw domeinen, jouw regels per vak, jouw taal. Houd hem
   onder ongeveer 6.250 tekens; het veld nam bij mij 7.750 tekens aan, een officiële limiet heb ik niet gevonden.
3. Zet de kern op twee plekken: in het claude.ai-voorkeurenveld en als bestand `~/.claude/systeemprompt/kern.md`
   (UTF-8). Maak `~/.claude/CLAUDE.md` met de importregel bovenaan, met een pad zonder spaties: met spaties
   werkte de import bij mij niet.
4. Controleer dat het laadt: start een nieuwe Code-sessie in een andere map en vraag om de eerste zin van je
   instructies letterlijk te citeren.
5. Test met [`werkwijze/testset-sjabloon.md`](werkwijze/testset-sjabloon.md) (nieuwe sessie per prompt, ook met je
   oude instructie als vergelijkingspunt) en daarna met [`werkwijze/redteam.md`](werkwijze/redteam.md).

`kern.md` en `domeinen.md` zijn gemaakt voor mijn eigen domeinen; neem de opbouw over, niet de inhoud.

## Wat hier bewust niet in staat

Mijn memory-export en lokale memory, klant- en prospectgegevens, de ruwe testuitvoer en de projectbestanden van
mijn bedrijf. Verwijzingen in de besluiten en de werkwijze naar bestanden als `5_data` of `test_v2.md` wijzen naar
het volledige werkarchief en staan niet in deze repo.
