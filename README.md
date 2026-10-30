# Website Progresso Consulting Germany GmbH

Statische Website (HTML/CSS, kein JavaScript, keine Cookies, keine externen Abrufe) für Cloudflare Pages.

## Inhalt

| Datei | Zweck |
|---|---|
| `index.html` | Startseite (Englisch, Inhalte wie bisher) |
| `impressum.html` | Impressum, erreichbar unter `/impressum` |
| `datenschutz.html` | Datenschutzerklärung, erreichbar unter `/datenschutz` |
| `404.html` | Seite für ungültige Adressen |
| `assets/style.css` | Gestaltung, inkl. Dunkelmodus |
| `assets/fonts/` | Schrift IBM Plex Sans, lokal eingebunden (Lizenz: SIL OFL) |
| `_redirects` | Leitet die alte IONOS-Adresse `/privacy18741a6b` auf `/datenschutz` um |
| `_headers` | Sicherheits-Header |
| `robots.txt`, `sitemap.xml` | Für Suchmaschinen |

## Veröffentlichen

1. **GitHub:** Neues Repository anlegen, z. B. `progresso-website`, Sichtbarkeit *Private*.
   Über *Add file → Upload files* den **Inhalt** dieses Ordners hochladen (nicht den Ordner selbst), inklusive `_headers`, `_redirects` und dem Ordner `assets`. Mit *Commit changes* abschließen.
2. **Cloudflare:** *Workers & Pages → Erstellen → Pages → Mit Git verbinden*.
   GitHub autorisieren (Zugriff nur auf dieses Repository genügt) und das Repository wählen.
   Build-Einstellungen: Framework *Keins*, Build-Befehl leer, Ausgabeverzeichnis leer bzw. `/`.
3. **Testen** unter der angezeigten Adresse `….pages.dev`.
4. **Domain verbinden:** Im Pages-Projekt unter *Benutzerdefinierte Domains* `www.progresso-consulting.com` und `progresso-consulting.com` hinzufügen. Voraussetzung: Die Domain läuft bereits über die Cloudflare-Nameserver.

## Ändern

Datei in GitHub bearbeiten und speichern (*Commit*). Cloudflare veröffentlicht die Änderung automatisch nach etwa einer Minute.

## Vor dem Livegang prüfen

- Impressum: Anschrift, Geschäftsführer und Telefonnummer
- Cloudflare: Auftragsverarbeitungsvertrag (Customer DPA) für das Konto
- Datenschutz, Abschnitt 4: Google Workspace erst erwähnen, wenn die Mail umgezogen ist
