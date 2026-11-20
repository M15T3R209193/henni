# Graph Report - henni  (2026-11-20)

## Corpus Check
- Corpus is ~29,312 words - fits in a single context window. You may not need a graph.

## Summary
- 166 nodes · 297 edges · 8 communities
- Extraction: 92% EXTRACTED · 8% INFERRED · 0% AMBIGUOUS · INFERRED: 24 edges (avg confidence: 0.88)
- Token cost: 396,784 input · 0 output

## Community Hubs (Navigation)
- Zentrale: Aufgaben-Rendering
- Tagwerk: KI-Schritte & Feiern
- Kai-Charakter & Grok-Prompts
- Zentrale: Speicher & Sync
- Termine: Kategorien & Formular
- Zentrale: Dashboard-Ansichten
- Zentrale: Navigation & Undo
- Fotos & Bildvarianten

## God Nodes (most connected - your core abstractions)
1. `Klick-Handler (document click)` - 19 edges
2. `zeichne()` - 17 edges
3. `renderDash()` - 14 edges
4. `aendern()` - 10 edges
5. `zFlow()` - 10 edges
6. `cloudStarten()` - 9 edges
7. `renderZLive()` - 9 edges
8. `fortschritt()` - 9 edges
9. `state {termine, aufgaben}` - 9 edges
10. `terminGruppen()` - 8 edges

## Surprising Connections (you probably didn't know these)
- `Bild-Workflow für Charaktere` --semantically_similar_to--> `So funktioniert's`  [INFERRED] [semantically similar]
  CLAUDE.md → charaktere/README.md
- `3D-Knete-Look (clay, b3, Kacheln)` --semantically_similar_to--> `Leuchtende System-Panels (Kalender · Tag · Übersicht)`  [INFERRED] [semantically similar]
  tagwerk/index.html → termine/index.html
- `CATS (Haushalt, Arbeit, Hobby, Termin, Persönlich)` --semantically_similar_to--> `CATS (Gym, Kunst, Arbeit, Privat, Sonstiges)`  [INFERRED] [semantically similar]
  tagwerk/index.html → termine/index.html
- `normalize()` --semantically_similar_to--> `normalize()`  [INFERRED] [semantically similar]
  tagwerk/index.html → termine/index.html
- `Speichern: Konto (db), Gerät als Rückfall` --semantically_similar_to--> `Speicher: Artifact-Datenbank, sonst Browser`  [INFERRED] [semantically similar]
  tagwerk/index.html → termine/index.html

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **zeichne()-Renderpipeline** — zentrale_index_zeichne, zentrale_index_renderkopf, zentrale_index_renderdash, zentrale_index_renderkalender, zentrale_index_rendertagkopf, zentrale_index_rendertagtermine, zentrale_index_rendertagaufgaben, zentrale_index_renderalletermine, zentrale_index_renderalleaufgaben, zentrale_index_hinweise [EXTRACTED 1.00]
- **Speicher-Flow Konto/lokal** — zentrale_index_speicherstarten, zentrale_index_cloudstarten, zentrale_index_lokalstarten, zentrale_index_speichern, zentrale_index_schreiben, zentrale_index_speicherfehler [EXTRACTED 1.00]
- **Zentrale-Widgets** — zentrale_index_renderzplayer, zentrale_index_renderzlive, zentrale_index_renderzprog, zentrale_index_renderzchart, zentrale_index_zflow [EXTRACTED 1.00]
- **Kai-Prompt-Aufbau (Stil, Szene, Baustein, Konsistenz-Satz)** — charaktere_kai_charakter_prompt_bauplan, charaktere_kai_charakter_stil_a, charaktere_kai_charakter_stil_b, charaktere_kai_charakter_stil_c, charaktere_kai_charakter_charakter_baustein, charaktere_kai_charakter_konsistenz_satz, charaktere_kai_charakter_kai_master [EXTRACTED 1.00]
- **Tagwerk Countdown-Ablauf** — tagwerk_index_starttimer, tagwerk_index_ontick, tagwerk_index_alarmon, tagwerk_index_chime, tagwerk_index_stoptimer, tagwerk_index_renderfocus [EXTRACTED 1.00]
- **Termine Speicherpfad (db oder localStorage)** — termine_index_boot, termine_index_saveitem, termine_index_removeitem, termine_index_dbcall, termine_index_errortext [EXTRACTED 1.00]
- **Photo edit variants of the original mirror selfie** — bilder_original, bilder_variante1_clean_pro, bilder_variante2_cinematic, bilder_variante3_schwarzweiss [INFERRED 0.95]

## Communities (8 total, 0 thin omitted)

