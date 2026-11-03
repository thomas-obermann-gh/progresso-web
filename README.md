# Website Progresso Consulting Germany GmbH

Statische Website auf Englisch und Deutsch (HTML/CSS, kein JavaScript, keine Cookies, keine externen Abrufe). Sie läuft als Cloudflare Worker, der nur die Dateien aus `public/` ausliefert.

## Inhalt

Jede Seite gibt es auf Englisch (Standard) und Deutsch. Der Umschalter EN/DE in der Kopfzeile besteht aus normalen Links, damit die Seite ohne JavaScript auskommt.

| Englisch | Deutsch | Zweck |
|---|---|---|
| `public/index.html` (`/`) | `public/de/index.html` (`/de/`) | Startseite |
| `public/legal-notice.html` (`/legal-notice`) | `public/de/impressum.html` (`/de/impressum`) | Impressum |
| `public/privacy.html` (`/privacy`) | `public/de/datenschutz.html` (`/de/datenschutz`) | Datenschutzerklärung |
| `public/thomas-obermann.html` (`/thomas-obermann`) | `public/de/thomas-obermann.html` (`/de/thomas-obermann`) | Profil Thomas Obermann |
| `public/pedro-averwald.html` (`/pedro-averwald`) | `public/de/pedro-averwald.html` (`/de/pedro-averwald`) | Profil Pedro Averwald |

| Datei | Zweck |
|---|---|
| `public/404.html` | Seite für ungültige Adressen, zweisprachig |
| `public/assets/style.css` | Gestaltung, inkl. Dunkelmodus |
| `public/assets/img/` | Portraits |
| `public/assets/fonts/` | Schrift IBM Plex Sans, lokal eingebunden (Lizenz: SIL OFL) |
| `public/_redirects` | Leitet alte Adressen (`/impressum`, `/datenschutz`, `/privacy18741a6b`) um |
| `public/_headers` | Sicherheits-Header |
| `public/robots.txt`, `public/sitemap.xml` | Für Suchmaschinen |
| `wrangler.jsonc` | Cloudflare-Einstellungen (Name des Workers, Ordner `public`, 404-Seite, Vorschau für Branches) |

Profilseiten bleiben anonym: keine Kundennamen, keine genauen Zeiträume, keine Länder, keine Geburtsdaten und kein PDF-Download.

Rechtlich maßgeblich ist die deutsche Fassung von Impressum und Datenschutzerklärung. Änderungen immer in beiden Sprachen vornehmen.

## Veröffentlichen

Cloudflare baut und veröffentlicht automatisch bei jeder Änderung auf `main` (Workers Builds). Andere Branches erscheinen als Vorschau unter `<branch>-progresso-web.thomasobermann.workers.dev`. Den Status zeigt GitHub beim jeweiligen Commit.

- **Testadresse:** im Cloudflare-Dashboard unter *Workers & Pages → progresso-web*, Endung `….workers.dev`
- **Eigene Domain:** im Worker unter *Einstellungen → Domains & Routen* `www.progresso-consulting.com` und `progresso-consulting.com` hinzufügen. Voraussetzung: Die Domain läuft bereits über die Cloudflare-Nameserver.

## Ändern

Datei in GitHub bearbeiten und speichern (*Commit*). Cloudflare veröffentlicht die Änderung nach etwa einer Minute.

## Wenn Pedro Averwald ausscheidet (31.12.2026)

Immer in beiden Sprachen:

- Startseite: Satz unter der Hauptüberschrift, Pedros Block in der Liste `crew` und `pedro-averwald.jpg` entfernen. Die zweispaltige Liste `.crew` auf eine Spalte umstellen.
- Referenzen aus seinen Projekten entfernen: Pharma (Response and Supply) und Lebensmittel (S&OP mit APO-Migration).
- Profilseite: `pedro-averwald.html` in beiden Sprachen löschen, aus `sitemap.xml` entfernen und in `_redirects` auf die Startseite umleiten.
- Impressum: Geschäftsführer anpassen.
- Bei einer Verlegung der GmbH: Anschrift in Impressum und Datenschutzerklärung anpassen.
