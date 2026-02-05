# Analisi SEO - architettipalermo.com

## Stato attuale: Buona base, margini di miglioramento importanti

---

## COSA FUNZIONA BENE

### 1. Dominio Exact Match (EMD)
`architettipalermo.com` = match esatto per "architetti palermo". Vantaggio competitivo reale nella Local SEO.

### 2. Strategia Contenuti (40 articoli)
Copertura keyword long-tail locali molto ampia:
- Ristrutturazioni (bagno, cucina, appartamento, affitti brevi)
- Pratiche edilizie (CILA, SCIA, Permesso di Costruire)
- Servizi (interior design, rendering 3D, direzione lavori)
- Hospitality (B&B, Airbnb, hotel, casa vacanze)
- Costi e bonus (quanto costa architetto, superbonus, incentivi)

### 3. SEO On-Page Presente
- Title tag univoci e ottimizzati su ogni pagina
- Meta description 120-160 char su ogni pagina
- URL canonical assoluti corretti
- `<html lang="it">` corretto
- OpenGraph + Twitter Card su tutte le pagine
- Verifica Google Search Console + Bing Webmaster

### 4. Structured Data JSON-LD
Schema `Architect` con dati business (indirizzo, telefoni, email, area servita).

### 5. Performance
- Sito statico puro (GitHub Pages) → TTFB rapidissimo
- Zero framework JS (vanilla 9.7KB)
- CSS leggero (~18KB)
- Immagini: coppie JPG/WebP, `loading="lazy"`, `width/height` espliciti, `<picture>` sulla hero

### 6. Infrastruttura SEO
- `sitemap.xml` (47 URL con priority e lastmod)
- `robots.txt` con riferimento sitemap
- Favicon, apple-touch-icon, theme-color

### 7. Accessibilità
- Skip link, ARIA labels, focus trap, `prefers-reduced-motion`
- HTML semantico (header/nav/main/footer/article)

---

## COSA VA MIGLIORATO

### CRITICI (Impatto alto)

#### 1. Schema sbagliato sugli articoli blog
**Problema:** Tutti i 40 articoli usano `"@type": "Architect"` (identico alla homepage).
**Soluzione:** Usare `"@type": "BlogPosting"` con `datePublished`, `dateModified`, `author`, `headline`, `publisher`.
**Impatto:** Google può mostrare rich snippets (data, autore) nei risultati di ricerca.

#### 2. Nessun schema FAQPage
**Problema:** Articoli con sezioni FAQ non hanno markup `FAQPage`.
**Soluzione:** Aggiungere schema FAQPage dove ci sono domande/risposte.
**Impatto:** FAQ visibili direttamente nei risultati Google → CTR più alto.

#### 3. Manca og:image su 44/45 pagine
**Problema:** Solo la homepage ha `og:image`. Blog e sottopagine non hanno immagine social.
**Soluzione:** Aggiungere `og:image` con l'immagine hero di ogni pagina.
**Impatto:** Anteprime visive su Facebook, LinkedIn, WhatsApp quando condivisi.

#### 4. Nessun Google Analytics
**Problema:** Zero tracciamento. Impossibile sapere traffico, keyword, conversioni.
**Soluzione:** Installare GA4 con eventi per click WhatsApp e link Studio4E.
**Impatto:** Senza dati, non si possono ottimizzare le pagine che funzionano.

#### 5. Nessun schema BreadcrumbList
**Problema:** Assenti i breadcrumb strutturati.
**Soluzione:** Aggiungere `BreadcrumbList` con percorso Home → Blog → Articolo.
**Impatto:** Google mostra breadcrumb al posto dell'URL nei risultati.

### IMPORTANTI (Impatto medio)

#### 6. og:type sbagliato sui blog
**Problema:** Tutti gli articoli hanno `og:type = "website"` invece di `"article"`.
**Soluzione:** Cambiare a `og:type = "article"` su tutte le pagine blog.

#### 7. Campo "image" nello schema è un URL, non un'immagine
**Problema:** `"image": "https://www.studio4e.it/"` non è un file immagine.
**Soluzione:** Puntare a un'immagine reale (logo o foto studio).

#### 8. Date assenti
**Problema:** Nessun articolo mostra data pubblicazione (né visibile né nei meta). Le date nella sitemap sono tutte uguali.
**Soluzione:** Aggiungere date visibili e differenziare le date nella sitemap.

#### 9. Articoli troppo brevi
**Problema:** Alcuni articoli hanno ~400 parole. Per keyword competitive servono 1000-2000+.
**Soluzione:** Ampliare gradualmente gli articoli più strategici con contenuto originale.

#### 10. Nessun link interno tra articoli correlati
**Problema:** Gli articoli non si linkano tra loro.
**Soluzione:** Aggiungere sezione "Articoli correlati" e link contestuali nel testo.

#### 11. Gallery homepage senza `<picture>` e senza width/height
**Problema:** Le immagini gallery usano `<img src="...jpg">` senza WebP e senza dimensioni.
**Soluzione:** Usare `<picture>` con WebP e aggiungere width/height.

#### 12. Nessun Google Business Profile collegato
**Problema:** Il `sameAs` nello schema punta solo a pagine interne di studio4e.it.
**Soluzione:** Collegare Google Business Profile e aggiungere al sameAs.

### SECONDARI (Impatto basso)

#### 13. Inconsistenza numeri di telefono
WhatsApp usa +39 329..., lo schema riporta +39 347... (due numeri diversi). Può confondere Google.

#### 14. CSS inline vs external
Homepage ha stili inline, le altre pagine usano styles.css esterno. Doppia manutenzione.

#### 15. Manca feed RSS
Utile per aggregatori e distribuzione contenuti.

---

## PRIORITÀ DI INTERVENTO

| # | Intervento | Impatto | Difficoltà |
|---|-----------|---------|------------|
| 1 | Schema BlogPosting sugli articoli | **Alto** | Media |
| 2 | Schema FAQPage | **Alto** | Bassa |
| 3 | og:image su tutte le pagine | **Alto** | Bassa |
| 4 | Google Analytics 4 | **Alto** | Bassa |
| 5 | Schema BreadcrumbList | **Medio-Alto** | Bassa |
| 6 | og:type "article" sui blog | Medio | Bassa |
| 7 | Date pubblicazione | Medio | Bassa |
| 8 | Fix "image" nello schema | Medio | Bassa |
| 9 | Link interni tra articoli | Medio | Media |
| 10 | Ampliare contenuto articoli | Medio | Alta |
| 11 | Gallery con picture + dimensioni | Basso-Medio | Bassa |
| 12 | Google Business Profile | **Alto** (local) | Esterna |
