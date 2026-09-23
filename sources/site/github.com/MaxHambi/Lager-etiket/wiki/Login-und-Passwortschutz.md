# Source: https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz

[MaxHambi](https://github.com/MaxHambi) / **[Lager-etiket](https://github.com/MaxHambi/Lager-etiket)** Public

- [Notifications](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket) You must be signed in to change notification settings
- [Fork 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)
- [Star 0](https://github.com/login?return_to=%2FMaxHambi%2FLager-etiket)

# Login und Passwortschutz

[Jump to bottom](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz#wiki-pages-box)

temp edited this page Sep 16, 2026 · [1 revision](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz/_history)

# Login und Passwortschutz

[Permalink: Login und Passwortschutz](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz#login-und-passwortschutz)

Das Werkzeug ist clientseitig verschlüsselt: Ohne korrektes Passwort existiert die Anwendungslogik gar nicht im Klartext auf der Seite.

## Entsperren

[Permalink: Entsperren](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz#entsperren)

1. Seite öffnen → Begrüßungsbildschirm erscheint.
2. Das **Login-Fenster** („Zugang bestätigen") liegt darüber.
3. Passwort eingeben → **Entsperren**.

- **Falsches Passwort:** rote Meldung „Falsches Passwort. Bitte erneut versuchen.", das Feld leert sich. Einfach erneut versuchen.
- **Richtiges Passwort:** das Fenster schließt sich und das Werkzeug ist einsatzbereit ([Schnellstart](https://github.com/MaxHambi/Lager-etiket/wiki/Schnellstart)).

## Sitzung — nicht bei jedem Reload tippen

[Permalink: Sitzung — nicht bei jedem Reload tippen](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz#sitzung--nicht-bei-jedem-reload-tippen)

Die Entsperrung gilt **pro Browser-Tab bis zum Schließen**:

- Seite neu laden (F5) → sofort wieder im Werkzeug, ohne Passwort.
- Tab schließen und neu öffnen → Passwort wird erneut verlangt.
- In einem neuen Tab/Privatfenster → Passwort wird erneut verlangt.

Das ist bewusst so: Der Zugriff ist an die geöffnete Sitzung gebunden.

## Für Admins: Passwort festlegen / ändern

[Permalink: Für Admins: Passwort festlegen / ändern](https://github.com/MaxHambi/Lager-etiket/wiki/Login-und-Passwortschutz#f%C3%BCr-admins-passwort-festlegen--%C3%A4ndern)

Das Passwort steht **nirgends im Code** — es wird beim Build angegeben und verschlüsselt damit die gesamte Anwendungslogik (AES-256-GCM, PBKDF2-Schlüsselableitung).

**GitHub Pages (Live-Seite):**

1. Repository → _Settings → Environments → github-pages_ → _Environment secrets_ → `APP_PASSWORD`.
2. Wert setzen (oder ändern) — das ist das Passwort der Live-Seite.
3. Beim nächsten automatischen Deploy (Push auf `master`) bzw. manuell über _Actions → Update GitHub Pages → Run workflow_ wird die Seite mit dem neuen Passwort gebaut.
4. Danach gilt: **neues** Passwort im Browser (ggf. Tab schließen, damit keine alte Sitzung dazwischenfunkt).

**Lokal (geschützter Build):**

```powershell
node build.mjs --password "DeinPasswort"
```

Ohne Passwort-Parameter entsteht ein unverschlüsselter Entwicklungs-Build (kein Login) — nur für die Entwicklung verwenden.

**Grenze des Schutzes (ehrlich gesagt):** Der Schutz verhindert die Nutzung ohne Passwort zuverlässig — aber nach dem Entsperren liegt die Logik im Browserspeicher des jeweiligen Nutzers. Es ist eine Türschloss- Lösung, kein Tresor.

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