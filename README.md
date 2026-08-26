# Kontor

Marketing-Landingpage für **Kontor** – Warenwirtschaft für Handelsunternehmen,
gebaut mit [Hugo](https://gohugo.io/) + [Tailwind CSS](https://tailwindcss.com/) + [daisyUI](https://daisyui.com/).

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
