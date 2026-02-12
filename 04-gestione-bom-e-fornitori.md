# Gestione BOM e fornitori

> *"Una bugia è solo una bella storia che qualcuno rovina con la verità."* – Barney Stinson (How I Met Your Mother)

La BOM (Bill of Materials) e i fornitori sono il cuore pulsante di qualsiasi progetto hardware; puoi raccontarti che il progetto andrà liscio, che i componenti saranno disponibili, che i costi resteranno nel budget. Poi arriva la verità: shortage, lead time infiniti, prezzi raddoppiati. La gestione di BOM e fornitori non è glamour ma è assolutamente critica per non affondare il progetto.

---

## Cos'è la BOM (Bill of Materials)

La BOM è l'elenco completo di tutti i componenti materiali e sottoassiemi necessari per costruire il tuo prodotto. È molto più di una lista della spesa: è un documento tecnico, commerciale e operativo che accompagna il prodotto dall'ideazione alla produzione.

### Tipi di BOM

Non esiste una sola BOM ma diverse versioni che servono a scopi diversi:

**EBOM (Engineering BOM)**
La BOM di progettazione creata dagli ingegneri durante il design. Contiene tutti i componenti dal punto di vista tecnico: part number, valori, package, specifiche. È la BOM che esce dal CAD/EDA e che viene usata per ordinare i prototipi.

**MBOM (Manufacturing BOM)**
La BOM di produzione che include informazioni specifiche per il processo produttivo: sequenze di assemblaggio, istruzioni di processo, alternative di componenti, scarto previsto. È quella che usa la fabbrica per produrre.

**SBOM (Service BOM)**
La BOM per la manutenzione e il servizio post-vendita. Include parti di ricambio, componenti sostituibili, istruzioni di riparazione.

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
| **Notes** | Note aggiuntive | Disponibile anche versione industrial temp |

Più la BOM è dettagliata e accurata, meno problemi avrai in produzione.
(Ricordati solo di aggiornarla e non di lasciarla morire su un file, ci resta male)

---

## 💡 Concetto chiave

**La BOM non è statica.** Cambia durante il ciclo di vita del prodotto: si affina dopo i test, si aggiorna se cambiano fornitori, si modifica se componenti vanno in obsolescenza. Il PM deve gestire questo processo di change management con attenzione.

---

## Come creare e gestire una BOM efficace

### 1. Inizia presto
Non aspettare la fine del design per pensare alla BOM. Già in fase di concept dovresti avere una BOM preliminare per stimare costi e identificare componenti critici.

### 2. Standardizza il formato
Usa un template condiviso e consistente. Se ogni progetto ha una BOM diversa, diventa un casino gestirle. Meglio avere un formato aziendale standard.

### 3. Usa part number ufficiali
Evita descrizioni generiche tipo "resistenza 10K". Usa part number precisi dei produttori. Questo elimina ambiguità e facilita gli ordini.

### 4. Verifica disponibilità e lead time
Prima di finalizzare il design, verifica che i componenti siano disponibili e quali siano i lead time. Un componente perfetto ma con 6 mesi di attesa è un problema.

### 5. Identifica componenti critici
Alcuni componenti sono critici per prestazioni, costi o disponibilità. Segnalali nella BOM e monitora la loro supply chain con particolare attenzione.

### 6. Prevedi alternative
Per componenti critici o ad alto rischio di shortage, identifica già in fase di design componenti alternativi compatibili. Questo ti salva quando il componente principale non è disponibile.

### 7. Calcola i costi realisticamente
Il costo della BOM non è la somma dei prezzi unitari. Devi considerare:
- Quantità di acquisto (più compri, meno paghi)
- Scarto di produzione (tipicamente 2-5%)
- Costi di gestione inventario
- Costi di obsolescenza

### 8. Versiona la BOM
Ogni modifica genera una nuova versione. Usa un sistema di versionamento chiaro (es. v1.0, v1.1, v2.0) e traccia cosa è cambiato tra versioni.

---

