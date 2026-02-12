# Pianificazione: WBS, Gantt, Milestone

> *"Volevo solo aiutare la gente, la cosa più dura è quanto in fretta devi andare avanti."* – J.D. (Scrubs)

La pianificazione è il cuore del lavoro del PM: puoi avere il team migliore del mondo ma senza una pianificazione solida stai solo sperando che le cose vadano bene. E nel mondo hardware, la speranza non è una strategia.

---

## Perché pianificare è fondamentale

In un progetto hardware non puoi improvvisare: i lead time sono lunghi, i costi sono alti, le dipendenze sono complesse. Se ordini i componenti sbagliati o al momento sbagliato, non è come rifare un deploy: hai perso settimane e migliaia di euro.

Una buona pianificazione ti permette di:
- Avere una visione chiara di cosa fare e quando
- Identificare colli di bottiglia e rischi prima che diventino problemi
- Coordinare il lavoro di persone e team diversi
- Comunicare in modo trasparente con gli stakeholder
- Tenere sotto controllo tempi e costi

Pianificare bene richiede tempo ma è tempo che recuperi (con gli interessi) durante l'esecuzione del progetto.

---

## La WBS (Work Breakdown Structure)

La WBS è la scomposizione gerarchica del progetto in elementi più piccoli e gestibili. È il primo passo fondamentale: prima di pianificare quando fare le cose, devi sapere **quali** cose fare.

### Come funziona

La WBS parte dal risultato finale (il prodotto completo) e lo scompone progressivamente in deliverable sempre più piccoli, fino ad arrivare a work package gestibili. È una struttura ad albero dove ogni livello aggiunge dettaglio.

**Esempio per lo sviluppo di un sensore IoT:**

Sensore IoT (Livello 0)
├── Hardware (Livello 1)
│ ├── Schematic design (Livello 2)
│ ├── PCB layout (Livello 2)
│ ├── BOM definition (Livello 2)
│ └── Prototipazione (Livello 2)
├── Firmware (Livello 1)
│ ├── Driver sensori (Livello 2)
│ ├── Stack comunicazione (Livello 2)
│ └── Power management (Livello 2)
├── Meccanica (Livello 1)
│ ├── Design case (Livello 2)
│ └── Tooling (Livello 2)
└── Testing & Validation (Livello 1)
├── Test funzionali (Livello 2)
├── Test ambientali (Livello 2)
└── Certificazioni (Livello 2)


Ogni elemento del livello più basso diventa un work package: un'unità di lavoro con responsabilità chiara, durata stimabile e deliverable definito.

### Come creare una WBS efficace

**1. Parti dal risultato finale**
Identifica il deliverable principale (il prodotto finito) e chiediti: quali sono i macro-blocchi necessari per arrivare lì?

**2. Scomponi per deliverable, non per attività**
La WBS ragiona in termini di "cosa" produce il lavoro, non di "come" lo fai. Non è un elenco di azioni, è una mappa di risultati.

**3. Scendi fino a un livello gestibile**
Continua a scomporre finché ogni elemento è:
- Assegnabile a una persona o un piccolo team
- Stimabile in termini di tempo e costo
- Verificabile (capisci quando è completato)

Tipicamente 3-4 livelli sono sufficienti per la maggior parte dei progetti hardware.

**4. Applica la regola 100%**
Ogni livello deve includere il 100% del lavoro necessario. Se manca qualcosa nella WBS manca nel progetto.

### Errori comuni

- Confondere WBS con cronoprogramma: la WBS non ha date, solo struttura  
- Mischiare deliverable e attività  
- Scendere troppo in dettaglio (micromanagement) o rimanere troppo generici  
- Dimenticare elementi trasversali (project management, documentazione, quality assurance)  

---

## 💡 Concetto chiave

**La WBS è la spina dorsale del progetto.** Se la WBS è incompleta o mal strutturata, tutto quello che viene dopo (pianificazione, budgeting, monitoring) sarà sbagliato. Vale la pena investire tempo per farla bene.

