# Bitflip

Das Design fÃ¼r Lernpakete, Lernvideos, Folien, Cover und ArbeitsblÃ¤tter im Fachinformatiker-Unterricht. Hell, nerdig, zeitlos: ein isometrischer WÃ¼rfel mit Prompt, kleine Inseln, gestrichelte Wege und genau eine Akzentfarbe (Amber).

â€žBitflipâ€œ ist der Name des Designs, kein geprÃ¼fter Markenname.

## Inhalt

| Ordner | Was |
|---|---|
| `skill/bitflip/` | Claude-Skill: Regelwerk, Tokens, Logos, Inselszene, Vorlagen. Wird automatisch geladen, wenn Unterrichtsmaterial gestaltet wird. |
| `design-system/` | Dieselben Grundlagen als Design-System fÃ¼r Claude Design: README, `tokens.json`, Logos, Vorlagen-Karten. |

## SchnellÃ¼berblick

- **Farben:** WeiÃŸ `#FFFFFF`, FlÃ¤che `#F4F6F8`, Tinte `#0B0F14`, Amber `#FFB020` (einzige Akzentfarbe), Text-Amber `#A85F00`.
- **Schrift:** JetBrains Mono (Titel, Labels, Code) und Inter (FlieÃŸtext), beide von Google Fonts.
- **Merkmale:** Titel enden mit einem Amber-Unterstrich (Cursor), Inselszene, gestrichelte Wege, Amber-Balken.
- **Kontrast:** Amber als Schrift auf WeiÃŸ ist nicht erlaubt (1,9:1), dafÃ¼r Text-Amber (4,9:1).

Alle Regeln: [`skill/bitflip/references/design.md`](skill/bitflip/references/design.md).

## Skill installieren

Claude Code (alle Projekte):

```powershell
Copy-Item bitflip\skill\bitflip $env:USERPROFILE\.claude\skills\bitflip -Recurse
```

claude.ai: den Ordner `skill/bitflip` als Zip packen und in den Skill-Einstellungen hochladen.

## Design-System in Claude Design

Die Dateien unter `design-system/` sind die Quelle des Design-Systems â€žBitflipâ€œ. Das System in Claude Design als Standard markieren, dann nutzt jedes neue Design es automatisch.

## Hinweise

- Die Wortmarke in den Logo-Dateien ist als Text gesetzt (JetBrains Mono Bold). FÃ¼r Druck in Pfade umwandeln.
- Der Name â€žBitflipâ€œ ist ein Fachbegriff und wird auch von einer US-IT-Firma gefÃ¼hrt. Vor einer Ã¶ffentlichen Nutzung als Marke prÃ¼fen.
- Keine Lizenz festgelegt.
