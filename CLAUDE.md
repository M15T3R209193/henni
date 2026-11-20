# Hinweise für Claude

## Muskelbilder fürs Split-Logbuch
- Neue Bilder von Muskelgruppen müssen dem Look in `muskelbilder/STIL.md` folgen: dunkle Glas-Hologramm-Figur, Zielmuskel leuchtet orange-gold, dunkler Hintergrund mit türkisen HUD-Linien, 1:1.
- Prompts dafür nach der Vorlage dort bauen. Schickt der Nutzer fertige Bilder, nach den Einbau-Schritten dort ins Artefakt übernehmen.

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