---

## Il Gantt Chart

Una volta che hai la WBS (sai **cosa** fare), devi capire **quando** farlo. Il Gantt chart è lo strumento principe per visualizzare la timeline del progetto.

### Come funziona

Il Gantt è un diagramma a barre dove:
- L'asse orizzontale rappresenta il tempo (giorni, settimane, mesi)
- Ogni riga rappresenta un task o work package
- Le barre mostrano durata e posizione temporale delle attività
- Le dipendenze tra task sono rappresentate con frecce

È uno strumento visivo potente: a colpo d'occhio vedi chi deve fare cosa, quando, e quali attività sono collegate.

### Elementi chiave del Gantt

**1. Task e durate**
Ogni work package della WBS diventa un task nel Gantt con una durata stimata. La stima deve essere realistica: considera la complessità, le risorse disponibili, i rischi.

**2. Dipendenze**
Le dipendenze collegano task che non possono iniziare finché altri non sono completati. Ci sono quattro tipi principali:
- **Finish-to-Start (FS)**: il task B inizia quando A finisce (la più comune)
- **Start-to-Start (SS)**: B può iniziare solo quando A è iniziato
- **Finish-to-Finish (FF)**: B finisce quando A finisce
- **Start-to-Finish (SF)**: B finisce quando A inizia (rarissima)

Nel mondo hardware le dipendenze FS sono dominanti: non puoi fare il layout PCB prima dello schematic, non puoi testare prima di avere il prototipo.

**3. Risorse**
Ogni task deve avere un responsabile. Il Gantt ti aiuta a vedere se una persona è sovraccarica (troppi task in parallelo) o sottoutilizzata.

**4. Slack/Float**
Alcune attività hanno margine (slack): possono slittare senza impattare la data finale. Altre sono sul critical path (vedi dopo) e ogni ritardo si traduce in ritardo del progetto.

### Come creare un Gantt efficace

**1. Inizia dalla WBS**
Trasforma ogni work package in un task. Aggiungi task di coordinamento se necessari (meeting, review, approvazioni).

**2. Stima le durate**
Chiedi agli esperti quanto tempo serve per ogni task. Considera:
- Complessità tecnica
- Esperienza del team
- Disponibilità delle risorse
- Lead time di fornitori (questo è critico in hardware!)

Aggiungi sempre un buffer per gli imprevisti ma non esagerare: un buffer troppo grande nasconde problemi invece di gestirli.

**3. Definisci le dipendenze**
Identifica quali task dipendono da altri. Sii rigoroso: dipendenze sbagliate generano piani irrealistici.

**4. Assegna le risorse**
Chi fa cosa? Verifica che nessuno sia allocato al 150% (succede più spesso di quanto pensi).

**5. Identifica il critical path**
Il critical path è la sequenza di task che determina la durata minima del progetto. Qualsiasi ritardo su questi task ritarda l'intero progetto. Il PM deve monitorare il critical path come un falco.

### Tool per il Gantt

Esistono decine di strumenti:
- **Microsoft Project**: il classico, potente ma pesante
- **Smartsheet**: moderno e collaborativo
- **GanttProject**: open source e gratuito
- **Asana, Monday.com, ClickUp**: tool generici con funzioni Gantt
- **Excel**: per progetti semplici può bastare (ma scala male)

Scegli il tool in base alle dimensioni del progetto e alla collaborazione necessaria. Per progetti complessi serve un tool robusto, per progetti piccoli va bene anche un foglio Excel ben fatto.

---

## 🎬 Momento Serie TV

> *"Devi ascoltare i messaggi, Leonard. Lasciare un messaggio rappresenta metà di un contratto sociale che è completato dall'ascolto del messaggio. Se quel contratto viene meno, allora tutti i contratti sociali verranno meno e piomberemo nell'anarchia."* – Sheldon Cooper (The Big Bang Theory)

