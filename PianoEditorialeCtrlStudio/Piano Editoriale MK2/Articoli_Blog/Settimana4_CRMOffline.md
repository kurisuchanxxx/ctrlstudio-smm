# Perché il tuo CRM dice "Traffico Diretto": Come unificare i dati tra Google Ads e HubSpot

**Keyword Target:** Integrazione CRM e Google Ads, Tracciare Lead Offline, Offline Conversion Tracking (OCT), HubSpot Google Ads integration, Dark Social.

---

Apri il tuo CRM aziendale (HubSpot, Salesforce, Pipedrive). Vai sulla dashboard delle fonti di acquisizione.
Se la fetta più grande del grafico a torta si chiama **"Traffico Diretto"** o **"Origine Sconosciuta"**, stai guardando un'illusione. E probabilmente stai tagliando il budget alle campagne sbagliate.

Nel B2B, il percorso di acquisto non è lineare. Un lead non clicca su un annuncio Google e compra subito un software da 10.000€. Ne parla su Slack (Dark Social), torna sul sito due settimane dopo digitando l'URL a mano, e compila il form.
Per il CRM, quello è "Traffico Diretto". Per la realtà, è una conversione generata da Google Ads.

In questo articolo vediamo come risolvere il problema dell'attribuzione implementando l'**Offline Conversion Tracking (OCT)** tra Google Ads e il tuo CRM.

## Il problema del "Lead Qualificato"
Il tracciamento standard (Pixel) si ferma al "Form Inviato".
Google Ads vede che 10 persone hanno compilato il form e pensa di aver fatto un ottimo lavoro. Ma tu sai che 8 di quei lead cercavano un lavoro o volevano venderti qualcosa, e solo 2 erano vere aziende in target.

Se ottimizzi le campagne sui "Form Inviati", l'algoritmo di Google ti porterà sempre più spam. Devi dire a Google cosa succede *dopo* il form, dentro le mura della tua azienda.

## La Soluzione: L'Offline Conversion Tracking (OCT)

L'OCT è una tecnica che permette al tuo CRM di "parlare" con Google Ads in differita.
Invece di dire a Google "Ehi, qualcuno ha compilato un form", il tuo CRM dirà a Google, tre giorni dopo: "Ehi, ricordi quel tizio che ha cliccato l'annuncio martedì? Ha appena firmato un contratto da 5.000€".

### Come funziona l'architettura OCT:

**Passo 1: Catturare il GCLID (Google Click ID)**
Quando un utente clicca su un tuo annuncio Google, Google aggiunge un parametro all'URL chiamato `gclid` (es. `tuosito.com/?gclid=12345abc`).
Devi usare uno script sul tuo sito per leggere questo GCLID e salvarlo in un cookie o nel Local Storage.

**Passo 2: Inviare il GCLID al CRM (Campi Nascosti)**
Quando l'utente compila il form contatti, il GCLID salvato deve essere inserito in un "Campo Nascosto" (Hidden Field) del form. 
In questo modo, il lead entra in HubSpot portandosi dietro il suo "scontrino identificativo" di Google Ads.

**Passo 3: Il cambio di stato nel CRM**
Il team vendite lavora il lead. Lo chiama, fa la demo. Dopo una settimana, il lead viene spostato nello stage "Contratto Chiuso Vinto" (Closed Won) dentro HubSpot.

**Passo 4: Il Webhook (Il ritorno dei dati)**
Qui avviene la magia. Quando lo stato cambia in "Chiuso Vinto", HubSpot fa scattare un'automazione (tramite integrazione nativa o tool come Zapier/Make).
Invia un pacchetto dati a Google Ads contenente:
- Il famoso `GCLID`.
- Il nome della conversione ("Acquisto Offline").
- Il valore economico reale (es. 5.000€).

### Il Risultato per il tuo Marketing
Ora l'algoritmo di Google Ads sa esattamente quali parole chiave e quali annunci portano clienti altospendenti, e non semplici compilatori di form seriali.

*   **Bidding basato sul ROAS:** Puoi dire a Google di massimizzare il valore delle conversioni, non il numero di click.
*   **Report Veritieri:** Il "Traffico Diretto" nel CRM si sgonfia, e finalmente vedi il vero ROI delle tue campagne a pagamento.

Smetti di ottimizzare le tue campagne per i Lead Spazzatura. Se vuoi collegare il tuo CRM alle tue campagne Ads, prenota una call con i nostri ingegneri dei dati.

**👉 [Vuoi sapere come implementare l'OCT sul tuo CRM specifico? Leggi la nostra documentazione tecnica o richiedi un audit.]**
