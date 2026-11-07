# Bitflip

Das Design für Lernpakete, Videos, Folien und Arbeitsblätter im Fachinformatiker-Unterricht. Hell, nerdig, zeitlos: ein isometrischer Würfel mit Prompt, kleine Inseln, gestrichelte Wege und genau eine Akzentfarbe.

Der Name spielt auf zwei Dinge an: das Kippen eines Bits von 0 auf 1 (der Aha-Moment) und den „Flipped Classroom“ (Video zu Hause, Aufgaben im Unterricht). Bitflip ist hier der Name des Designs. Wer es öffentlich als Marke nutzen will, prüft vorher Marken und Domain.

## Grundhaltung

- **Hell vor dunkel.** Weiß ist der Grund. Dunkel gibt es nur als Code-Fenster, als Tinte für Text und als Variante für Videos.
- **Eine Akzentfarbe.** Amber (#FFB020) trägt alles Bunte: das Lernpaket, die Wege, Buttons. Es gibt keine zweite Akzentfarbe.
- **Mono gibt den Ton an.** JetBrains Mono für Titel und Labels, Inter für Fließtext.
- **Der Cursor.** Titel enden auf einem Unterstrich in Amber (`Subnetting_`). Das Logo heißt „bitflip_“.
- **Inseln statt Einzelbilder.** Illustrationen bestehen aus einer bis drei Inseln mit Server, Lernpaket und Würfeltreppe, verbunden durch gestrichelte Wege.

## Inhalt und Ton

- Sprache: Deutsch, Du-Form, kurz und konkret. Fachbegriffe bleiben englisch (VLAN, Subnetz, Switch), Erklärungen deutsch.
- Titel sind Substantive oder kurze Aufforderungen: „VLANs planen“, „Probier’s selbst“. Aufgaben beginnen mit einem Verb im Imperativ.
- Kicker in Versalien mit Mittelpunkt: `MODUL 03 · NETZWERKTECHNIK`.
- Zahlen mit führender Null in Zählern: `03 / 12`, `03:06`.
- Keine Emojis, keine Ausrufezeichen in Titeln.
- Platzhalter für Namen: „Dein Name“.

## Visuelle Grundlagen

### Farbe

| Rolle | Token | Wert |
|---|---|---|
| Grund | `paper` | #FFFFFF |
| Fläche | `surface` | #F4F6F8 |
| Text, Linie | `ink` | #0B0F14 |
| Nebentext | `muted` | #5B6573 |
| Akzent | `amber` | #FFB020 |
| Akzent als Text auf Hell | `amber-text` | #A85F00 |

Flächenverteilung einer typischen Folie: Weiß 62 %, Fläche 12 %, Tinte 10 %, Amber 16 %.

Kontrast: Tinte auf Weiß 19,1:1, Tinte auf Amber 10,4:1, Text-Amber auf Weiß 4,9:1, Nebentext auf Weiß 5,9:1, Amber auf Tinte 10,4:1. **Amber als Schrift auf Weiß ist nicht erlaubt** (1,9:1). Auf Amber steht immer Tinte, nie Weiß.

### Schrift

JetBrains Mono (Titel, Labels, Code) und Inter (Fließtext). Beide liegen lokal als woff2 in `assets/Fonts/` (SIL Open Font License), nie von Google Fonts oder einem CDN laden. Titel mit −0,05 em Laufweite, Kicker mit +0,16 em in Versalien. Stile: `display` 56/56, `title` 40/44, `subtitle` 24/29, `body` 17/27, `label` 12 Versalien, `code` 14/22.

### Raster und Form

8-px-Raster. Rand auf Folien und Videos 40 px, auf großen Flächen 64 px. Karten haben 20 px Radius, Code-Fenster 12 px, Chips und Buttons sind Pillen. Trenner sind Haarlinien (`line`) oder ein gestrichelter Amber-Weg.

### Erkennungsmerkmale

1. **Inselszene** auf Covern, Titeln und Thumbnails.
2. **Gestrichelter Weg** als Trenner und Fortschrittsanzeige: Amber-dark, Strich 6/5, runde Enden, Punkte in Amber mit Tinte-Rand.
3. **Amber-Balken** (72 × 6 px, Radius 3) unter dem Titel, dazu der Cursor am Titelende.

## Logo

Ein isometrischer Würfel mit `>_` auf zwei Flächen: das Prompt-Zeichen `>` auf der linken, der Unterstrich auf der rechten Fläche. Dazu die Wortmarke „bitflip_“ in JetBrains Mono Bold, „bit“ in Tinte, „flip_“ in Text-Amber.

Dateien: siehe die Gruppe „Logos“ unter Assets. Schutzraum: halbe Zeichenhöhe. Mindestgröße: Zeichen 24 px (6 mm), Logo 96 px (25 mm) Breite. Nicht strecken, nicht drehen, nicht umfärben. Auf Amber-Flächen das Tinte-Zeichen verwenden (`bitflip-mark-ink.svg`), auf Dunkel das normale Zeichen mit der hellen Wortmarke.

## Illustration: der Inselbaukasten

Alles isometrisch im 30°-Raster. Kanten 1,5 px in Tinte, keine Verläufe, keine Schatten außer einer flachen Ellipse unter jeder Insel (`#E4E8ED`).

**Bausteine:** Insel (flache Platte), Server-Blade (flacher Quader mit zwei LEDs: Amber und Weiß), neutraler Würfel, **Lernpaket** (Amber-Würfel mit Prompt), Code-Fenster (stehende Fläche mit Tinte-Kopfzeile und Zeilen in Amber und Grau).

**Farbregel:** Flächen sind weiß oder hellgrau (`iso-top`, `iso-left`, `iso-right`). Farbe tragen nur das Lernpaket (`amber-light`, `amber`, `amber-dark`) und die Wege. Pro Bild höchstens ein Amber-Würfel in der Mitte, leicht schwebend über einer Amber-Ellipse (Deckkraft 40 %).

**Geometrie:** Ein Würfel der Kantenlänge 80 hat die Flächen (Mittelpunkt als Ursprung):

- oben: `0,-80 69.3,-40 0,0 -69.3,-40`
- links: `-69.3,40 0,80 0,0 -69.3,-40`
- rechts: `69.3,40 0,80 0,0 69.3,-40`

Der Prompt `>` liegt auf der linken Fläche (`matrix(0.866 0.5 0 1 -69.3 40)`), der Unterstrich auf der rechten (`matrix(-0.866 0.5 0 1 69.3 40)`). Bodenflächen werden mit `matrix(0.866 0.5 -0.866 0.5 0 0)` gezeichnet.

**Wege:** gestrichelte Kurven in `amber-dark`, Strich 6/5, enden in Punkten. Keine Pfeile.

**Keine Texte** in Illustrationen, außer dem Prompt `>_`.

## Vorlagen

- **Video 16:9:** Titel, Kapitelkarte (große Ziffer mit Cursor), Lower Third (Tinte-Karte mit Zeichen), Aufgabenkarte (vollflächig Amber, Timer in Tinte), Endcard (zwei gestrichelte Felder), Thumbnail (zwei Wörter, Inselszene).
- **Folien 16:9:** Titel, Inhalt, Aufgabe (graue Fläche, Code-Fenster rechts), Zusammenfassung (Merkepunkte als Amber-Quadrate). Fußzeile mit Wortmarke links und Zähler rechts.
- **Arbeitsblatt A4:** Kopf mit Logo, Titel mit Balken, Namenszeile, nummerierte Aufgaben, Tabelle mit Tinte-Kopf, Merke-Kasten auf Fläche.
- **Cover 4:3, LMS-Kachel 16:9, Avatar 1:1:** Titel links, Inselszene rechts, Fortschritt als Amber-Balken.

Fertige Beispiele: Karten „VideoTitle“ und „TaskSlide“ unter Components.

## Für Agenten

Wenn Du mit diesem System ein Design baust:

1. Lies `tokens.json` und nutze nur diese Farben. Eine Akzentfarbe, keine zweite.
2. Grund ist `paper`. Text ist `ink` oder `muted`. Amber nie als Text auf Weiß, dafür `amber-text`.
3. Titel in JetBrains Mono 800 mit Cursor, Text in Inter.
4. Illustrationen nach dem Inselbaukasten. Keine Fotos, keine Verläufe, keine Emojis.
5. Logo nur aus den Dateien unter Assets, nie nachzeichnen.
6. Prüfe die Kontraste: Text mindestens 4,5:1.