## 🎬 Momento Serie TV

> *"A noi la qualità c'ha rotto er cazzo!"* – René Ferretti (Boris)

Quando gestisci la BOM ti scontrerai con questo dilemma: componenti di qualità altissima che costano troppo e hanno lead time lunghi, oppure componenti più economici e disponibili ma con qualche compromesso. Il PM deve trovare il giusto equilibrio tra qualità, costi e fattibilità. Non sempre puoi avere il meglio del meglio, e va bene così se il compromesso è consapevole.

---

## Gestione fornitori

I fornitori sono i tuoi partner nella supply chain. Senza di loro, non hai componenti. Senza componenti, non hai prodotto. La relazione con i fornitori va gestita in modo professionale e strategico.

### Tipi di fornitori

**Distributori autorizzati**
Vendono componenti originali direttamente dai produttori. Sono affidabili, offrono garanzie ma i prezzi possono essere più alti. Esempi: Digi-Key, Mouser, Farnell, RS Components, Arrow.

**Broker**
Comprano e rivendono componenti sul mercato aperto. Utili per trovare componenti in shortage o obsoleti ma richiedono più attenzione sulla qualità e autenticità.

**Produttori diretti**
Per volumi alti, puoi trattare direttamente con i produttori di componenti. Ottieni prezzi migliori ma devi gestire MOQ (Minimum Order Quantity) alti e relazioni più complesse.

**Produttori di PCB e assemblatori**
Fornitori che producono i PCB e/o fanno l'assemblaggio. Possono anche procurare componenti per tuo conto.

### Come selezionare i fornitori

**1. Affidabilità**
Il fornitore consegna nei tempi promessi? Ha una buona reputazione? Verifica recensioni, chiedi referenze, parti con ordini piccoli per testare.

**2. Prezzo**
Confronta prezzi tra più fornitori ma non scegliere solo in base al prezzo più basso. Un fornitore che costa il 5% in più ma consegna sempre in tempo vale più di uno che costa meno ma ti fa slittare il progetto.

**3. Lead time**
Quanto tempo ci vuole per ricevere i componenti? I lead time variano enormemente: da pochi giorni per componenti standard a mesi per componenti specifici o in shortage.

**4. MOQ (Minimum Order Quantity)**
Alcuni fornitori richiedono quantità minime d'ordine. Per prototipi in piccola quantità può essere un problema. Verifica sempre i MOQ prima di scegliere un componente.

**5. Supporto tecnico**
Un buon fornitore offre supporto: ti aiuta a trovare alternative, ti avvisa di obsolescenze, ti consiglia su disponibilità. Questo vale molto.

### RFQ (Request for Quotation)

Per ordini consistenti o rapporti stabili, fai RFQ formali: mandi la BOM al fornitore e chiedi un preventivo dettagliato. L'RFQ include:
- Lista completa dei componenti con part number
- Quantità richieste
- Date di consegna desiderate
- Eventuali requisiti specifici (certificazioni, packaging, ecc.)

I fornitori rispondono con:
- Prezzi per quantità
- Lead time
- MOQ
- Termini di pagamento
- Validità del preventivo

Confronta più RFQ prima di decidere. Non basarti solo sul prezzo totale: guarda anche lead time, affidabilità, flessibilità del fornitore.

---

## Lead time: il nemico silenzioso

Il lead time è il tempo che passa tra l'ordine e la ricezione dei componenti. È uno dei vincoli più critici in hardware e viene spesso sottovalutato.

### Tipologie di lead time

**Lead time di approvvigionamento**
Tempo dal momento dell'ordine alla consegna del componente al tuo magazzino o alla fabbrica.

**Lead time di produzione PCB**
Tempo per produrre i PCB: tipicamente 1-3 settimane per prototipi, può arrivare a 4-6 settimane per produzioni complesse o multilayer.

**Lead time di assemblaggio**
Tempo per assemblare i componenti sui PCB: da pochi giorni per piccoli lotti a settimane per produzioni grandi.

