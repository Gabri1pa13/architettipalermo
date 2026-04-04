# TASK 5 — SCHEMA MARKUP E TECHNICAL SEO: Implementazione Segnali Massimi

L'implementazione tecnica garantisce che Google comprenda perfettamente il contesto locale e professionale del sito, massimizzando le probabilità di apparire in rich snippet e AI Overview.

## 1. JSON-LD Strutturati (Esempi Core)

### Homepage: LocalBusiness & Organization
```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Architetti Palermo - Studio 4e",
  "image": "https://architettipalermo.it/assets/images/studio4e-logo.png",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Piazza Sant'Oliva 19",
    "addressLocality": "Palermo",
    "postalCode": "90141",
    "addressCountry": "IT"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 38.123,
    "longitude": 13.355
  },
  "url": "https://architettipalermo.it",
  "telephone": "+39091XXXXXX",
  "priceRange": "$$",
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
    "opens": "09:00",
    "closes": "18:00"
  }
}
```

### Articoli Pillar: Article & FAQPage
Ogni articolo deve contenere una sezione FAQ strutturata:
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "Quanto costa ristrutturare casa a Palermo?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "Il costo medio di ristrutturazione a Palermo nel 2025 varia tra 600€ e 1.200€ al mq, a seconda dei materiali e del tipo di intervento."
    }
  }]
}
```

## 2. Ottimizzazioni Tecniche Cruciali

-   **Core Web Vitals (Mobile First)**: Obiettivo LCP < 2.5s su reti 4G siciliane. Ottimizzazione delle immagini (WebP con fallback JPG) e Lazy Loading.
-   **Struttura URL**: Clean URLs (parlanti) in italiano, senza caratteri speciali o parametri inutili.
-   **Sitemap.xml**: Suddivisa per sezioni (Pagine, Guide, Zone, Glossario).
-   **Robots.txt**: Ottimizzato per favorire il crawling dei contenuti pillar ed escludere aree private o di test.
-   **Hreflang**: Non necessario se il sito è solo in italiano, ma consigliato per la versione inglese (Expats/Turisti) se implementata.
-   **Canonical**: Utilizzo rigoroso dei tag canonical per evitare duplicazione di contenuti tra pagine geografiche simili (es. /palermo-centro/ e /centro-storico-palermo/).

## 3. SEO Mobile e Local
-   **Click-to-Call**: Bottoni telefono ben visibili su mobile.
-   **Maps Integration**: Mappa interattiva Google Maps integrata nella pagina `/contatti/` e `/studio-di-riferimento/`.
-   **Internal Linking Geografico**: Link a pagine di zona (Livello 3) direttamente dal footer per massimizzare la scansione locale.

## 4. GEO (Generative Engine Optimization)
-   **Risposte Dirette**: Utilizzare paragrafi brevi (40-60 parole) all'inizio di ogni H2 per rispondere direttamente alle domande più frequenti.
-   **Dati Verificabili**: Inserire tabelle e grafici con dati numerici chiari per facilitare l'estrazione da parte delle AI (ChatGPT, Claude, Google SGE).
