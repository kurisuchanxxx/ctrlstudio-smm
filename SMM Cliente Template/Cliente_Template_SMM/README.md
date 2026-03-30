# Flusso di Gestione Social Media per [Nome Cliente]

Questa cartella contiene il flusso di lavoro completo per i social media di [Nome Cliente], progettato per l'uso con agenti TRAE e l'orchestrazione SOLO Coder.

## Struttura delle Cartelle

- `.trae/rules/brand_guidelines.md`: Contiene il tono del brand, lo stile, gli hashtag e le regole dell'identità visiva. Gli agenti caricheranno automaticamente questo contesto.
- `materiali/`: Inserisci qui brief del brand, loghi e materiali di riferimento.
- `piano_editoriale/`: Archivia qui i calendari editoriali settimanali o mensili e i documenti strategici.
- `post/`: Salva qui le bozze delle didascalie (txt o md).
- `immagini/`: Archivia qui gli asset visivi o i placeholder delle immagini.
- `programmazione/`: Tieni traccia qui degli slot di pubblicazione e dei metadati.
- `report/`: Archivia qui i riepiloghi analitici e i report sulle prestazioni.
- `archivio/`: Sposta qui i post pubblicati o vecchi.

## Istruzioni per l'Uso

1.  **Apri sempre direttamente questa cartella** quando lavori su questo brand per garantire l'isolamento del contesto.
2.  **Non riutilizzare le chat** tra brand diversi per evitare la contaminazione del contesto.
3.  **Aggiorna `brand_guidelines.md`** immediatamente con i dettagli specifici per questo cliente.
4.  Usa la cartella `materiali/` per fornire il contesto iniziale agli agenti.

## Agenti

Questa struttura supporta i seguenti agenti globali:
- `content-planner`: Per creare calendari editoriali.
- `copywriter`: Per redigere didascalie e post.
- `design-assistant`: Per creare asset visivi.
- `scheduler`: Per pianificare la programmazione.
- `publisher`: Per pubblicare i contenuti.
- `community-manager`: Per interagire con il pubblico.
- `analytics-reporter`: Per generare report sulle prestazioni.

## Per Iniziare

1.  Compila il file `brand_guidelines.md`.
2.  Aggiungi eventuali asset del brand esistenti in `materiali/`.
3.  Avvia una nuova chat e chiedi al `content-planner` di generare un calendario editoriale.
