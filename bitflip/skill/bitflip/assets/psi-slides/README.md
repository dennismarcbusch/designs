# Bitflip in psi-slides

Startvorlage für Folien mit [psi-slides](https://psi-slides.org/de/index.html) (mein Präsentationsstandard). Getestet mit psi-slides 2.3.0: baut ohne Fehler, lädt nichts von fremden Servern.

## Benutzen

1. Den Ordner kopieren, `source.md` anpassen (Titel, Inhalt).
2. In der psi-slides-App öffnen oder mit `node build.js pfad/zur/source.md` bauen. Der Ordner `fonts/` muss neben der `source.md` liegen.

## Was Bitflip hier abbildet

| Bitflip | psi-slides |
|---|---|
| Inter (Fließtext) | `fonts: {serif: Inter, sans: Inter}` mit den Dateien in `fonts/` |
| JetBrains Mono (Titel, Code) | `fonts: {mono: JetBrains Mono}`, liegt bei psi-slides bereits bei, keine Datei nötig |
| Amber als Akzent | `theme: light-orange` (Akzent `oklch(0.54 0.17 60)`, also dunkles Amber) |
| Weißer Grund, kühle Grautöne | `style: {neutrals: neutral}` |
| Kicker in Versalien | `style: {caps: on, headline: eyebrow}` |

## Grenzen

- **Amber `#FFB020` gibt es nicht.** psi-slides kennt nur feste Themen, keinen eigenen Farbwert. `light-orange` ist der nächste Ton und entspricht eher Text-Amber `#A85F00` als der leuchtenden Akzentfarbe. Das ist für Text auf Weiß sogar gewollt (Kontrast), die Amber-Fläche des Designs entsteht dadurch nicht.
- **Titel mit Cursor, Logo und Inselszene** sind nicht automatisch dabei. Bilder lassen sich über die Bildfunktionen von psi-slides einbinden (nicht getestet), das Logo als Datei aus `assets/logos/`.
- Wer die Schriften weitergibt, braucht die Lizenztexte (`OFL-Inter.txt` liegt bei).
