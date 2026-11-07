# Bitflip

Das Design für Lernpakete, Lernvideos, Folien, Cover und Arbeitsblätter im Fachinformatiker-Unterricht. Hell, nerdig, zeitlos: ein isometrischer Würfel mit Prompt, kleine Inseln, gestrichelte Wege und genau eine Akzentfarbe (Amber).

„Bitflip“ ist der Name des Designs, kein geprüfter Markenname.

## Inhalt

| Ordner | Was |
|---|---|
| `skill/bitflip/` | Claude-Skill: Regelwerk, Tokens, Logos, Inselszene, Vorlagen. Wird automatisch geladen, wenn Unterrichtsmaterial gestaltet wird. |
| `design-system/` | Dieselben Grundlagen als Design-System für Claude Design: README, `tokens.json`, Logos, Vorlagen-Karten. |

## Schnellüberblick

- **Farben:** Weiß `#FFFFFF`, Fläche `#F4F6F8`, Tinte `#0B0F14`, Amber `#FFB020` (einzige Akzentfarbe), Text-Amber `#A85F00`.
- **Schrift:** JetBrains Mono (Titel, Labels, Code) und Inter (Fließtext), beide von Google Fonts.
- **Merkmale:** Titel enden mit einem Amber-Unterstrich (Cursor), Inselszene, gestrichelte Wege, Amber-Balken.
- **Kontrast:** Amber als Schrift auf Weiß ist nicht erlaubt (1,9:1), dafür Text-Amber (4,9:1).

Alle Regeln: [`skill/bitflip/references/design.md`](skill/bitflip/references/design.md).

## Skill installieren

Claude Code (alle Projekte):

```powershell
Copy-Item skill\bitflip $env:USERPROFILE\.claude\skills\bitflip -Recurse
```

claude.ai: den Ordner `skill/bitflip` als Zip packen und in den Skill-Einstellungen hochladen.

## Design-System in Claude Design

Die Dateien unter `design-system/` sind die Quelle des Design-Systems „Bitflip“. Das System in Claude Design als Standard markieren, dann nutzt jedes neue Design es automatisch.

## Hinweise

- Die Wortmarke in den Logo-Dateien ist als Text gesetzt (JetBrains Mono Bold). Für Druck in Pfade umwandeln.
- Der Name „Bitflip“ ist ein Fachbegriff und wird auch von einer US-IT-Firma geführt. Vor einer öffentlichen Nutzung als Marke prüfen.
- Keine Lizenz festgelegt.
