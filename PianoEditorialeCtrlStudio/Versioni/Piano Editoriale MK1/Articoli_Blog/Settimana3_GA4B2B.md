# GA4 per il B2B: Quali eventi tracciare se non vendi online

**Keyword Target:** GA4 Eventi Custom B2B, Google Analytics 4 lead generation, misurare conversioni B2B, setup GA4 per servizi.

---

Se hai un eCommerce, Google Analytics 4 (GA4) è relativamente facile da configurare: tracci gli "Aggiungi al Carrello" e gli "Acquisti", e vedi subito il fatturato.

Ma se sei un'azienda B2B che vende servizi complessi, macchinari o software Enterprise, non hai un carrello. La tua vendita avviene offline, dopo mesi di trattative. 
Se apri GA4 oggi, probabilmente vedi solo metriche inutili come "Visualizzazioni di Pagina" e "Tempo sul sito". Come fai a sapere se il tuo marketing sta funzionando?

La risposta è smettere di guardare le vanity metrics e iniziare a tracciare i **Micro-Eventi** e le **Conversioni di Qualità**. Ecco la guida definitiva agli eventi custom di GA4 per il B2B.

## Le Vanity Metrics (Cosa NON guardare)
Prima di aggiungere, devi togliere. Ignora questi dati di default:
- **Sessioni:** Avere 10.000 visite di studenti indiani non aiuta la tua azienda italiana di bulloni.
- **Scroll (Scroll Depth):** Sapere che qualcuno ha scrollato il 90% della pagina non significa che abbia letto o capito.

## Gli Eventi d'Oro per il B2B (Cosa tracciare davvero)

Nel B2B, il sito web ha uno scopo principale: generare Lead Qualificati e far avanzare l'utente nel funnel educativo. Ecco i 4 eventi che devi configurare (usando Google Tag Manager) e segnare come "Conversioni" in GA4.

### 1. Il Form Submit (Quello vero)
Sembra ovvio, ma l'80% delle aziende sbaglia. Non tracciare il "click sul bottone Invia". Se l'utente clicca ma ha dimenticato un campo obbligatorio, il form dà errore ma tu conti una conversione finta.
**Come tracciarlo:** Traccia l'apparizione del messaggio di successo (`success_message_view`) o l'atterraggio sulla Thank You Page (`page_view` su `/grazie`).
*Nome evento GA4 consigliato:* `generate_lead`

### 2. Il Click sulla Email (Mailto) e sul Telefono (Tel)
Nel B2B tradizionale, molti clienti preferiscono chiamare o scrivere una mail direttamente dal loro client di posta piuttosto che compilare un form. Se non tracci questi click, stai perdendo una fetta enorme del tuo ROI.
**Come tracciarlo:** Crea un trigger in GTM che scatta quando un utente clicca su un link che inizia per `mailto:` o `tel:`.
*Nome evento GA4 consigliato:* `click_email` e `click_phone`

### 3. Il Download di Materiale Tecnico (Whitepaper / Casi Studio)
I cicli di vendita B2B sono lunghi. Prima di contattare un commerciale, l'utente vuole capire se siete competenti. Scaricare una brochure tecnica, le specifiche di un macchinario o un caso studio è un fortissimo segnale di intento.
**Come tracciarlo:** Traccia il click sui link che finiscono in `.pdf`, `.doc`, o `.zip`. (GA4 lo fa in parte automaticamente con l'Enhanced Measurement, ma è meglio configurare un evento specifico per i file "Premium").
*Nome evento GA4 consigliato:* `file_download_premium`

### 4. La Visualizzazione Video Profonda (Demo / Webinar)
Se avete un video di 10 minuti che spiega come funziona il vostro software, sapere che qualcuno lo ha guardato fino alla fine vale molto di più di 100 visite alla homepage.
**Come tracciarlo:** Se usate YouTube o Vimeo integrati nel sito, configurate GTM per tracciare quando l'utente arriva al 75% o 90% della riproduzione.
*Nome evento GA4 consigliato:* `video_complete_demo`

## L'ultimo step: Trasforma gli eventi in "Conversioni"
Una volta che i dati entrano in GA4, vai nella sezione *Amministrazione > Conversioni* e segna l'evento `generate_lead` come Conversione.
In questo modo, potrai dire a Google Ads: "Portami persone simili a quelle che scatenano questo specifico evento".

## Conclusione
Un'installazione base di GA4 per un'azienda B2B è praticamente inutile. Devi insegnare alla macchina quali sono le azioni che per te hanno valore. 
In Ctrl Studio non ci fidiamo mai dei setup di default. Costruiamo architetture dati su misura per i processi di vendita complessi.

**👉 [Il tuo GA4 è un cimitero di numeri inutili? Chiedici un Audit della tua infrastruttura Analytics.]**
