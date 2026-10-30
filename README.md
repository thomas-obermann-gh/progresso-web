# Website Progresso Consulting Germany GmbH

Statische Website (HTML/CSS, kein JavaScript, keine Cookies, keine externen Abrufe). Sie läuft als Cloudflare Worker, der nur die Dateien aus `public/` ausliefert.

## Inhalt

| Datei | Zweck |
|---|---|
| `public/index.html` | Startseite (Englisch, Inhalte wie bisher) |
| `public/impressum.html` | Impressum, erreichbar unter `/impressum` |
| `public/datenschutz.html` | Datenschutzerklärung, erreichbar unter `/datenschutz` |
| `public/404.html` | Seite für ungültige Adressen |
| `public/assets/style.css` | Gestaltung, inkl. Dunkelmodus |
| `public/assets/fonts/` | Schrift IBM Plex Sans, lokal eingebunden (Lizenz: SIL OFL) |
| `public/_redirects` | Leitet die alte IONOS-Adresse `/privacy18741a6b` auf `/datenschutz` um |
| `public/_headers` | Sicherheits-Header |
| `public/robots.txt`, `public/sitemap.xml` | Für Suchmaschinen |
| `wrangler.jsonc` | Cloudflare-Einstellungen (Name des Workers, Ordner `public`, 404-Seite) |

## Veröffentlichen

Cloudflare baut und veröffentlicht automatisch bei jeder Änderung auf `main` (Workers Builds). Den Status zeigt GitHub beim jeweiligen Commit.

- **Testadresse:** im Cloudflare-Dashboard unter *Workers & Pages → progresso-web*, Endung `….workers.dev`
- **Eigene Domain:** im Worker unter *Einstellungen → Domains & Routen* `www.progresso-consulting.com` und `progresso-consulting.com` hinzufügen. Voraussetzung: Die Domain läuft bereits über die Cloudflare-Nameserver.

## Ändern

Datei in GitHub bearbeiten und speichern (*Commit*). Cloudflare veröffentlicht die Änderung nach etwa einer Minute.

## Vor dem Livegang prüfen

- Impressum: Anschrift, Geschäftsführer und Telefonnummer
- Cloudflare: Auftragsverarbeitungsvertrag (Customer DPA) für das Konto
- Datenschutz, Abschnitt 4: Google Workspace erst erwähnen, wenn die Mail umgezogen ist
