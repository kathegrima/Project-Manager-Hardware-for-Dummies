# Gestione BOM e fornitori

> *"Una bugia è solo una bella storia che qualcuno rovina con la verità."* – Barney Stinson (How I Met Your Mother)

La BOM (Bill of Materials) e i fornitori sono il cuore pulsante di qualsiasi progetto hardware. Puoi raccontarti che il progetto andrà liscio, che i componenti saranno disponibili, che i costi resteranno nel budget. Poi arriva la verità: shortage, lead time infiniti, prezzi raddoppiati. La gestione di BOM e fornitori non è glamour ma è assolutamente critica per non affondare il progetto.

---

## Cos'è la BOM (Bill of Materials)

La BOM è l'elenco completo di tutti i componenti, materiali e sottoassiemi necessari per costruire il tuo prodotto. È molto più di una lista della spesa: è un documento tecnico, commerciale e operativo che accompagna il prodotto dall'ideazione alla produzione.

### Tipi di BOM

Non esiste una sola BOM ma diverse versioni che servono a scopi diversi:

**EBOM (Engineering BOM)** - La BOM di progettazione creata dagli ingegneri durante il design. Contiene tutti i componenti dal punto di vista tecnico: part number, valori, package, specifiche. È quella che esce dal CAD/EDA.

**MBOM (Manufacturing BOM)** - La BOM di produzione che include informazioni specifiche per il processo produttivo: sequenze di assemblaggio, istruzioni di processo, alternative di componenti, scarto previsto.

**SBOM (Service BOM)** - La BOM per la manutenzione e il servizio post-vendita. Include parti di ricambio, componenti sostituibili, istruzioni di riparazione.

Ogni tipo di BOM ha il suo pubblico e il suo scopo. Il PM deve assicurarsi che tutte siano allineate e aggiornate.

---

## Struttura di una BOM

Una BOM tipica contiene queste informazioni per ogni componente:

| Campo | Descrizione | Esempio |
|-------|-------------|---------|
| **Part Number** | Codice identificativo univoco del componente | STM32F103C8T6 |
| **Description** | Descrizione del componente | Microcontroller ARM Cortex-M3 |
| **Manufacturer** | Produttore del componente | STMicroelectronics |
| **Quantity** | Quantità per unità di prodotto | 1 |
| **Reference Designator** | Riferimento sullo schematic/PCB | U1 |
| **Package** | Tipo di package | LQFP48 |
| **Supplier** | Fornitore da cui si acquista | Digi-Key, Mouser, Farnell |
| **Supplier Part Number** | Codice del fornitore | 497-6063-ND |
| **Unit Price** | Prezzo unitario | €3.50 |
| **Lead Time** | Tempo di consegna | 8-12 settimane |
| **Notes** | Note aggiuntive | Disponibile versione industrial temp |

Più la BOM è dettagliata e accurata, meno problemi avrai in produzione.

---

## 💡 Concetto chiave

**La BOM non è statica.** Cambia durante il ciclo di vita del prodotto: si affina dopo i test, si aggiorna se cambiano fornitori, si modifica se componenti vanno in obsolescenza. Il PM deve gestire questo processo di change management con attenzione.

---

## Come creare e gestire una BOM efficace

### 1. Inizia presto e standardizza
Già in fase di concept dovresti avere una BOM preliminare per stimare costi e identificare componenti critici. Usa un template aziendale standard per tutti i progetti.

### 2. Usa part number ufficiali
Evita descrizioni generiche tipo "resistenza 10K". Usa part number precisi dei produttori per eliminare ambiguità e facilita gli ordini.

### 3. Verifica disponibilità e lead time
Prima di finalizzare il design, controlla che i componenti siano disponibili e quali siano i lead time reali. Un componente perfetto ma con 6 mesi di attesa è un problema.

### 4. Identifica componenti critici e alternative
Segnala componenti critici per prestazioni, costi o disponibilità. Per questi, identifica già in fase di design componenti alternativi compatibili.

