# Kontor

Marketing-Landingpage für **Kontor** – Warenwirtschaft für Handelsunternehmen,
gebaut mit [Hugo](https://gohugo.io/).

## Lokal starten

```bash
hugo server
```

## Build

```bash
hugo --minify
```

Das Deployment nach GitHub Pages läuft automatisch über
`.github/workflows/hugo-pages.yml` bei jedem Push auf `main`. Damit das
greift, muss unter *Settings → Pages* als Quelle **GitHub Actions**
eingestellt sein. Live-URL: https://dpb97.github.io/kontor-erp/