### Come gestire i lead time

**1. Pianifica in anticipo**
Non ordinare componenti all'ultimo minuto. Se un componente ha 12 settimane di lead time, devi ordinarlo 12 settimane prima di quando ti serve. Sembra ovvio ma viene violato costantemente.

**2. Monitora costantemente**
I lead time cambiano. Un componente che oggi ha 4 settimane di lead time domani può averne 16 se va in shortage. Controlla regolarmente lo stato della supply chain.

**3. Usa forecast con i fornitori**
Se hai rapporti continuativi, condividi forecast (previsioni di ordini futuri) con i fornitori. Questo li aiuta a pianificare e può ridurre i lead time.

**4. Mantieni buffer di sicurezza**
Per componenti critici, considera di mantenere un buffer di scorta. Costa ma ti protegge da ritardi imprevisti.

---

## 🎬 Momento Serie TV

> *"Non sento l'Africa, René!"* – Stanis La Rochelle (Boris)

I lead time richiedono pazienza. Non puoi forzarli, non puoi accorciarli con la forza di volontà. Quando Stanis aspetta di "sentire l'Africa" prima di recitare, sta facendo esattamente quello che deve fare il PM con i lead time: aspettare che le cose siano pronte, senza fretta inutile. Se un componente arriva tra 10 settimane, pianifica di conseguenza e usa quel tempo per fare altro.

---

## Component shortage e obsolescenza

Il mercato dei componenti elettronici è volatile. Shortage (carenze) e obsolescenze sono eventi normali che devi saper gestire.

### Component shortage

Quando la domanda supera l'offerta, i componenti vanno in shortage: lead time si allungano, prezzi aumentano, disponibilità diventa limitata. Cause comuni:
- Picchi di domanda (es. pandemia, mining crypto, lancio nuovi device)
- Problemi produttivi dei produttori
- Disastri naturali o geopolitica
- Fine vita di tecnologie

### Come gestire gli shortage

**1. Monitora il mercato**
Usa tool come Octopart, Findchips o i portali dei distributori per monitorare disponibilità e trend dei componenti chiave.

**2. Ordina in anticipo**
Quando vedi segnali di shortage in arrivo, valuta di ordinare componenti in anticipo (se il design è stabile).

**3. Identifica alternative**
Avere già pronte alternative compatibili nella BOM ti permette di switchare velocemente se il componente primario non è disponibile.

**4. Lavora con più fornitori**
Non dipendere da un solo fornitore. Diversificare riduce il rischio.

### Obsolescenza

I produttori dichiarano componenti obsoleti (EOL - End of Life) regolarmente. Quando un componente va EOL:
- Il produttore smette di produrlo
- Devi fare un last time buy (ultimo ordine) o trovare alternative
- Se continui a produrre il tuo prodotto, devi fare un redesign

### Come gestire l'obsolescenza

**1. Scegli componenti con ciclo di vita lungo**
In fase di design, preferisci componenti mainstream con supporto a lungo termine. Evita componenti esotici o di nicchia.

**2. Monitora PCN (Product Change Notification)**
I produttori avvisano con mesi di anticipo quando un componente andrà EOL. Iscriviti alle notifiche e agisci tempestivamente.

**3. Pianifica upgrade tecnologici**
Se il tuo prodotto ha vita lunga (5+ anni), pianifica da subito upgrade periodici per sostituire componenti che andranno obsoleti.

---

## 💡 Concetto chiave

**Supply chain management è risk management.** Ogni componente è un potenziale punto di fallimento. Il PM deve identificare i rischi, monitorarli e avere piani B pronti.

---

## Tool per la gestione BOM e fornitori

### Tool per BOM management

**Arena PLM, Propel, PTC Windchill**
Piattaforme PLM (Product Lifecycle Management) professionali per gestire BOM, revisioni, approvazioni. Potenti ma costose.

**Altium 365, Fusion 360 Manage**
Soluzioni cloud-based più accessibili, integrate con tool di design.

