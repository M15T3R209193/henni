# Muskelbilder: Stil

Look für alle Muskelgruppen-Bilder im **Split-Logbuch** (Trainings-Artefakt: https://claude.ai/artifact/LNd3ppK5VN24j3u9vSG4EM).
Neue Bilder müssen genau so aussehen wie die vier vorhandenen: Brust, Rücken, Bizeps, Trizeps.

## Merkmale

- **Figur:** anonymer, athletischer Männerkörper ohne Gesicht und ohne Haare. Er ist aus dunklem, fast schwarzem, halbtransparentem Glas bzw. Hologramm-Material.
- **Oberfläche:** feine, helle Netz- und Faserlinien mit kleinen Lichtpunkten über den ganzen Körper, wie ein digitales Drahtgitter.
- **Zielmuskel:** Nur dieser Muskel leuchtet **warm orange-gold** (etwa #F5A524), mit sichtbaren Muskelfasern und einem leichten Glühen. Alles andere bleibt dunkel.
- **Hintergrund:** sehr dunkles Blauschwarz mit weichen, unscharfen Lichtpunkten (Bokeh) in Türkis und kleinen, schwebenden HUD-Strichen und Datenlinien in Türkis.
- **Ausschnitt:** quadratisch (1:1), Figur mittig, nur Oberkörper bzw. der Bereich, in dem der Muskel liegt. Vorderansicht bei Muskeln vorne, Rückansicht bei Muskeln hinten.
- **Licht:** dramatisch und filmisch, leichte Kanten-Lichter an der Silhouette, hoher Kontrast.

## Prompt-Vorlage für Grok

Ersetze `<MUSKEL>` durch die englische Bezeichnung und `<ANSICHT>` durch `front view` oder `back view`.

```
Cinematic 3D anatomy render, square 1:1. An anonymous athletic male body without face details or hair,
made of dark, almost black translucent glass-like holographic material, covered in fine glowing white
wireframe fiber lines and tiny light particles. <ANSICHT>, centered, framed on the area of the <MUSKEL>.
Only the <MUSKEL> glows in warm orange-gold (#F5A524) with visible luminous muscle fibers and a soft glow;
every other muscle stays dark. Background: very dark blue-black with soft teal bokeh lights and small
floating teal HUD data lines. Dramatic rim lighting, high contrast, clean, no text, no logos.
```

## Vorhandene Bilder

| Muskelgruppe | Schlüssel im Artefakt | Ansicht |
|---|---|---|
| Brust | `brust` | vorne |
| Rücken (Latissimus) | `ruecken` | hinten |
| Bizeps | `bizeps` | vorne, leicht seitlich |
| Trizeps | `trizeps` | hinten, leicht seitlich |

Mögliche Ergänzungen: Schultern (`shoulders / deltoids`, vorne), Beine vorne (`quadriceps`), Beinbeuger (`hamstrings`, hinten), Po (`glutes`, hinten), Waden (`calves`, hinten), Bauch (`abdominal muscles`, vorne), Nacken (`trapezius`, hinten).

## Einbau ins Artefakt

1. Bild auf 720 × 720 px verkleinern, als JPG (Qualität ca. 78) unter `img/<schlüssel>.jpg` mit dem Artefakt veröffentlichen.
2. Im Skript in `MUSCLES` einen Eintrag ergänzen (`label`, `pos` und `zoom` für den runden Ausschnitt um den leuchtenden Bereich).
3. In `guessMuscle()` passende Übungsnamen ergänzen, z. B. Schulterdrücken und Seitheben für Schultern.
4. Die Bilder kommen nur ins Artefakt, nicht ins Repo.
