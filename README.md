# Kontor

Marketing-Landingpage für **Kontor** – Warenwirtschaft für Handelsunternehmen,
gebaut mit [Hugo](https://gohugo.io/) + [Tailwind CSS](https://tailwindcss.com/).

## Lokal starten

```bash
npm install
npm run build:css   # einmalig, oder erneut nach Klassen-Änderungen in layouts/
hugo server
```

## Build

```bash
npm run build:css
hugo --minify
```

Das Deployment nach GitHub Pages läuft automatisch über
`.github/workflows/hugo-pages.yml` bei jedem Push auf `main` (Node-Build
für die CSS, dann Hugo-Build). Damit das greift, muss unter
*Settings → Pages* als Quelle **GitHub Actions** eingestellt sein.
Live-URL: https://dpb97.github.io/kontor-erp/

## Mehrsprachigkeit

Die Seite ist zweisprachig (DE Standard unter `/`, EN unter `/en/`).

- Kicker/Tagline/Description/Audience/FAQ: `hugo.toml`, je unter
  `[languages.de.params]` / `[languages.en.params]`
- Template-Texte (Nav, Section-Überschriften, Buttons): `i18n/de.toml` /
  `i18n/en.toml`, im Template per `{{ i18n "key" }}` bzw.
  `{{ i18n "key" (dict "Product" .Site.Params.product) }}` bei Platzhaltern
- Module & Referenz: `data/modules.yaml` / `data/references.yaml`, je mit
  `de:`/`en:`-Top-Level-Keys, im Template per
  `index .Site.Data.modules .Site.Language.Lang`
- Neue Startseite für eine weitere Sprache: `content/_index.<lang>.md`
  anlegen und in `hugo.toml` einen `[languages.<lang>]`-Block ergänzen

Impressum/Datenschutz existieren nur auf Deutsch (deutsche Rechtstexte);
der Footer verlinkt von der englischen Seite aus trotzdem dorthin, mit
Hinweis „(German only)“.