**Google Sheets / Excel**
Per progetti piccoli o startup, un foglio Excel ben fatto può bastare. Non scala bene ma costa zero.

**PartsBox**
Tool dedicato alla gestione BOM per elettronica, con integrazione a distributori per controllo prezzi e disponibilità.

### Tool per component sourcing

**Octopart**
Motore di ricerca che aggrega dati da decine di distributori. Puoi confrontare prezzi, disponibilità, datasheet in un colpo solo.

**Findchips**
Simile a Octopart, utile per trovare componenti difficili o confrontare broker.

**Portali dei distributori (Digi-Key, Mouser, Farnell)**
Hanno tool per caricare BOM, verificare disponibilità, ottenere preventivi automatici.

---

## Best practice per BOM e fornitori

### Per la BOM

 **Mantieni una single source of truth**: una BOM master aggiornata e condivisa  
 **Versiona ogni modifica**: traccia cosa cambia e perché  
 **Valida con produzione**: coinvolgi chi produce per verificare fattibilità  
 **Calcola costi per fasce di volume**: 100pz, 1K, 10K, 100K hanno costi diversi  
 **Documenta le decisioni**: perché hai scelto quel componente? Scrivi le motivazioni  

 **Non usare componenti esotici senza motivo**: più mainstream = meno problemi  
 **Non ignorare i lead time in fase di design**: è troppo tardi scoprirlo dopo  
 **Non fare single-source**: avere un solo fornitore per componenti critici è rischioso  

### Per i fornitori

 **Costruisci relazioni a lungo termine**: i fornitori fidati sono asset preziosi  
 **Comunica con trasparenza**: condividi forecast e piani  
 **Paga in tempo**: la reputazione conta  
 **Diversifica**: non dipendere da un solo fornitore per componenti critici  
 **Monitora performance**: tieni traccia di puntualità, qualità, supporto  

 **Non cambiare fornitore solo per risparmiare il 2%**: la stabilità vale  
 **Non ordinare all'ultimo minuto**: i lead time sono reali  
 **Non ignorare le PCN**: le notifiche di cambio prodotto vanno seguite  

---

## Esempio pratico: gestire uno shortage critico

**Scenario:** Stai sviluppando un dispositivo IoT. Il microcontroller che hai scelto (un STM32 specifico) improvvisamente va in shortage globale. Lead time passa da 4 settimane a 26 settimane. La produzione è tra 8 settimane.

**Azioni del PM:**

1. **Valuta l'impatto**: senza quel componente, il progetto si ferma
2. **Cerca alternative immediate**:
   - Modelli pin-compatible della stessa famiglia STM32
   - Microcontroller di altri produttori con caratteristiche simili
3. **Contatta più fornitori**: verifica se qualcuno ha stock residuo
4. **Considera broker**: più costosi ma potrebbero avere disponibilità
5. **Valuta redesign parziale**: se necessario, modifica il design per usare componenti disponibili
6. **Comunica agli stakeholder**: avvisa subito management e clienti del rischio e delle azioni in corso
7. **Aggiorna il risk log**: documenta il problema e le azioni di mitigazione

In questo scenario, la velocità di reazione e avere già identificato alternative fa la differenza tra un ritardo di 2 settimane e uno di 6 mesi.

---

## 🧠 Cosa deve ricordare un PM

- La **BOM è un documento vivo**: va mantenuta aggiornata per tutta la vita del prodotto
- I **lead time sono vincoli fisici**: vanno pianificati, non ignorati
- **Shortage e obsolescenza** sono la norma, non l'eccezione: preparati
- Avere **componenti alternativi** identificati salva il progetto quando il componente primario non è disponibile
- I **fornitori sono partner**: trattali bene e costruisci relazioni stabili
- **Diversificare** riduce il rischio: mai dipendere da un solo fornitore per componenti critici
- Monitora costantemente **disponibilità e prezzi**: il mercato cambia velocemente

---

**Prossimo capitolo**: [Risk Management e Change Control](./05-risk-management-e-change-control.md)
