---
title: Subnetting ohne Kopfschmerzen
subtitle: Modul 03 · Netzwerk
presenter: Dennis Busch
affiliation: Staatliche Berufsschule Lichtenfels
cover: display
lang: de
theme: light-orange
collapse: none
auto-fit: true
section: outline
section-mark: Modul
fonts:
  serif: Inter
  sans: Inter
  mono: JetBrains Mono
style:
  headline: eyebrow
  caps: on
  neutrals: neutral
  bold: accent-bold
  code: tint
---

## title: {#cover}

Subnetting_

# Grundlagen

## free: Was ein Subnetz tut {.standard #subnetz}

**Ein Subnetz teilt ein Netz in kleinere Abschnitte.** Jeder Abschnitt bekommt seine eigene Adresse und seine eigene Maske.

Ein Router verbindet die Abschnitte. Geräte im selben Subnetz erreichen sich direkt.

> note: Bei Bedarf live mit `ipcalc` zeigen.

## free: Aufgabe 03 · VLANs planen {.wide #aufgabe}

::: cards 2
- **Drei Subnetze anlegen**
  - nach Abteilung trennen
  - Vertrieb, Entwicklung, Verwaltung
- **Erreichbarkeit prüfen**
  - Ports dem VLAN zuordnen
  - mit `ping` testen
:::

```bash
vlan add 30
ping -c 3 10.0.30.1
```
