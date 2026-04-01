# Come configurare le Conversion API di Meta per aggirare i blocchi di iOS (Schema Architetturale)

**Keyword Target:** Facebook Conversion API setup, Bypassare blocchi iOS 14 Tracking, Meta CAPI GTM Server-side, tracciamento Facebook Ads.

---

Se fai advertising su Facebook o Instagram, l'aggiornamento iOS 14.5 di Apple è stato il momento in cui le tue dashboard hanno iniziato a mentire.
Da un giorno all'altro, Meta ha perso visibilità su una fetta enorme di utenti (quelli che hanno cliccato "Chiedi all'app di non tracciare"). 

Il vecchio Pixel di Facebook, basato sul browser, non basta più. La soluzione tecnica, spinta da Meta stessa, si chiama **Conversion API (CAPI)**. In questo articolo tecnico, ti mostriamo l'architettura esatta che usiamo in Ctrl Studio per ripristinare il flusso dei dati.

## Cos'è la Meta Conversion API?
A differenza del Pixel che manda i dati dal *browser* dell'utente a Facebook (Client-Side), la Conversion API manda i dati dal *tuo server* ai server di Meta (Server-to-Server).

Poiché la comunicazione avviene nel backend, non può essere bloccata dagli AdBlocker o dalle restrizioni di Safari (ITP - Intelligent Tracking Prevention). 

### L'Architettura Ideale: Il Doppio Tracciamento (Deduplicazione)
La best practice non è eliminare il Pixel, ma far lavorare Pixel e CAPI insieme. Meta riceverà lo stesso evento due volte (una dal browser, una dal server) e userà un ID univoco (`Event ID`) per scartare il doppione. Se il browser è bloccato, il server "salva" la conversione.

## Schema Architetturale: Come costruiamo l'infrastruttura

Ecco i componenti necessari per il setup avanzato:

1.  **Il Data Layer (Sul Sito Web):** Il tuo sito (es. Shopify o custom) deve esporre i dati strutturati (es. valore acquisto, email criptata dell'utente) a livello di codice.
2.  **Google Tag Manager (Web Container):** Raccoglie i dati dal Data Layer e, invece di mandarli a Facebook, li manda al tuo Server Container GTM.
3.  **Il Server Cloud (GCP o AWS):** È l'ambiente di hosting dove risiede il tuo GTM Server. Gira su un sottodominio del tuo sito (es. `data.tuosito.com`).
4.  **Google Tag Manager (Server Container):** Riceve i dati dal Web Container, li "pulisce" (es. esegue l'hashing SHA-256 delle email) e li impacchetta per le API di Meta.
5.  **Meta Graph API:** Riceve il payload finale e lo abbina all'utente per ottimizzare l'algoritmo pubblicitario.

## I Passaggi Critici (Dove tutti sbagliano)

### 1. La Deduplicazione (Event ID)
Se non invii lo stesso identico `Event ID` e `Event Name` sia dal Pixel web che dal Server, Meta conterà le conversioni doppie, rovinando il ROAS. Assicurati che l'ID sia generato nel browser e passato al server.

### 2. L'Event Match Quality (EMQ)
Non basta mandare un evento "Acquisto" vuoto. Per far capire a Meta chi ha comprato, devi inviare i "Customer Information Parameters" (Email, Telefono, Nome, CAP, IP Address, User Agent).
*Attenzione:* Questi dati **devono** essere criptati (SHA-256) prima di essere inviati. Il Server-side ti permette di fare questo hashing in ambiente sicuro.

### 3. Il First-Party Cookie (fbp e fbc)
Il tuo server GTM deve essere configurato sullo stesso dominio principale del tuo sito (es. `tracking.azienda.it`). Solo così può generare e leggere i cookie `_fbp` e `_fbc` come cookie "di prima parte", essenziali per l'attribuzione della campagna.

## Vale la pena farlo?
Implementare un'architettura Server-Side per le Conversion API richiede un setup tecnico e costi di server mensili (da 30€ a 150€ a seconda del traffico). 
Tuttavia, se investi più di 1.000€/mese in Ads, recuperare il 20% di conversioni "perse" migliora l'algoritmo al punto da ripagare l'infrastruttura in pochi giorni.

**👉 [L'architettura ti sembra complessa? Scarica il nostro Diagramma Blueprint ad alta risoluzione o contattaci per un setup chiavi in mano.]**
