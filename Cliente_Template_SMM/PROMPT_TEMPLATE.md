Imposta una struttura completa di cartelle di progetto per gestire il flusso di lavoro dei social media di un singolo brand cliente utilizzando agenti TRAE condivisi. (che riutilizzerò ogni volta per un nuovo progetto, quindi salvami anche questo prompt in formato .md

La struttura deve:

- Mantenere il contesto e la memoria isolati dagli altri clienti
- Supportare il riutilizzo di agenti globali come: content-planner, copywriter, design-assistant, scheduler, publisher, community-manager, analytics-reporter
- Essere compatibile con l'orchestrazione usando SOLO Coder o altri agenti di flusso di lavoro

🔧 Struttura delle Cartelle:
- Nome cartella radice: usa `Cliente_[nomecliente]_SMM`
- All'interno della cartella, crea:
  - `.trae/rules/brand_guidelines.md`: un file markdown contenente tono, voce, stile, hashtag, regole di identità visiva del brand
  - `materiali/`: per brief del brand, loghi, riferimenti
  - `piano_editoriale/`: per calendari settimanali o mensili e file di strategia
  - `post/`: per bozze di didascalie (txt o md)
  - `immagini/`: per asset visivi o placeholder di immagini
  - `programmazione/`: per slot di pubblicazione e metadati
  - `report/`: riepiloghi analitici
  - `archivio/`: post pubblicati o vecchi
  - `README.md`: breve documento di utilizzo che spiega come usare lo spazio di lavoro

🧠 Configurazione aggiuntiva:
- Aggiungi testo segnaposto all'interno di `brand_guidelines.md` per guidare l'utente (es. "Descrivi tono di voce, pubblico, esempi di hashtag, posizionamento logo...")
- Aggiungi un README con istruzioni come:
  - Apri sempre questa cartella quando lavori su questo brand
  - Non riutilizzare mai le chat tra i brand
  - Gli agenti caricheranno automaticamente le regole del brand in questa cartella come contesto persistente

📌 Obiettivo:
Rendere questa cartella plug-and-play per i flussi di lavoro AI dei social media. Deve essere pronta per la pianificazione orchestrata, la scrittura di didascalie, il design visivo, la programmazione, la pubblicazione, la reportistica e le attività della community — tutto isolato per ogni brand cliente.
