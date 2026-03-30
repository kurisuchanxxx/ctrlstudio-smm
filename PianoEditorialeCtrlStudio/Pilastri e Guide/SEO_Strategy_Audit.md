# SEO Audit: Ctrl Studio (www.ctrlstudio.it)

**Stato Attuale:** Il sito è bloccato da Cloudflare per le richieste automatiche (bot protection), il che è ottimo per la sicurezza ma impedisce un audit tecnico profondo dall'esterno senza accesso.
Tuttavia, analizzando la struttura visibile e l'indicizzazione su Google, ecco i punti chiave su cui lavorare per il Blog.

## 1. Struttura Attuale (One-Page vs Blog)
Attualmente Google vede principalmente la Homepage e poche pagine di servizio.
Il sito sembra strutturato molto come una **Landing Page unica** (ottima per conversione immediata, pessima per SEO organica su keyword diverse).

**Problema:** Se cerco "Consulenza Marketing Ancona" o "Tracking Server-Side", oggi atterro sempre sulla home (o non atterro affatto).
**Soluzione:** Serve verticalizzare. Il Blog non deve essere un "diario", ma una raccolta di Landing Page editoriali.

## 2. Strategia Blog "Hub & Spoke"

Per posizionarci come "Ingegneri del Marketing", dobbiamo coprire 3 cluster semantici principali (che corrispondono ai nostri pillar):

### Cluster A: Infrastruttura & Tracking (Keyword Tecniche)
*Target:* Marketing Manager, CTO, Founder tecnici.
*   **Articolo Pillar:** "La Guida Definitiva al Server-Side Tracking per il 2026".
*   **Articoli Spoke (da linkare):**
    *   "GA4 vs Universal Analytics: Cosa cambia per il B2B".
    *   "Perché il Pixel di Meta sta morendo (e cosa usare invece)".
    *   "Cookie Law e Tracking: Come non perdere dati legalmente".

### Cluster B: Strategia & Conversioni (Keyword "Pain Point")
*Target:* CEO, Imprenditori che non vedono risultati.
*   **Articolo Pillar:** "Perché il tuo sito ha traffico ma non converte (Audit CRO)".
*   **Articoli Spoke:**
    *   "Guest Checkout vs Registrazione: Il caso E-commerce".
    *   "Come progettare una Thank You Page che vende ancora".
    *   "Form Contatti: 3 errori che ti costano il 50% dei lead".

### Cluster C: Anti-Agency (Keyword "Opinion/Trend")
*Target:* Chi cerca partner seri, non fornitori.
*   **Articolo Pillar:** "Smetti di cercare un Social Media Manager (Cerca un Sistema)".
*   **Articoli Spoke:**
    *   "Linktree è il male: Riporta il traffico a casa".
    *   "Vanity Metrics: Perché i Like non pagano le bollette".

## 3. Checklist Tecnica per il Blog (Webflow/WordPress)
Visto che usate Webflow (dal blocco Cloudflare "cdn.webflow.com" lo deduco):

1.  **URL Structure:** Usa `/blog/titolo-post` pulito. Niente date (`/2026/03/...`).
2.  **H1/H2:** Assicurati che ogni articolo abbia UN solo H1 (il titolo) e H2 per i sottotitoli.
3.  **Schema Markup:** Webflow non lo mette in automatico bene. Bisogna iniettare lo script JSON-LD `Article` o `BlogPosting` nell'head di ogni post. (Skill `schema-markup` serve a questo).
4.  **Internal Linking:** Ogni articolo deve linkare almeno a:
    *   La pagina "Contatti" o "Servizi" (CTA).
    *   Un altro articolo correlato (Retention).

## 4. Prossimi Passi Operativi

1.  **Scegliere il CMS per il Blog:** Se siete su Webflow, usate il CMS di Webflow. È potente per la SEO se settato bene.
2.  **Piano Editoriale Blog:** Abbiamo già definito i primi 4 titoli nel file `Blog_SEO_Integration.md`.
3.  **Scrittura:** Iniziare a scrivere il primo articolo ("Server-side Tracking").

Vuoi che abbozzi la struttura (H1, H2, H3) del primo articolo del blog per vedere come verrebbe?