### Community 0 - "Zentrale: Aufgaben-Rendering"
Cohesion: 0.12
Nodes (34): aufgabeHtml(), aufgabenSortiert(), datumChip(), erledigtTage(), esc(), fokusMerken(), fokusSetzen(), fortschritt() (+26 more)

### Community 1 - "Tagwerk: KI-Schritte & Feiern"
Cohesion: 0.09
Nodes (27): aiSplitDraft(), aiSplitItem(), aiSteps() – KI-Unteraufgaben, alarmOn(), burst() – Konfetti, celebrate(), commit(), connect() (+19 more)

### Community 2 - "Kai-Charakter & Grok-Prompts"
Cohesion: 0.15
Nodes (20): Aussehen (verbindlich), Charakter-Baustein, Galerie, Grok, Häufige Fehler, Kai – Charakterblatt, Kai-Master-Bild, Konsistenz-Satz (+12 more)

### Community 3 - "Zentrale: Speicher & Sync"
Cohesion: 0.17
Nodes (17): aendern(), Beispieleinträge (beispiel: true), beispiele(), Speicher im Claude-Konto (window.claude db/user), cloudStarten(), hinweise(), localStorage-Speicher (tagwerk:v1, tagwerk:cache, tagwerk:abgleich), lokalLesen() (+9 more)

### Community 4 - "Termine: Kategorien & Formular"
Cohesion: 0.16
Nodes (16): CATS (Haushalt, Arbeit, Hobby, Termin, Persönlich), normalize(), normItem(), boot(), CATS (Gym, Kunst, Arbeit, Privat, Sonstiges), dbCall(), errorText(), normalize() (+8 more)

### Community 5 - "Zentrale: Dashboard-Ansichten"
Cohesion: 0.12
Nodes (15): Als Nächstes: Termin-Player, iPhone-Ansichten über untere Leiste (data-ansicht), Bereiche-Kacheln (wie Geräte), Farb-Tokens :root mit Dark-Mode, Fortschritt: Aufgaben wie Akkustände, Kennzahlen, Schnellaktionen, stempel() (+7 more)

### Community 6 - "Zentrale: Navigation & Undo"
Cohesion: 0.25
Nodes (15): bereit(), eintragenAmTag(), gehZu(), hinweis(), Klick-Handler (document click), neueAufgabe(), renderModus(), rueckgaengig() (+7 more)

### Community 7 - "Fotos & Bildvarianten"
Cohesion: 0.25
Nodes (8): Original Photo (mirror selfie), Mirror Selfie Scene (round mirror, athletic pose), Variant 1: Clean Pro Edit, Clean Professional Retouch Style, Variant 2: Cinematic Grade, Cinematic Color Grade, Variant 3: Black and White, High-Contrast Monochrome Conversion

## Ambiguous Edges - Review These
- `Charakter-Baustein` → `Szene: Steinmetz (Stil A)`  [AMBIGUOUS]
  charaktere/kai/CHARAKTER.md · relation: references

## Knowledge Gaps
- **11 isolated node(s):** `Beispieleinträge (beispiel: true)`, `Farb-Tokens :root mit Dark-Mode`, `graphify-Anleitung`, `Typische Posen`, `Häufige Fehler` (+6 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 20 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `zeichne()` connect `Zentrale: Aufgaben-Rendering` to `Zentrale: Speicher & Sync`, `Zentrale: Navigation & Undo`?**
  _High betweenness centrality (0.094) - this node is a cross-community bridge._
- **What connects `Beispieleinträge (beispiel: true)`, `Farb-Tokens :root mit Dark-Mode`, `graphify-Anleitung` to the rest of the system?**
  _11 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Zentrale: Aufgaben-Rendering` be split into smaller, more focused modules?**
  _Cohesion score 0.12233285917496443 - nodes in this community are weakly interconnected._
- **Why does `renderDash()` connect `Zentrale: Aufgaben-Rendering` to `Zentrale: Speicher & Sync`, `Zentrale: Dashboard-Ansichten`?**
  _High betweenness centrality (0.070) - this node is a cross-community bridge._
- **Should `Tagwerk: KI-Schritte & Feiern` be split into smaller, more focused modules?**
  _Cohesion score 0.08994708994708994 - nodes in this community are weakly interconnected._
- **Why does `Klick-Handler (document click)` connect `Zentrale: Navigation & Undo` to `Zentrale: Aufgaben-Rendering`, `Zentrale: Speicher & Sync`, `Zentrale: Dashboard-Ansichten`?**
  _High betweenness centrality (0.069) - this node is a cross-community bridge._

### Low-confidence Hints
_AMBIGUOUS edges — the extractor was unsure. Verify before acting on these._

- **What is the exact relationship between `Charakter-Baustein` and `Szene: Steinmetz (Stil A)`?**
  _Edge tagged AMBIGUOUS (relation: references) - confidence is low._