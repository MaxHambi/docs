# Source: https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration

[MaxHambi](https://github.com/MaxHambi) / **[Lager-etiket](https://github.com/MaxHambi/Lager-etiket)** Public

- [Notifications](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket) You must be signed in to change notification settings
- [Fork 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)
- [Star 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)

# Konfiguration

[Jump to bottom](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#wiki-pages-box)

temp edited this page Sep 18, 2026 · [4 revisions](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration/_history)

# Konfiguration

[Permalink: Konfiguration](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#konfiguration)

Alle Einstellungen befinden sich in Karte **„3 Konfiguration"**. Sie entsprechen 1:1 der `config.json` — Import/Export hält Browser-Tool und PowerShell-Werkzeug synchron.

## Barcode-Aussehen

[Permalink: Barcode-Aussehen](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#barcode-aussehen)

| Feld | Bedeutung | Typischer Wert |
| --- | --- | --- |
| Balkenhöhe (px) | Höhe der Barcode-Balken | 180 |
| Strichbreite (px) | Dicke eines einzelnen Moduls | 4 |
| Rand (px) | Innenabstand rund um Barcode + Text | 20 |
| Schriftgröße (px) | Klartext unter dem Barcode | 54 |
| Textabstand (px) | Abstand Balken ↔ Klartext | 6 |
| Farbe | Balken + Klartext (Hex) | `#000000` |
| Schriftart | Klartext-Schriftfamilie | Consolas/monospace |

## Zielbereich (Platzierung auf der Vorlage)

[Permalink: Zielbereich (Platzierung auf der Vorlage)](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#zielbereich-platzierung-auf-der-vorlage)

| Feld | Bedeutung |
| --- | --- |
| Links / Oben (px) | Obere linke Ecke des Zielbereichs auf der Vorlage |
| Breite / Höhe (px) | Größe des Zielbereichs — **deaktiviert bei „Zielbereich automatisch"** (füllt dann bis zum Vorlagenrand) |
| Max. Breite / Höhe (%) | Wie viel Prozent des Zielbereichs der Barcode maximal einnehmen darf; der Barcode wird nur **verkleinert**, nie vergrößert |
| Verschiebung X / Y (px) | Feinjustierung nach rechts/unten (auch negativ) |

## Erweiterte Platzierung

[Permalink: Erweiterte Platzierung](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#erweiterte-platzierung)

Aufklappen „Erweiterte Platzierung" für Max.-Prozente und Verschiebung — die Felder wirken relativ, passen sich also automatisch an, wenn sich der Zielbereich ändert.

## Ausgabe

[Permalink: Ausgabe](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#ausgabe)

| Feld | Bedeutung | Standard |
| --- | --- | --- |
| Dateiname-Präfix | Vorangestellter Text, z. B. `lagerplatz_01A01.png` | `lagerplatz_` |
| DPI (Metadaten) | Auflösung im PNG — wichtig für exaktes Druckformat | 300 |
| Raster-DPI Barcode | Effektive Auflösung der Barcode-Rasterung — CLI und Browser nutzen denselben Wert, damit beide identische Schilder erzeugen | 600 |

## config.json laden / exportieren / zurücksetzen

[Permalink: config.json laden / exportieren / zurücksetzen](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#configjson-laden--exportieren--zur%C3%BCcksetzen)

- **Exportieren**: Speichert die aktuellen Formularwerte als `config.json` — kompatibel zum `lager`\-CLI (`pnpm cli generate`).
- **Laden**: Spielt eine `config.json` ein (z. B. eine pro Vorlage, wie `config-MV-C.json`).
- **Zurücksetzen**: Formular auf die Standardwerte (`DEFAULT_CONFIG` der Bibliothek) zurücksetzen.

**Zielbereich automatisch bleibt erhalten**: Der Zustand der Checkbox „Zielbereich automatisch" wird lokal gespeichert und überlebt einen Neuladen der Seite — genau wie das Overlay („Zielbereich einzeichnen") und die zuletzt gewählte Vorlage.

Typische Feld-Zuordnung „Was will ich ändern?":

| Wunsch | Einstellung |
| --- | --- |
| Größere Balken | Balkenhöhe ↑ |
| Größerer Klartext | Schriftgröße ↑ |
| Barcode kleiner relativ zum Zielbereich | Max. Breite/Höhe (%) ↓ |
| Barcode weiter nach unten/rechts | Verschiebung Y / X ↑ |
| Barcode nur in einer Ecke | „Zielbereich automatisch" abwählen, Breite/Höhe setzen |
| Andere Dateinamen | Dateiname-Präfix ändern |
| Anderes Druckformat | DPI ändern |

Nach jeder Änderung: [Vorschau und Erzeugung](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung) prüfen, bevor der vollständige Bestand läuft.

## Themes (Aussehen)

[Permalink: Themes (Aussehen)](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#themes-aussehen)

Im Protokoll-Panel (**„7 Protokoll & Einstellungen"**) wählt das Dropdown **„Theme (Catppuccin)"** das Aussehen:

| Theme | Eindruck |
| --- | --- |
| 🌸 Mocha | dunkel (Standard) |
| ☕ Macchiato | dunkel, etwas heller |
| 🌿 Frappé | dunkel, sanfter |
| 🌻 Latte | hell |

Die Wahl wird **im Browser gespeichert** und beim nächsten Start wieder hergestellt. Ohne eigene Wahl richtet sich das Tool nach der **Systemeinstellung** (dunkler Modus → Mocha, heller Modus → Latte).

## Gespeicherte Einstellungen

[Permalink: Gespeicherte Einstellungen](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#gespeicherte-einstellungen)

Das Tool merkt sich im Browser (localStorage) und stellt sie beim nächsten Start automatisch her:

- **Theme** — letzte manuelle Wahl
- **„Zielbereich einzeichnen"** — Overlay-Modus der Vorschau
- **Zuletzt gewählte Vorlage** — wird aus der Vorlagen-Galerie erneut geladen (eigene Dropzone-Dateien können nicht gemerkt werden)

Über den Browser-Datenschutz (Cookies/Site-Daten löschen) werden auch diese Einstellungen entfernt — das Tool funktioniert danach trotzdem normal, nur ohne Merkung.

## Konfiguration in der CLI

[Permalink: Konfiguration in der CLI](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration#konfiguration-in-der-cli)

Die CLI (`lager generate`, siehe [CLI](https://github.com/MaxHambi/Lager-etiket/wiki/CLI)) nutzt dieselbe `config.json` — per `--config` kann ein abweichender Pfad übergeben werden. Ohne Angabe gilt die Standard-Konfiguration des Projekts, identisch zur Web-App.

---

© 2026 Max Hambi · Lagerplatz-Barcode-Generator · Made with ❤️ · Verwendung außerhalb Auto-Kabel Rülzheim ist nicht gestattet!

**Benutzerhandbuch**

- [Home](https://github.com/MaxHambi/Lager-etiket/wiki/Home)
- [Schnellstart](https://github.com/MaxHambi/Lager-etiket/wiki/Schnellstart)
- [Vorlagen und Einträge](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge)
- [Konfiguration](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration)
- [Vorschau und Erzeugung](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung)
- [Login und Passwortschutz](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz)
- [Protokoll und Fehlerbehebung](https://github.com/MaxHambi/Lager-etiket/wiki/Protokoll-und-Fehlerbehebung)

**Installation & Betrieb**

- [Lokales Setup](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup)
- [CLI](https://github.com/MaxHambi/Lager-etiket/wiki/CLI)

**Nachschlagen**

- [FAQ](https://github.com/MaxHambi/Lager-etiket/wiki/FAQ)

---

**Werkzeuge**

- [Live-Tool (GitHub Pages)](https://maxhambi.github.io/Lager-etiket/)
- [Repository](https://github.com/MaxHambi/Lager-etiket)

### Clone this wiki locally