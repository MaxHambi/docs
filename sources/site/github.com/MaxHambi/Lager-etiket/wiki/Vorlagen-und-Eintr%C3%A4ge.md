# Source: https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge

[MaxHambi](https://github.com/MaxHambi) / **[Lager-etiket](https://github.com/MaxHambi/Lager-etiket)** Public

- [Notifications](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket) You must be signed in to change notification settings
- [Fork 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)
- [Star 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)

# Vorlagen und Einträge

[Jump to bottom](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#wiki-pages-box)

temp edited this page Sep 16, 2026 · [2 revisions](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge/_history)

# Vorlagen und Einträge

[Permalink: Vorlagen und Einträge](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#vorlagen-und-eintr%C3%A4ge)

## Vorlagen-Galerie nutzen

[Permalink: Vorlagen-Galerie nutzen](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#vorlagen-galerie-nutzen)

Die **Vorlagen-Galerie** (Karte „1 Vorlage") zeigt alle Vorlagen, die im Ordner `public/templates/` hinterlegt sind — anklicken genügt, kein Datei-Dialog nötig.

**Eigene Vorlagen hinterlegen** (Voraussetzung: Zugriff auf das Repo oder den lokalen Ordner `apps/web/public/templates/`):

1. PNG-Datei in `apps/web/public/templates/` ablegen.
2. In derselben Datei `templates.json` registrieren:

    ```json
    {
      "templates": [
        { "file": "MV-AB.png", "label": "MV Abteilung A–B" },
        { "file": "MV-C.png", "label": "MV Abteilung C" }
      ]
    }
    ```

3. Seite neu laden — die Karte erscheint in der Galerie.

**Eigene Datei ohne Hinterlegung:** Die Dropzone darunter nimmt weiterhin jedes PNG per Klick oder Drag & Drop. Das hebt die Galerie-Auswahl auf.

Die Vorschau unter der Galerie zeigt immer die aktuell gewählte Vorlage mit Name und Pixelgröße.

## PNG-Vorlage vorbereiten

[Permalink: PNG-Vorlage vorbereiten](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#png-vorlage-vorbereiten)

Die Vorlage ist das fertige Etiketten-Design als PNG; der Barcode wird später auf einem freien Bereich davon zentriert.

**Anforderungen an die Vorlage:**

- PNG-Format, weißer/heller Bereich für den Barcode.
- Der Bereich hinter dem Barcode muss frei von Linien, Logos oder Mustern sein — besonders die **Ruhezonen** links und rechts vom Barcode (freier Rand) dürfen nicht überlagert werden, sonst scannert das Schild nicht mehr zuverlässig.
- Vorlage nicht beschnitten oder mit Transparenz an kritischen Stellen laden; problematische Dateien vorher normalisieren (dazu `konvertieren.mjs` in der Haupt-README).

## Zielbereich festlegen

[Permalink: Zielbereich festlegen](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#zielbereich-festlegen)

Der Zielbereich bestimmt, **wo** auf der Vorlage der Barcode landet (Einstellungen in Karte „3 Konfiguration", Details: [Konfiguration](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration)):

- **Automatisch** (Häkchen gesetzt): Der Bereich füllt alles ab den Koordinaten „Links/Oben" bis zum Vorlagenrand — passt sich an jede Vorlagengröße an.
- **Manuell**: „Zielbereich automatisch" abwählen und „Breite/Höhe" fest eintragen — sinnvoll, wenn der Barcode nur in einer bestimmten Ecke stehen soll.
- **Feinjustierung**: „Verschiebung X/Y" (auch negativ) oder „Max. Breite/Höhe (%)" verkleinern.

Ob die Platzierung stimmt, zeigt die Vorschau mit eingezeichnetem Zielbereich ([Vorschau und Erzeugung](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung)).

## Config-Bibliothek: gespeicherte Konfigurationen

[Permalink: Config-Bibliothek: gespeicherte Konfigurationen](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#config-bibliothek-gespeicherte-konfigurationen)

Das Dropdown **„Gespeicherte Konfiguration"** (Karte „3 Konfiguration") listet alle Configs aus `apps/web/public/configs/`:

1. `config.json`\-Datei in `apps/web/public/configs/` ablegen (z. B. `gross.json` für große Schilder, `klein.json` für Restposten).
2. In `configs.json` registrieren:

    ```json
    {
      "configs": [
        { "file": "gross.json", "label": "Große Schilder" },
        { "file": "klein.json", "label": "Kleine Schilder" }
      ]
    }
    ```

3. Im Dropdown wählen — das Formular übernimmt alle Werte. Exportieren/importieren bleibt daneben weiterhin möglich.

**Tipp:** Die eigene Konfiguration exportieren, als JSON ablegen und in die Liste eintragen — so ist sie für alle Kollegen sofort verfügbar.

## Unterkategorien: Bereiche von Lagerplätzen

[Permalink: Unterkategorien: Bereiche von Lagerplätzen](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#unterkategorien-bereiche-von-lagerpl%C3%A4tzen)

Ab Karte „2 Lagerplätze" per **„Mehrere Bereiche"** aktivierbar:

- Jede Unterkategorie besteht aus **Start**, **Ende** und einem **Konfigurations-Dropdown**.
- Der Bereich wird aufsteigend inklusive expandiert: `01A01` bis `01A03` ergibt `01A01`, `01A02`, `01A03`.
- Das Ziffern-Suffix muss **gleich lang** sein (führende Nullen: `01A01 → 01A09`, nicht `01A1 → 01A9`).
- **„+ Unterkategorie"** legt weitere Bereiche an — z. B. eine pro Abteilung oder Regalreihe. Jede kann eine eigene Konfiguration haben (unterschiedliche Vorlagen-Größen pro Abteilung).
- Leere Unterkategorien (Start und Ende leer) werden übersprungen.
- **Duplikate über Unterkategorien hinweg** brechen die Erzeugung ab — so entstehen nie zwei Schilder mit demselben Barcode.
- Maximale Größen: 10 000 Einträge pro Bereich, 10 Unterkategorien.

## Eintragslisten pflegen (.txt)

[Permalink: Eintragslisten pflegen (.txt)](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge#eintragslisten-pflegen-txt)

- UTF-8, eine Zeile pro Platz, `#` am Zeilenanfang = Kommentar.
- Beim Laden mit genau **einem** Eintrag landet dieser direkt im Einzelfeld; bei mehreren Einträgen den Mehrfach-Modus nutzen (Hinweis erscheint im Protokoll).

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