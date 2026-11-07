---
name: bitflip
description: Das Design "Bitflip" für Lernpakete, Lernvideos, Folien, Thumbnails, Cover und Arbeitsblätter im Fachinformatiker-Unterricht (hell, eine Akzentfarbe Amber, JetBrains Mono und Inter, isometrische Inseln mit Lernpaket-Würfel, Prompt-Cursor). Verwenden, sobald Material für Unterricht, Lernvideos oder Lernpakete gestaltet wird, ein Design oder Aussehen dafür gefragt ist oder "Bitflip" fällt, auch für Webseiten, SVG-Grafiken und Präsentationen im selben Stil.
---

# Bitflip: das Design

Bitflip ist das Design für Lernmaterial im IT-Unterricht: weiß, ruhig, nerdig. Ein isometrischer Würfel mit Prompt, kleine Inseln, gestrichelte Wege, **genau eine Akzentfarbe (Amber)**. Lies bei jeder Gestaltungsaufgabe zuerst `references/design.md`, die Regeln und Maße stehen dort.

## Schnellregeln

1. **Grund ist Weiß** (`#FFFFFF`), Flächen `#F4F6F8`, Text Tinte `#0B0F14`, Nebentext `#5B6573`.
2. **Eine Akzentfarbe:** Amber `#FFB020`. Keine zweite Farbe, keine Verläufe. Auf Amber steht immer Tinte. Amber als Schrift auf Weiß ist verboten (1,9:1): dafür Text-Amber `#A85F00`.
3. **Schrift:** JetBrains Mono (800) für Titel, Labels und Code, Inter für Fließtext. Titel enden mit einem Unterstrich in Amber (`Subnetting_`). Titel −0,05 em Laufweite, Kicker in Versalien mit +0,16 em.
4. **Logo nur aus den Dateien** in `assets/logos/` verwenden, nie nachzeichnen. Auf Amber-Flächen das Tinte-Zeichen (`bitflip-mark-ink.svg`).
5. **Illustration:** Isometrie im 30°-Raster, Kanten 1,5 px Tinte, Flächen weiß oder hellgrau. Farbe tragen nur das Lernpaket (Amber-Würfel mit `>_`) und die gestrichelten Wege. Bausteine und Maße siehe `references/design.md`, fertige Szene in `assets/scene.svg`.
6. **Texte:** Deutsch, Du-Form, kurz. Kicker: `MODUL 03 · NETZWERKTECHNIK`. Aufgaben beginnen mit einem Verb. Keine Emojis.
7. **Kontrast:** Text mindestens 4,5:1. Die geprüften Paare stehen in `references/design.md`.

## Dateien

- `references/design.md`: das vollständige Regelwerk (Farben, Schrift, Raster, Logo, Illustration, Vorlagen).
- `assets/tokens.css`: Farben, Schrift, Abstände und Radien als CSS-Variablen (hell, dunkel per `data-theme="dark"`). In HTML und Webseiten einbinden.
- `assets/tokens.json`: dieselben Tokens als Daten.
- `assets/logos/`: `bitflip-mark.svg`, `bitflip-mark-ink.svg`, `bitflip-logo.svg`, `bitflip-logo-dark.svg`.
- `assets/fonts/`: JetBrains Mono (400, 500, 700, 800) und Inter (400, 500, 700) als woff2 mit `fonts.css` und den OFL-Lizenztexten.
- `assets/psi-slides/`: getestete Startvorlage (`source.md`, `fonts/`, README) für Folien mit psi-slides.
- `assets/scene.svg`: die Inselszene (Server-Insel, Lernpaket mit Code-Fenster, Würfeltreppe).
- `assets/templates/video-title.html` und `task-slide.html`: lauffähige Vorlagen für Videotitel und Aufgabenfolie, 16:9.

## Vorgehen

1. `references/design.md` lesen, passende Vorlage aus `assets/templates/` als Ausgangspunkt nehmen oder neu aufbauen.
2. `assets/tokens.css` einbinden, keine eigenen Farben erfinden.
3. Schriften nur lokal einbinden (`assets/fonts/`, kommt über `tokens.css`). **Nie Google Fonts oder ein anderes CDN verlinken** (Datenschutz: IP-Übertragung an Dritte).
4. Vor dem Abgeben prüfen: eine Akzentfarbe, Amber nie als Text auf Weiß, Logo aus Datei, Titel mit Cursor.

## Bei Formaten

- **Folien mit psi-slides (Standard):** Vorlage in `assets/psi-slides/` (Inter, JetBrains Mono, Theme `light-orange`). psi-slides kennt keinen eigenen Akzentwert, der Amber-Ton ist dort dunkler als `#FFB020`. Nie eine Schrift von einem CDN laden.
- **PowerPoint/Folien:** nur wenn ausdrücklich verlangt (Standard ist psi-slides). 16:9, Rand 40 px entspricht etwa 1 cm. Titelfolie mit Szene rechts, Aufgabenfolie auf `#F4F6F8` mit dunklem Code-Fenster. Fußzeile: Wortmarke links, Zähler rechts.
- **Arbeitsblatt (A4):** Kopf mit Logo, Titel mit Amber-Balken, Namenszeile, nummerierte Aufgaben, Tabelle mit Tinte-Kopf, Merke-Kasten auf `#F4F6F8`. Muss auch in Schwarzweiß lesbar sein.
- **Video/Thumbnail:** Titel höchstens zwei Wörter pro Zeile, Thumbnail höchstens zwei Wörter insgesamt.
- **Name:** „Bitflip“ ist der Name des Designs, kein geprüfter Markenname.