### 5. Calcola costi realisticamente e versiona
Il costo della BOM deve considerare: quantità di acquisto, scarto (2-5%), gestione inventario, obsolescenza. Ogni modifica genera una nuova versione (v1.0, v1.1, v2.0) con tracciamento dei cambiamenti.

---

## 🎬 Momento Serie TV

> *"A noi la qualità c'ha rotto er cazzo!"* – René Ferretti (Boris)

Quando gestisci la BOM ti scontrerai con questo dilemma: componenti di qualità altissima che costano troppo e hanno lead time lunghi, oppure componenti più economici e disponibili ma con qualche compromesso. Il PM deve trovare il giusto equilibrio tra qualità, costi e fattibilità. Non sempre puoi avere il meglio del meglio, e va bene così se il compromesso è consapevole.

---

## Gestione fornitori

I fornitori sono i tuoi partner nella supply chain. Senza di loro, non hai componenti. Senza componenti, non hai prodotto.

### Tipi di fornitori

Esistono diverse tipologie di fornitori, ognuna con pro e contro: **distributori autorizzati** (Digi-Key, Mouser, Farnell) vendono componenti originali con garanzie ma prezzi più alti; **broker** sono utili per componenti in shortage o obsoleti ma richiedono più attenzione sulla qualità; **produttori diretti** offrono prezzi migliori per volumi alti ma con MOQ elevati e relazioni complesse; **produttori di PCB e assemblatori** che possono anche procurare componenti per tuo conto.

### Come selezionare i fornitori

Valuta i fornitori su questi criteri:

**Affidabilità** - Consegna nei tempi promessi? Buona reputazione? Verifica recensioni e referenze.

**Prezzo vs servizio** - Non scegliere solo il prezzo più basso. Un fornitore che costa il 5% in più ma consegna sempre in tempo vale molto di più.

**Lead time** - Da pochi giorni per componenti standard a mesi per componenti specifici o in shortage.

**MOQ (Minimum Order Quantity)** - Per prototipi in piccola quantità può essere un problema. Verifica sempre i MOQ.

**Supporto tecnico** - Un buon fornitore aiuta a trovare alternative, avvisa di obsolescenze, consiglia su disponibilità.

### RFQ (Request for Quotation)

Per ordini consistenti, fai RFQ formali mandando la BOM al fornitore con: lista componenti, quantità, date consegna, requisiti specifici. I fornitori rispondono con: prezzi per quantità, lead time, MOQ, termini di pagamento, validità preventivo. Confronta più RFQ considerando non solo il prezzo ma anche lead time, affidabilità e flessibilità.

---

## Lead time: il nemico silenzioso

Il lead time è il tempo tra l'ordine e la ricezione dei componenti. È uno dei vincoli più critici in hardware e viene spesso sottovalutato. Include: approvvigionamento componenti, produzione PCB (1-6 settimane), assemblaggio (giorni-settimane).

### Come gestire i lead time

**Pianifica in anticipo** - Se un componente ha 12 settimane di lead time, ordinalo 12 settimane prima. Sembra ovvio ma viene violato costantemente.

**Monitora costantemente** - I lead time cambiano. Un componente con 4 settimane di lead time può averne 16 se va in shortage.

**Usa forecast con fornitori** - Condividi previsioni di ordini futuri. Li aiuta a pianificare e può ridurre i lead time.

**Mantieni buffer di sicurezza** - Per componenti critici, considera buffer di scorta. Costa ma ti protegge da ritardi imprevisti.

---

## 🎬 Momento Serie TV

> *"Non sento l'Africa"* – Stanis La Rochelle (Boris)

I lead time richiedono pazienza. Non puoi forzarli con la forza di volontà. Quando Stanis aspetta di "sentire l'Africa" prima di recitare, sta facendo esattamente quello che deve fare il PM con i lead time: aspettare che le cose siano pronte, senza fretta inutile. Se un componente arriva tra 10 settimane, pianifica di conseguenza e usa quel tempo per fare altro.

---

## Component shortage e obsolescenza

Il mercato dei componenti elettronici è volatile. Shortage e obsolescenze sono eventi normali che devi saper gestire.

