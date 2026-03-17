# Naming Convention per Google Tag Manager: La guida definitiva (con Template)

**Keyword Target:** GTM Naming Conventions, Ottimizzazione Google Tag Manager, come organizzare GTM, analytics data governance.

---

Apri il tuo container di Google Tag Manager. Se trovi tag chiamati `click_pulsante_blu`, `test_marco_finale`, o `Facebook Pixel - Copia`, hai un problema. 
Un grosso problema che ti sta costando soldi.

Il tracciamento dei dati non è un lavoro per creativi disordinati. È ingegneria pura. E come ogni buon codice, richiede una sintassi rigorosa. In questo articolo ti spieghiamo perché la **Naming Convention** in GTM è vitale e ti regaliamo il framework esatto che usiamo in Ctrl Studio.

## Il costo del caos in GTM
Molte aziende sottovalutano l'importanza dei nomi dei tag, trigger e variabili, finché non succede uno di questi disastri:
1. **Doppie Conversioni:** Due agenzie diverse creano due tag per lo stesso form, gonfiando falsamente i report di Facebook Ads del 100%.
2. **Tag Orfani:** Il sito viene aggiornato, i vecchi tag smettono di funzionare, e nessuno sa a cosa servissero per poterli riparare.
3. **Onboarding Lento:** Un nuovo analista impiega 3 giorni solo per capire come è stato mappato il sito.

## Il Framework Ctrl Studio: La regola delle 3 componenti

Un buon nome in GTM deve rispondere a tre domande senza bisogno di aprire il tag:
1. *A chi sto mandando il dato?* (Piattaforma)
2. *Che tipo di azione è?* (Tipo Evento)
3. *Dove/Cosa è successo esattamente?* (Dettaglio Elemento)

La nostra struttura base è questa:
**[Piattaforma] - [Tipo Evento] - [Dettaglio]**

### 1. I Tag (Cosa invia il dato)
Usa sempre il nome ufficiale della piattaforma, seguito dall'azione standard.

*   ❌ Sbagliato: `FB acquisto ok`
*   ✅ Corretto: `Meta - Purchase - Checkout Completo`
*   ❌ Sbagliato: `GA4 form contatti`
*   ✅ Corretto: `GA4 - generate_lead - Form B2B Footer`
*   ❌ Sbagliato: `Linkedin insight tag`
*   ✅ Corretto: `LinkedIn - PageView - All Pages`

### 2. I Trigger (Quando si attiva il tag)
I trigger devono descrivere l'azione esatta dell'utente sul sito, indipendentemente dalla piattaforma a cui andranno i dati. Noi usiamo il formato: **[Tipo Azione] - [Condizione]**.

*   ❌ Sbagliato: `Scatta su ringraziamento`
*   ✅ Corretto: `Page View - /thank-you-page/`
*   ❌ Sbagliato: `Click bottone preventivo`
*   ✅ Corretto: `Click - Element - Button "Richiedi Preventivo"`
*   ❌ Sbagliato: `Form inviato`
*   ✅ Corretto: `Custom Event - hubspotFormSubmit - Success`

### 3. Le Variabili (Che dato raccolgo)
Le variabili sono i "contenitori" delle informazioni. Spesso si usano variabili predefinite, ma per quelle custom (Data Layer, JavaScript), è fondamentale indicarne il tipo.
Noi usiamo un prefisso per il tipo di variabile:
*   `DLV - e-commerce.value` (Data Layer Variable)
*   `CJS - Clean URL` (Custom JavaScript)
*   `C - Facebook Pixel ID` (Constant)

## Il Vantaggio delle Cartelle (Folders)
Oltre ai nomi, usa la funzione "Cartelle" di GTM per raggruppare tutto. Crea cartelle per:
*   `01 - Configurazione Base` (Pixel base, GA4 Config)
*   `02 - Eventi E-commerce` (Add to cart, Purchase)
*   `03 - Eventi Lead Gen` (Form submit, click email)
*   `04 - Variabili di Sistema`

## Scarica il Template
Sistemare un GTM incasinato è il primo passo per prendere decisioni basate su dati reali e non su supposizioni.

Abbiamo preparato un file Google Sheets con la nostra nomenclatura completa, pronto per essere copiato e incollato per il tuo prossimo audit.
**👉 [Scarica il Template GTM Naming Convention di Ctrl Studio qui]**