Le dipendenze nel Gantt funzionano esattamente come i contratti sociali di Sheldon: sono accordi che vanno rispettati: se il team A non consegna quando promesso, il team B non può iniziare. 
Se ignori le dipendenze, il progetto piomba nel caos. Nessuna pressione, tranquillo.

---

## Le Milestone

Le milestone sono i checkpoint del progetto: punti specifici nella timeline che segnano il completamento di fasi importanti. Non sono task (non hanno durata), sono traguardi.

### Perché le milestone sono importanti

Le milestone servono a:
- Dare visibilità agli stakeholder sull'avanzamento
- Creare punti di verifica e decisione
- Mantenere il team focalizzato su obiettivi intermedi
- Permettere correzioni di rotta prima che sia troppo tardi

Una milestone ben definita è un momento in cui puoi dire con certezza: "Abbiamo raggiunto questo obiettivo".

### Come definire milestone efficaci

**1. Collegale a deliverable concreti**
Una milestone deve essere verificabile. "Design completato" è vago. "Schematic approvato e layout PCB rilasciato per produzione" è chiaro.

**2. Distribuiscile lungo il progetto**
Non concentrare tutte le milestone alla fine. Milestone intermedie ti permettono di monitorare e correggere.

**3. Rendile significative**
Non ogni task è una milestone. Le milestone segnano passaggi importanti: completamento di fasi, approvazioni critiche, delivery di prototipi.

### Esempi di milestone tipiche in hardware

| Milestone | Deliverable verificabile |
|-----------|--------------------------|
| **Concept approval** | Documento di concept approvato dal management |
| **Design freeze** | Schematic e BOM congelati, approvati per prototipazione |
| **First prototype** | Primo prototipo assemblato e acceso |
| **Design validation** | Test completati con successo, design approvato per produzione |
| **Pilot run completed** | Primo lotto pilota prodotto e verificato |
| **Production ready** | Processo produttivo validato, go per produzione di serie |

Ogni milestone ha criteri di accettazione chiari. Se i criteri non sono soddisfatti, la milestone non è raggiunta. Semplice.

---

## Il Critical Path (percorso critico)

Il critical path è la sequenza di task che determina la durata totale del progetto. È la catena più lunga di attività dipendenti: se ritardi una di queste, ritardi tutto.

### Come identificare il critical path

Il critical path si calcola attraverso il **Critical Path Method (CPM)**:

1. **Forward pass**: parti dall'inizio e calcola la data più presto possibile per ogni task
2. **Backward pass**: parti dalla fine e calcola la data più tardi possibile senza ritardare il progetto
3. **Calcola lo slack**: la differenza tra "più tardi" e "più presto" ti dice il margine di ogni task
4. **Identifica il critical path**: i task con slack zero sono sul critical path

La maggior parte dei tool di project management calcola automaticamente il critical path. Il tuo lavoro come PM è monitorarlo costantemente.

### Perché il critical path è cruciale

Ogni ritardo sul critical path si traduce in ritardo del progetto finale. Se un task sul critical path slitta di una settimana, il progetto slitta di una settimana. Fine.

Task fuori dal critical path hanno slack: possono ritardare un po' senza impattare il progetto (entro certi limiti). Questo ti dice dove concentrare l'attenzione: il critical path è la tua priorità numero uno.

### Gestire il critical path

**Quando sei in ritardo sul critical path:**
- Aggiungi risorse ai task critici (se possibile)
- Riduci lo scope di task non critici per liberare risorse
- Cerca di parallelizzare attività dove possibile
- Negozia estensioni di deadline (ultima spiaggia)

**Attenzione:** aggiungere troppe risorse a un task non sempre accelera. C'è un limite oltre il quale più persone rallentano invece che accelerare (legge di Brooks: "adding manpower to a late project makes it later").

---

## Concetto chiave

