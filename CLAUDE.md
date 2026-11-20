# Hinweise für Claude

## Charaktere für Bilder
- Gespeicherte Figuren liegen in `charaktere/<name>/CHARAKTER.md`. Die Übersicht steht in `charaktere/README.md`.
- Sagt der Nutzer etwas wie „Bild mit Kai …“ oder „Szene mit <Name>“, gehe so vor:
  1. Lies zuerst das passende `CHARAKTER.md`.
  2. Baue den Prompt nach dem dortigen Bauplan: Stil-Vorlage, dann Szene, dann den Charakter-Baustein **wörtlich und unverändert**, dann der Konsistenz-Satz.
  3. Gib den Prompt in einem Codeblock aus, damit er sich kopieren lässt. Er ist auf Englisch, die Erklärung drumherum auf Deutsch.
  4. Erinnere den Nutzer daran, das Kai-Master-Bild als Referenz in Grok mit hochzuladen.
  5. Ist eine Bildgenerierung verfügbar (Tool oder API), erzeuge das Bild direkt.
  6. Trage die Szene in die Galerie-Tabelle des Charakterblatts ein, dann committen und pushen.
- Zeichne Figuren **nicht** selbst als SVG. Der Nutzer will Qualität wie bei Grok. Handgezeichnete Vektorgrafiken wurden abgelehnt.
- Das Repo ist öffentlich. Lege keine privaten Fotos des Nutzers ab, ohne vorher zu fragen.

## graphify

This project has a knowledge graph at graphify-out/ with god nodes, community structure, and cross-file relationships.

Rules:
- When graphify-out/graph.json exists, run `graphify query "<question>"` before your first grep, search or source-file read for a codebase question, and put this rule in every subagent prompt that explores code. Read raw files only for lines the graph or an earlier read already located. Use `graphify path "<A>" "<B>"` for relationships and `graphify explain "<concept>"` for focused concepts. When the answer is under a Markdown heading, `graphify section "<heading>"` prints that section's text, so the .md need not be opened. These return a scoped subgraph, usually much smaller than GRAPH_REPORT.md or raw grep output.
- If graphify-out/wiki/index.md exists, use it for broad navigation instead of raw source browsing.
- Read graphify-out/GRAPH_REPORT.md only for broad architecture review or when query/path/explain do not surface enough context.
- After modifying code, run `graphify update .` to keep the graph current (AST-only, no API cost).
- A committed graphify-out/graph.json is rewritten whole on every build, so a large diff to it in a pull request is expected. Do not flag it as churn or suggest skipping the graph rebuild or its hooks.
