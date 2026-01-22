# architettipalermo.com (GitHub Pages)

Sito statico vetrina + blog (40 pagine) per SEO locale (Palermo/Sicilia).

## Struttura
- `index.html` home
- `servizi.html` servizi
- `blog.html` indice blog con ricerca
- `blog/*.html` 40 articoli
- `contatti.html` contatti
- `assets/` css, js, immagini
- `sitemap.xml`, `robots.txt`
- `CNAME` per dominio custom

## Come pubblicare su GitHub Pages
1. Crea repo (es. `architettipalermo.com`)
2. Carica questi file nella root del repo
3. Settings → Pages → Deploy from branch → `main` / root
4. Collega il dominio: `architettipalermo.com` (già presente `CNAME`)

### DNS (riassunto)
Nel pannello del tuo provider DNS:
- A record verso GitHub Pages (4 IP standard GitHub Pages)
- CNAME `www` → `<tuo-username>.github.io`

> Nota: gli IP GitHub possono cambiare nel tempo: usa la doc ufficiale GitHub Pages per verificare.

## Foto
Metti le foto in `assets/images/` e rinomina la principale in `hero.jpg`.