**Il critical path non è fisso.** Può cambiare durante il progetto se task critici vengono completati prima del previsto o se task non critici slittano consumando tutto lo slack. Il PM deve ricalcolare e monitorare il critical path regolarmente.

---

## Pianificazione realistica vs. pianificazione ottimistica

Uno degli errori più comuni è fare pianificazioni troppo ottimistiche. Il problema non è che le cose vadano sempre male ma che le cose vanno **raramente** nel modo perfetto che hai immaginato.

### Come fare stime realistiche

**1. Coinvolgi chi farà il lavoro**
Le stime top-down (imposte dal management) sono quasi sempre sbagliate. Chi conosce il lavoro meglio di chi lo deve fare?

**2. Considera i lead time reali**
In hardware i lead time sono critici. Se un componente ha 12 settimane di lead time, non puoi pianificare di averlo in 6. Verifica sempre con i fornitori.

**3. Aggiungi buffer ai task critici**
Non a tutti i task (altrimenti diventa tutto buffer) ma ai task sul critical path e ad alta incertezza. Usa la tecnica del **PERT** (Program Evaluation and Review Technique):
- Stima ottimistica (O)
- Stima pessimistica (P)
- Stima più probabile (M)
- Stima PERT = (O + 4M + P) / 6

**4. Pianifica contingency time**
Aggiungi un buffer generale (10-20% del tempo totale) per imprevisti. Non distribuirlo nei singoli task, tienilo come riserva di progetto.

**5. Rivedi regolarmente**
La pianificazione non è scolpita nella pietra. Rivisitala regolarmente e aggiustala in base alla realtà.

---

## 🎬 Momento Serie TV

> *""Sono un fisico, non posso farci niente se la realtà non coincide con le tue aspettative."*  – Sheldon Cooper (The Big Bang Theory)

Questa è la reazione tipica quando il piano incontra la realtà. Il fornitore che prometteva 4 settimane consegna dopo 8. Il test che "sicuramente passa" fallisce. Il componente che "è disponibile" è andato in shortage globale. Pianificare bene significa mettere in conto che alcune cose andranno storte e avere un piano B.

---

## Tool e best practice

### Tool consigliati

**Per progetti piccoli/medi:**
- Asana, Trello, Monday.com (con funzioni Gantt)
- Smartsheet (ottimo compromesso tra potenza e usabilità)
- Excel/Google Sheets (per progetti semplici)

**Per progetti complessi:**
- Microsoft Project (lo standard ma richiede formazione)
- Primavera P6 (per progetti molto grandi e complessi)
- Jira (se lavori in metodologia Agile/ibrida)

### Best practice

 **Condividi il piano con tutto il team**: un piano che solo tu conosci è inutile  
 **Aggiorna il Gantt regolarmente**: almeno settimanalmente  
 **Usa milestone per le decisioni**: milestone = gate per procedere o fermarsi  
 **Comunica gli slittamenti subito**: nascondere problemi li peggiora solo  
 **Traccia le modifiche al piano**: capire perché il piano è cambiato aiuta a imparare  

 **Non fare piani troppo dettagliati**: scendere al livello orario è micromanagement  
 **Non ignorare le dipendenze**: sono il cuore della pianificazione hardware  
 **Non pianificare al 100% di capacità**: lascia margine per imprevisti  

---

## 🧠 Cosa deve ricordare un PM

- La **WBS** scompone il progetto in elementi gestibili ed è la base di tutto
- Il **Gantt** visualizza timeline, dipendenze e risorse
- Le **milestone** sono checkpoint verificabili per monitorare l'avanzamento
- Il **critical path** identifica i task che non possono slittare
- Le stime devono essere **realistiche**, non ottimistiche
- La pianificazione è **iterativa**: va rivista regolarmente in base alla realtà
- In hardware i **lead time** sono vincoli fisici che non puoi ignorare

---

**Prossimo capitolo**: [Gestione BOM e fornitori](./04-gestione-bom-e-fornitori.md)
