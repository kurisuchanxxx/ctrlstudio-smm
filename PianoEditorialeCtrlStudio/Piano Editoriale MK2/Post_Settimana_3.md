# LinkedIn Post Drafts - Settimana 3 (Customer Discovery & Trasparenza)

## Post 1: Teardowns
**Pillar:** Teardowns & Fixes (Analisi Pratica)
**Framework:** Steve Blank (L'Illusione vs La Realtà)
**Format:** Text-only (Con formattazione pulita e paragrafi brevi)
**Hook:** "Il 90% dei siti B2B viene progettato basandosi su quello che l'azienda pensa di sé stessa."

**Copy:**
Il 90% dei siti web B2B viene progettato basandosi su quello che l'azienda pensa di sé stessa. Nessuno chiede ai clienti cosa stanno cercando.

Funziona così:
Passate mesi in sala riunioni a litigare su un pantone blu.
Scegliete foto stock di gente sorridente che si stringe la mano.
Scrivete come titolo: "Siamo leader di settore con soluzioni sinergiche a 360 gradi".

Poi lo mettete online.
E scoprite che i clienti reali, quelli che strisciano la carta di credito, cercano solo una cosa: "Quanto mi costa, quanto tempo ci vuole e quali problemi mi risolve?"

In Ctrl Studio abbiamo una regola: non iniziamo a disegnare un singolo pixel finché non abbiamo fatto Discovery.
- Analizziamo le registrazioni delle call commerciali.
- Leggiamo i ticket di supporto clienti.
- Scopriamo quali sono le obiezioni VERE e i dubbi irrisolti.

Nessun restyling grafico, per quanto bello, sopravvive al primo vero lead qualificato se non risponde alle sue domande.

L'ultima volta che avete rifatto il sito o una landing page, quante interviste ai vostri clienti avete letto o ascoltato prima di iniziare?

#customerdiscovery #uxdesign #b2b #ctrlstudio #cro

---

## Post 2: Building Ctrl
**Pillar:** Building Ctrl Studio (Trasparenza)
**Framework:** PostHog (The Honest Post-Mortem)
**Format:** Meme (es. "This is fine" con il cane tra le fiamme) o Screenshot di un avviso di errore critico su Slack.
**Hook:** "La settimana scorsa abbiamo inavvertitamente bloccato il tracciamento di un cliente per 2 ore."

**Copy:**
La settimana scorsa abbiamo inavvertitamente bloccato il tracciamento di un nostro cliente per 2 ore.
Ecco cosa è successo (e come abbiamo risolto).

Un aggiornamento imprevisto di un plugin per i cookie di terze parti ha fatto saltare il nostro container server-side. Tutti gli eventi di conversione: zero. Morti.
Panico in ufficio? Un po'.

Ma in Ctrl Studio non crediamo nell'infrastruttura perfetta (perché si rompe tutto, sempre). Crediamo nell'infrastruttura resiliente.

Avevamo impostato degli alert automatici su Slack tramite un webhook personalizzato per i cali di traffico anomali sui tag chiave.
L'alert è scattato. Il team tecnico è intervenuto, ha isolato il problema bypassando il plugin colpevole e ha fatto il rollback della versione GTM.
Tempo di down effettivo: 12 minuti da quando ce ne siamo accorti.

Nessuno è immune ai bug. La differenza la fa il tempo di reazione.

Quanto tempo ci mettereste voi (o la vostra agenzia) ad accorgervi se il vostro tracciamento delle conversioni smettesse di funzionare *esattamente in questo momento*?

#buildinpublic #engineering #tracking #failforward #ctrlstudio

---

## Post 3: The Anti-Agency
**Pillar:** The Anti-Agency (Verità Scomode)
**Framework:** Alex Hormozi (The Value Reversal)
**Format:** Immagine di un diagramma complesso (es. schema di tracciamento Server-Side in Mermaid o Miro) in alta risoluzione.
**Hook:** "Perché regaliamo i nostri Template GTM migliori?"

**Copy:**
Molti colleghi del settore ci dicono: "Ma siete pazzi? Se date via pubblicamente i vostri setup tecnici e le architetture, poi i clienti non vi assumono per farli".

Sbagliato.

Il valore di un'agenzia tecnica oggi non è nel "sapere cosa fare". L'informazione pura è diventata una commodity: è gratis ovunque, su YouTube o chiedendo a ChatGPT.

Il vero valore è nel *non avere il tempo, le competenze interne o la voglia di implementarlo da soli senza rompere tutto*.

Più dimostriamo pubblicamente che il nostro metodo funziona regalandone i blueprint, più si alza la percezione del nostro valore per l'esecuzione. Dai via l'informazione, vendi l'implementazione senza sbattimenti.

Qui sotto vi lascio il nostro schema esatto per impostare le Conversion API di Meta aggirando i blocchi iOS. È complesso, ma funziona al 100%.

Scaricatelo, studiatelo, usatelo.
E se vi viene mal di testa solo a guardarlo, sapete a chi mandare un messaggio. 😉

#marketingagency #value #b2b #servertracking #ctrlstudio
