# Source: https://github.com/MaxHambi/Lager-etiket/wiki

[MaxHambi](https://github.com/MaxHambi) / **[Lager-etiket](https://github.com/MaxHambi/Lager-etiket)** Public

- [Notifications](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket) You must be signed in to change notification settings
- [Fork 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)
- [Star 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)

# Home

[Jump to bottom](https://github.com/MaxHambi/Lager-etiket/wiki#wiki-pages-box)

MaxHambi edited this page Sep 18, 2026 · [4 revisions](https://github.com/MaxHambi/Lager-etiket/wiki/Home/_history)

# Lagerplatz-Barcode-Generator — Benutzerhandbuch

[Permalink: Lagerplatz-Barcode-Generator — Benutzerhandbuch](https://github.com/MaxHambi/Lager-etiket/wiki#lagerplatz-barcode-generator--benutzerhandbuch)

Willkommen im Benutzerhandbuch für die **Anwendung** des Werkzeugs. Hier findest du alles, was du zum täglichen Arbeiten brauchst — keine Entwickler-Themen (dafür siehe README und `docs/` im Repository).

## Seiten

[Permalink: Seiten](https://github.com/MaxHambi/Lager-etiket/wiki#seiten)

| Seite | Inhalt |
| --- | --- |
| **[Schnellstart](https://github.com/MaxHambi/Lager-etiket/wiki/Schnellstart)** | In 5 Minuten zum ersten Schild (Web-App) |
| **[Vorlagen und Einträge](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge)** | PNG-Vorlagen vorbereiten, Eintragslisten pflegen |
| **[Konfiguration](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration)** | Alle Einstellungen im Formular und in config.json |
| **[Vorschau und Erzeugung](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung)** | Einzelvorschau, Stapel-Lauf, ZIP-Download |
| **[Login und Passwortschutz](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz)** | Entsperren, Sitzung, Passwort-Änderung (für Admins) |
| **[Protokoll und Fehlerbehebung](https://github.com/MaxHambi/Lager-etiket/wiki/Protokoll-und-Fehlerbehebung)** | Log verstehen, typische Fehler lösen |
| **[Lokales Setup](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup)** | Web-App lokal betreiben, ohne GitHub Pages |
| **[CLI](https://github.com/MaxHambi/Lager-etiket/wiki/CLI)** | Schilder per Kommandozeile erzeugen (`lager generate` …) |
| **[FAQ](https://github.com/MaxHambi/Lager-etiket/wiki/FAQ)** | Häufig gestellte Fragen und Antworten |

## Zwei Wege zum fertigen Schild

[Permalink: Zwei Wege zum fertigen Schild](https://github.com/MaxHambi/Lager-etiket/wiki#zwei-wege-zum-fertigen-schild)

| | **Web-App** | **CLI** |
| --- | --- | --- |
| Für | tägliche Arbeit im Lager | Automatisierung, Batch-Skripte |
| Start | [GitHub Pages](https://maxhambi.github.io/Lager-etiket/) öffnen | `lager generate --start 01A01 --end 01A12 --out output` |
| Eingabe | Formular, Vorlagen-Galerie, .txt-Liste | Argumente, .txt-Liste |
| Ausgabe | Thumbnails + ZIP-Download | PNG-Dateien in einem Ordner |
| Details | [Schnellstart](https://github.com/MaxHambi/Lager-etiket/wiki/Schnellstart) | [CLI](https://github.com/MaxHambi/Lager-etiket/wiki/CLI) |

Beide Wege nutzen **dieselbe Rendering-Engine** (Code 128 via [etiket](https://github.com/productdevbook/etiket)) — ein Lagerplatz sieht in der Web-App und aus der CLI pixelidentisch aus.

## Das Wichtigste in einem Satz

[Permalink: Das Wichtigste in einem Satz](https://github.com/MaxHambi/Lager-etiket/wiki#das-wichtigste-in-einem-satz)

Vorlage laden → Lagerplätze eintragen → Vorschau prüfen → „Alle Schilder erzeugen" → als ZIP herunterladen und drucken.

## Gültige Regeln nicht vergessen

[Permalink: Gültige Regeln nicht vergessen](https://github.com/MaxHambi/Lager-etiket/wiki#g%C3%BCltige-regeln-nicht-vergessen)

- Das Werkzeug läuft **komplett offline** — keine Internetverbindung nötig.
- **Doppelte Einträge brechen die Erzeugung ab** (bewusst, damit nie zwei Schilder mit demselben Barcode entstehen).
- In tatsächlicher Größe drucken, **nicht** „An Seite anpassen".
- Vor großen Läufen immer erst 2–3 Testschilder prüfen (idealerweise mit einem echten Scanner).
- Das Tool merkt sich Theme, Overlay-Modus und die letzte Vorlage im Browser — beim nächsten Start ist alles wie du es verlassen hast.

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