### Component shortage

Quando la domanda supera l'offerta: lead time si allungano, prezzi aumentano, disponibilità diventa limitata. Cause comuni: picchi di domanda (pandemia, mining crypto), problemi produttivi, disastri naturali, geopolitica.

**Come gestire gli shortage:**
- Monitora il mercato con Octopart, Findchips
- Ordina in anticipo quando vedi segnali di shortage
- Identifica alternative compatibili nella BOM
- Lavora con più fornitori per diversificare

### Obsolescenza

I produttori dichiarano componenti obsoleti (EOL - End of Life) regolarmente. Quando un componente va EOL: il produttore smette di produrlo, devi fare last time buy o trovare alternative, serve redesign se continui a produrre.

**Come gestire l'obsolescenza:**
- Scegli componenti mainstream con supporto lungo termine
- Monitora PCN (Product Change Notification) dai produttori
- Pianifica upgrade periodici per prodotti con vita lunga (5+ anni)

---

## 💡 Concetto chiave

**Supply chain management è risk management.** Ogni componente è un potenziale punto di fallimento. Il PM deve identificare i rischi, monitorarli e avere piani B pronti.

---

## Tool per la gestione BOM e fornitori

**Per BOM management:**
- **Arena PLM, Propel, PTC Windchill** - Piattaforme professionali (potenti ma costose)
- **Altium 365, Fusion 360 Manage** - Cloud-based, integrate con design tool
- **Excel/Google Sheets** - Per progetti piccoli, costa zero
- **PartsBox** - Dedicato elettronica, integrazione con distributori

**Per component sourcing:**
- **Octopart/Findchips** - Aggregatori per confrontare prezzi e disponibilità
- **Portali distributori** - Tool per caricare BOM e ottenere preventivi automatici

---

## Best practice

### Per la BOM

 **Mantieni una single source of truth** aggiornata e condivisa  
 **Versiona ogni modifica** e traccia i cambiamenti  
 **Calcola costi per fasce di volume** (100pz, 1K, 10K, 100K)  

 **Non usare componenti esotici** senza motivo valido  
 **Non ignorare i lead time** in fase di design  
 **Non fare single-source** per componenti critici  

### Per i fornitori

 **Costruisci relazioni a lungo termine** con fornitori fidati  
 **Comunica con trasparenza** condividendo forecast  
 **Diversifica** per non dipendere da un solo fornitore  

 **Non cambiare fornitore** solo per risparmiare il 2%  
 **Non ordinare all'ultimo minuto**  
 **Non ignorare le PCN** dei produttori  

---

## Esempio pratico: gestire uno shortage critico

**Scenario:** Il microcontroller del tuo dispositivo IoT va in shortage globale. Lead time passa da 4 a 26 settimane. Produzione prevista tra 8 settimane.

**Azioni del PM:**

1. **Valuta l'impatto** - Senza il componente, il progetto si ferma
2. **Cerca alternative immediate** - Modelli pin-compatible o altri produttori
3. **Contatta più fornitori** - Verifica stock residuo, considera broker
4. **Comunica agli stakeholder** - Avvisa subito management del rischio e delle azioni
5. **Aggiorna risk log** - Documenta problema e mitigazioni

La velocità di reazione e avere alternative pronte fa la differenza tra un ritardo di 2 settimane e uno di 6 mesi.

---

## 🧠 Cosa deve ricordare un PM

- La **BOM è un documento vivo**: va mantenuta aggiornata per tutta la vita del prodotto
- I **lead time sono vincoli fisici**: vanno pianificati, non ignorati
- **Shortage e obsolescenza** sono la norma, non l'eccezione
- Avere **componenti alternativi** identificati salva il progetto
- I **fornitori sono partner**: trattali bene e costruisci relazioni stabili
- **Diversificare** riduce il rischio: mai dipendere da un solo fornitore
- Monitora costantemente **disponibilità e prezzi**: il mercato cambia velocemente

---

**Prossimo capitolo**: [Risk Management e Change Control](./05-risk-management-e-change-control.md)
