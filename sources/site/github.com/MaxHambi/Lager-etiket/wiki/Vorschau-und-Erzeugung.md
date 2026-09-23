# Source: https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung

[MaxHambi](https://github.com/MaxHambi) / **[Lager-etiket](https://github.com/MaxHambi/Lager-etiket)** Public

- [Notifications](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket) You must be signed in to change notification settings
- [Fork 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)
- [Star 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)

# Vorschau und Erzeugung

[Jump to bottom](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#wiki-pages-box)

MaxHambi edited this page Sep 18, 2026 · [4 revisions](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung/_history)

# Vorschau und Erzeugung

[Permalink: Vorschau und Erzeugung](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#vorschau-und-erzeugung)

## Einzelvorschau (Karte „4 Vorschau")

[Permalink: Einzelvorschau (Karte „4 Vorschau")](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#einzelvorschau-karte-4-vorschau)

Bevor du hunderte Schilder erzeugst, prüfe **einen** Eintrag:

1. Im Einzelfeld (Karte „2") einen Lagerplatz eingeben — oder im Mehrfach-Modus den ersten Eintrag der ersten Unterkategorie nutzen.
2. Optional: **„Zielbereich einzeichnen"** — eine gestrichelte Linie zeigt, in welchem Bereich der Barcode zentriert wird. Der Modus wird gemerkt und beim nächsten Start wiederhergestellt (siehe [Konfiguration](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration) → Gespeicherte Einstellungen).
3. **„Vorschau erzeugen"** klicken.
4. **Klick auf das Bild** öffnet die **Großansicht** (Lightbox) — praktisch, um kleine Details zu prüfen. Schließen per Klick auf eine freie Stelle, das × oder die Taste **Esc**.

**Prüfen:**

- Barcode vollständig im Zielbereich, nichts läuft über die Vorlage.
- Klartext unter dem Barcode lesbar.
- Keine Überlappung mit Logos/Linien der Vorlage.
- Protokoll zeigt Position und Größe des Barcodes in Pixeln.

Die gestrichelte Linie nutzt die Akzentfarbe des aktiven Designs.

## Alle Schilder erzeugen (Karte „5 Erzeugen")

[Permalink: Alle Schilder erzeugen (Karte „5 Erzeugen")](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#alle-schilder-erzeugen-karte-5-erzeugen)

1. **„Alle Schilder erzeugen"** klicken (aktiv, sobald eine Vorlage gewählt ist und mindestens ein gültiger Eintrag bzw. Bereich existiert).
2. Der Fortschrittsbalken zeigt den Lauf; jede erzeugte Datei steht im Protokoll („Erstellt: …"). Bei mehreren **Unterkategorien** werden alle Bereiche nacheinander abgearbeitet — jede mit ihrer gewählten Konfiguration.
3. Enthält die Eingabe doch ein Duplikat (auch über Unterkategorien hinweg), bricht der Lauf sofort mit einer Meldung ab — korrigieren und erneut starten.
4. Fehler bei einzelnen Einträgen (z. B. unkodierbare Zeichen) erscheinen im Protokoll als **verständliche deutsche Meldung mit Lösungshinweis** (z. B. „Zeichen an Position 3 ist kein ASCII — die installierte etiket-Version kodiert es nicht in den Barcode…") und stoppen den Lauf nicht — die restlichen Schilder werden normal erzeugt.
5. Fehlt die Config-Datei einer Unterkategorie (im Dropdown gewählt, aber nicht hinterlegt), greift automatisch die globale Konfiguration; eine Warnung erscheint im Protokoll.

## Ergebnisse verwalten (Karte „6 Ergebnisse")

[Permalink: Ergebnisse verwalten (Karte „6 Ergebnisse")](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#ergebnisse-verwalten-karte-6-ergebnisse)

- Jedes fertige Schild erscheint als Thumbnail mit Dateinamen.
- **Klick auf das Thumbnail** öffnet die Großansicht (Lightbox).
- **↓** lädt ein einzelnes PNG herunter.
- Ein neuer Lauf ersetzt die bisherigen Ergebnisse.

## ZIP herunterladen

[Permalink: ZIP herunterladen](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#zip-herunterladen)

**„Alle als ZIP herunterladen"** (der bewusst **große** Button) packt alle Schilder des letzten Laufs in `lagerplatz-schilder.zip` (unkomprimiert gespeichert, nur gebündelt).

## Drucken — die Regeln

[Permalink: Drucken — die Regeln](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#drucken--die-regeln)

1. **In tatsächlicher Größe drucken**, nie „An Seite anpassen" / „an Rahmen anpassen".
2. Die DPI-Metadaten im PNG sorgen dafür, dass Druckprogramme die physische Größe korrekt übernehmen.
3. Ruhezonen nicht überkleben oder laminieren, ohne zu prüfen.
4. Vor dem Großlauf: [Protokoll und Fehlerbehebung](https://github.com/MaxHambi/Lager-etiket/wiki/Protokoll-und-Fehlerbehebung) und die Produktionsprüfung in der Haupt-README beachten (Scanner-Test unter realer Beleuchtung, auf dem echten Material).

## Gleiches Ergebnis in der CLI

[Permalink: Gleiches Ergebnis in der CLI](https://github.com/MaxHambi/Lager-etiket/wiki/Vorschau-und-Erzeugung#gleiches-ergebnis-in-der-cli)

Wer die Erzeugung automatisieren will, nutzt die [CLI](https://github.com/MaxHambi/Lager-etiket/wiki/CLI): `lager generate` erzeugt aus denselben Einträgen und derselben Konfiguration **pixelgleiche** Schilder — beide Wege teilen sich die Rendering-Engine (etiket, Code 128).

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