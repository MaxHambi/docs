# Source: https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup

[MaxHambi](https://github.com/MaxHambi) / **[Lager-etiket](https://github.com/MaxHambi/Lager-etiket)** Public

- [Notifications](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket) You must be signed in to change notification settings
- [Fork 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)
- [Star 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)

# Lokales Setup

[Jump to bottom](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup#wiki-pages-box)

MaxHambi edited this page Sep 18, 2026 · [1 revision](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup/_history)

# Lokales Setup

[Permalink: Lokales Setup](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup#lokales-setup)

Die Web-App läuft normalerweise auf [GitHub Pages](https://maxhambi.github.io/Lager-etiket/) — komplett im Browser, ohne Installation. Diese Seite beschreibt, wie du sie **lokal** betreibst, und was du für die **CLI** brauchst.

## Variante 1: Live-Tool nutzen (ohne Installation)

[Permalink: Variante 1: Live-Tool nutzen (ohne Installation)](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup#variante-1-live-tool-nutzen-ohne-installation)

[GitHub Pages](https://maxhambi.github.io/Lager-etiket/) öffnen, Passwort eingeben, loslegen. details: [Login und Passwortschutz](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz).

## Variante 2: Web-App lokal betreiben

[Permalink: Variante 2: Web-App lokal betreiben](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup#variante-2-web-app-lokal-betreiben)

Da die App zu 100 % offline im Browser läuft, genügt ein einfacher statischer Server:

1. Repository klonen und Abhängigkeiten installieren:

    ```shell
    git clone https://github.com/MaxHambi/Lager-etiket.git
    cd Lager-etiket
    npm install -g pnpm    # falls pnpm fehlt
    pnpm install
    pnpm build
    ```

2. Einen statischen Server im Web-Paket starten, z. B.:

    ```shell
    npx serve packages/web
    # oder: python -m http.server 8080 --directory packages/web
    ```

3. Im Browser `http://localhost:3000` (bzw. den Port des Servers) öffnen.

**Wichtig:** Die App muss über `http://…` geladen werden, nicht per `file://` — sonst blockiert der Browser das Laden von Vorlagen und Konfigurationsdateien.

## Variante 3: Entwicklung

[Permalink: Variante 3: Entwicklung](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup#variante-3-entwicklung)

Wer am Code arbeiten will:

```shell
pnpm install
pnpm dev:web      # Web-App mit Watch-Build
pnpm dev:cli      # CLI im Stub-Modus (Änderungen sofort ausführbar)
pnpm test         # Testsuite
pnpm build        # Produktions-Build aller Pakete
```

Benötigt wird **Node.js ≥ 24** und **pnpm**. Weitere Details für Beitragende: `CONTRIBUTING.md` im Repository.

## CLI nutzen

[Permalink: CLI nutzen](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup#cli-nutzen)

Für die Kommandozeilen-Erzeugung siehe [CLI](https://github.com/MaxHambi/Lager-etiket/wiki/CLI) — die Installation aus Variante 2 deckt die CLI mit ab.

## Nach dem Setup

[Permalink: Nach dem Setup](https://github.com/MaxHambi/Lager-etiket/wiki/Lokales-Setup#nach-dem-setup)

- Erste Schritte: [Schnellstart](https://github.com/MaxHambi/Lager-etiket/wiki/Schnellstart)
- Eigene Vorlagen: [Vorlagen und Einträge](https://github.com/MaxHambi/Lager-etiket/wiki/Vorlagen-und-Eintr%C3%A4ge)
- Einstellungen: [Konfiguration](https://github.com/MaxHambi/Lager-etiket/wiki/Konfiguration)

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