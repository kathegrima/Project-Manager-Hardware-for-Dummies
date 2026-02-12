# Agile per hardware: si può fare?

> *"Quello che non cambia mai fa risaltare quello che cambia... i cambiamenti fanno paura ma sono inevitabili, sta a te tirarne fuori il meglio."* – Scrubs

Agile ha rivoluzionato il mondo del software. Ma nell'hardware? La domanda che tutti si pongono è: si può applicare Agile allo sviluppo di prodotti fisici? La risposta breve è: sì ma non come te lo aspetti. I cambiamenti sono necessari ma vanno adattati alla realtà dell'hardware.

---

## Il problema: Agile è nato per il software

Agile (Scrum, Kanban, XP, ecc.) nasce nel mondo software con presupposti specifici:
- **Iterazioni veloci**: deploy continui, anche più volte al giorno
- **Costo delle modifiche basso**: refactoring, fix, nuove feature si implementano rapidamente
- **Feedback immediato**: rilasci, testi, raccogli feedback, modifichi
- **Dipendenze limitate**: principalmente interne al team di sviluppo

Nell'hardware questi presupposti non reggono.

---

## Perché Agile "puro" non funziona nell'hardware

### 1. I cicli sono più lunghi
Non puoi fare uno sprint di 2 settimane se il PCB richiede 3 settimane di produzione. Non puoi iterare ogni giorno se ogni iterazione richiede ordine componenti, assemblaggio, test fisici.

### 2. Le modifiche costano molto di più
Nel software, cambiare una linea di codice costa minuti. Nell'hardware, cambiare un componente può significare: nuovo layout PCB, nuovo ordine componenti, nuovo assemblaggio, nuovi test, nuove certificazioni. Costi e tempi si moltiplicano.

### 3. Le dipendenze esterne sono maggiori
Il team software controlla quasi tutto. Il team hardware dipende da: fornitori, lead time, produzione esterna, certificazioni, logistica. Non puoi "sprintare" su cose che non controlli.

### 4. Il testing richiede hardware fisico
Non puoi testare un sensore di temperatura senza avere il sensore fisico. Non puoi validare la dissipazione termica con un mockup. Il testing hardware richiede prototipi reali, camere climatiche, strumentazione, tempo.

---

## 💡 Concetto chiave

**Agile per hardware non significa applicare Scrum alla lettera.** Significa prendere i principi Agile (iterazioni, feedback, adattamento, collaborazione) e adattarli ai vincoli dell'hardware.

---

## I principi Agile che funzionano nell'hardware

Non tutto di Agile va buttato. Alcuni principi si adattano bene, altri richiedono modifiche.

### ✅ Cosa funziona

**1. Lavoro iterativo**
Anche se più lenti, i cicli iterativi funzionano: concept → design → prototipo → test → miglioramento. Ogni ciclo affina il prodotto.

**2. Feedback continuo**
Coinvolgere utenti, clienti, produzione fin dalle prime fasi. Raccogliere feedback dai prototipi. Validare assunzioni presto invece che alla fine.

**3. Collaborazione cross-funzionale**
Team misto (hardware, firmware, meccanica, produzione, qualità) che lavora insieme invece di silos separati. Funziona benissimo nell'hardware.

**4. Prioritizzazione continua**
Il backlog di feature e miglioramenti va rivisto e riprioritizzato regolarmente in base a feedback e vincoli.

**5. Trasparenza e visibilità**
Stand-up, board visivi, metriche condivise aiutano tutti a sapere cosa sta succedendo e dove sono i problemi.

**6. Miglioramento continuo**
Retrospettive, lessons learned, adattamento dei processi. Fondamentale anche (e soprattutto) nell'hardware.

### Cosa non funziona (o va adattato pesantemente)

**1. Sprint di 2 settimane**
Troppo brevi per cicli hardware. Sprint di 4-8 settimane sono più realistici ma dipende dalla fase del progetto.

**2. Demo a fine sprint con prodotto funzionante**
Non sempre possibile. A fine sprint potresti avere design completati, componenti ordinati, test parziali. Il "prodotto funzionante" arriva più tardi.

**3. Cambiamenti continui dei requisiti**
Nel software è gestibile. Nell'hardware, cambiamenti frequenti ai requisiti possono mandare a monte mesi di lavoro. Serve più stabilità.

**4. Daily stand-up**
Utili ma da adattare. Se metà del team aspetta componenti o risultati di test che richiedono giorni, il daily può diventare ripetitivo.

---

## Come adattare Agile all'hardware

### 1. Sprint più lunghi e flessibili

Invece di sprint fissi di 2 settimane, usa sprint di durata variabile in base alla fase:
- **Fase concept/design**: sprint 2-4 settimane (lavoro prevalentemente software/design)
- **Fase prototipazione**: sprint 4-8 settimane (include ordine componenti, assemblaggio, test)
- **Fase NPI/produzione**: cadenze ancora più lunghe

Gli sprint nell'hardware seguono le milestone naturali del progetto, non calendari arbitrari.

### 2. Backlog strutturato per fasi

Il backlog non è una lista piatta di user story. Va strutturato per fase del progetto:
- **Phase 1 - Concept**: definizione requisiti, feasibility, POC
- **Phase 2 - Design**: schematic, layout, BOM, design review
- **Phase 3 - Prototyping**: ordine componenti, assemblaggio, test
- **Phase 4 - NPI**: industrializzazione, pilot run
- **Phase 5 - Production**: produzione serie, supporto

Ogni fase ha obiettivi e deliverable chiari. Le user story si mappano su queste fasi.

### 3. Definition of Done adattata

Nel software, "Done" = codice scritto, testato, deployato. Nell'hardware dipende dalla fase:
- **Design Done**: schematic approvato, BOM finalizzata, design review passata
- **Prototype Done**: prototipo assemblato, test funzionali passati, problemi documentati
- **Production Done**: processo validato, primo lotto prodotto con qualità accettabile

Ogni fase ha la sua Definition of Done. Non confondere "design completato" con "prodotto finito".

---

## 🎬 Momento Serie TV

> *"È coffee break signori"* – Duccio (Boris)

Gli sprint nell'hardware non sono corse continue senza sosta. Ci sono momenti di attesa inevitabili: aspetti i componenti, aspetti i risultati dei test, aspetti le approvazioni. Non è inefficienza, è la natura dell'hardware. Il PM deve pianificare questi "coffee break" e usarli per altre attività (documentazione, preparazione fase successiva, risk review).

---

## Scrum per hardware: un esempio pratico

Vediamo come potrebbe funzionare Scrum adattato per lo sviluppo di un dispositivo IoT.

### Sprint 0 (2 settimane): Concept
**Goal**: Definire requisiti e verificare fattibilità tecnica  
**Activities**:
- Raccolta requisiti
- Analisi mercato/competitor
- Proof of Concept su breadboard
- Identificazione componenti chiave
- Stima tempi e costi  
**Output**: Documento requisiti, POC funzionante, decisione go/no-go

### Sprint 1 (3 settimane): Design Hardware
**Goal**: Completare schematic e layout PCB  
**Activities**:
- Schematic design
- Scelta componenti definitiva
- Layout PCB
- Design review
- BOM preliminare  
**Output**: File per produzione PCB, BOM, ordine componenti avviato

### Sprint 2 (6 settimane): First Prototype
**Goal**: Assemblare e testare primo prototipo  
**Activities**:
- Ricezione PCB e componenti (4 settimane lead time)
- Assemblaggio prototipo
- Test funzionali base
- Identificazione problemi  
**Output**: Prototipo funzionante (anche con problemi), lista issue

### Sprint 3 (4 settimane): Design Refinement
**Goal**: Risolvere problemi e ottimizzare design  
**Activities**:
- Analisi root cause dei problemi
- Modifiche design
- Ordine secondo prototipo
- Inizio sviluppo firmware  
**Output**: Design rev 2, secondo prototipo ordinato

### Sprint 4 (5 settimane): Validation
**Goal**: Validare design con test completi  
**Activities**:
- Test funzionali completi
- Test ambientali (temperatura, umidità, vibrazioni)
- Test EMC (se applicabile)
- Documentazione risultati  
**Output**: Design validato, report test, go/no-go per NPI

Come vedi, gli sprint hanno durate diverse (2-6 settimane) in base alle attività e ai lead time. Non è Scrum ortodosso ma funziona per l'hardware.

---

## Kanban per hardware: un'alternativa

Kanban può funzionare meglio di Scrum per alcuni progetti hardware, specialmente per team che lavorano su più prodotti in parallelo o in fase di manutenzione/evoluzione prodotti esistenti.

### Vantaggi di Kanban nell'hardware

**1. Niente sprint fissi**
Il lavoro fluisce continuamente. Utile quando hai task con durate molto variabili (alcune ore, alcune settimane).

**2. WIP (Work In Progress) limitato**
Limiti quante attività possono essere "in corso" simultaneamente. Aiuta a focalizzare il team e evitare multitasking inefficiente.

**3. Visualizzazione del flusso**
La board Kanban mostra chiaramente dove sono i colli di bottiglia: molti task in "Waiting for components"? Problema supply chain. Task bloccati in "Testing"? Mancano risorse o strumentazione.

**4. Flessibilità**
Puoi aggiungere task urgenti senza rompere uno sprint. Utile per gestione change request o problemi produttivi urgenti.

### Board Kanban tipica per hardware

| Backlog | Design | Review | Order Parts | Waiting | Assembly | Testing | Done |


Ogni task (es. "Design rev 3 della scheda power") si sposta da sinistra a destra. Limiti il WIP in ogni colonna per evitare sovraccarichi.

---

## Hybrid approach: il più realistico

Nella pratica, molti team hardware usano approcci ibridi che prendono il meglio di Agile e di metodologie tradizionali (Waterfall, Stage-Gate):

**Macro-livello: Stage-Gate**
Il progetto segue gate classici (Concept → Design → Prototype → NPI → Production). Ogni gate ha criteri di approvazione chiari.

**Micro-livello: Agile**
All'interno di ogni fase, usi pratiche Agile: iterazioni, stand-up, backlog, board visuali, retrospettive.

**Esempio:**
- La fase "Design" è un gate Waterfall: non passi a "Prototype" finché il design non è approvato
- Ma durante la fase "Design", lavori in modo Agile: sprint brevi, design review continue, adattamenti basati su feedback

Questo approccio bilancia la stabilità necessaria nell'hardware (non puoi cambiare idea ogni settimana) con la flessibilità e la collaborazione di Agile.

---

## 🎬 Momento Serie TV

> *"Apri tutto, voglio che smarmelli!"* – Duccio (Boris)

Applicare Agile all'hardware in modo troppo semplicistico è come "smarmellare": illumini tutto in modo eccessivo e dozzinale, perdendo sfumature e profondità. Agile per hardware richiede attenzione ai dettagli, agli equilibri, alle complessità. Non puoi semplicemente "aprire tutto" e sperare che funzioni: devi adattare, calibrare, trovare il giusto compromesso tra velocità e controllo.

---

## Tool per Agile hardware

### Board e task management
- **Jira**: potente, configurabile, supporta sia Scrum che Kanban
- **Trello**: semplice, visuale, buono per team piccoli
- **Asana, Monday.com**: via di mezzo, collaborative
- **Physical board**: lavagna fisica con post-it. Sembra old-school ma funziona benissimo per visibilità immediata

### PLM integration
Per hardware è fondamentale integrare task management con PLM (Product Lifecycle Management) per gestire BOM, revisioni, documentazione. Tool come Arena, Propel, Fusion 360 Manage offrono questa integrazione.

---

## Le sfide culturali

Il vero ostacolo all'Agile hardware spesso non è tecnico, è culturale.

### Mentalità Waterfall radicata
Molti ingegneri hardware sono cresciuti con Waterfall: pianifica tutto, esegui, testa alla fine. Chiedere di iterare, di mostrare prototipi "incompleti", di cambiare in corso d'opera può generare resistenza.

### Paura del fallimento
Nel software, un test fallito è normale. Nell'hardware, un prototipo che non funziona sembra un fallimento costoso. Serve cambiare mentalità: i prototipi servono a trovare problemi, non a dimostrare che tutto è perfetto.

### Silos organizzativi
Hardware, firmware, meccanica, produzione spesso lavorano in silos separati. Agile richiede collaborazione stretta. Rompere i silos è difficile ma necessario.

### Management che vuole certezze
Agile richiede accettare incertezza e adattarsi. Management abituato a piani dettagliati con date fisse può sentirsi scomodo con approcci iterativi. Serve educazione e trasparenza.

---

## 💡 Concetto chiave

**Agile nell'hardware è più un mindset che una metodologia rigida.** L'importante non è seguire Scrum o Kanban alla lettera ma abbracciare i principi: iterazione, feedback rapido, collaborazione, adattamento, trasparenza, miglioramento continuo.

---

## Best practice per Agile hardware

 **Adatta la metodologia al tuo contesto**: non copiare Scrum software, modificalo per l'hardware  
 **Sprint allineati ai cicli naturali**: rispetta lead time e fasi del progetto  
 **Coinvolgi produzione presto**: Design for Manufacturing dal primo giorno  
 **Prototipa spesso**: anche prototipi parziali danno feedback prezioso  
 **Documenta le decisioni**: nell'hardware la tracciabilità è critica  
 **Retrospettive dopo ogni fase**: cosa ha funzionato? Cosa no? Adatta  

 **Non forzare sprint di 2 settimane**: se non ha senso per il tuo progetto, non farlo  
 **Non cambiare requisiti ogni sprint**: serve più stabilità che nel software  
 **Non ignorare i vincoli fisici**: lead time, certificazioni, produzione sono realtà  
 **Non aspettarti demo perfette ogni sprint**: il progresso nell'hardware è meno lineare  

---

## Caso pratico: sviluppo agile di una scheda IoT

**Contesto**: Startup che sviluppa sensore ambientale IoT. Team piccolo (3 hardware, 2 firmware, 1 meccanico, 1 PM).

**Approccio scelto**: Kanban ibrido con milestone Stage-Gate

**Setup:**
- Board Kanban con colonne: Backlog, Design, Review, Parts Ordered, Waiting, Assembly, Testing, Done
- Standup 3 volte a settimana (non daily perché troppo ripetitivo)
- Retrospettiva ogni 4 settimane
- Gate formali tra fase Prototype e NPI

**Risultati dopo 6 mesi:**
- 3 cicli di prototipazione completati (vs. 2 pianificati con approccio tradizionale)
- Problemi identificati e risolti prima dell'NPI
- Team più allineato e comunicazione migliore
- Time-to-market ridotto di ~20%

**Lezioni apprese:**
- WIP limit fondamentale: senza, il team si disperdeva
- Waiting column essenziale: visualizzava chiaramente i blocchi supply chain
- Standup 3x settimana giusto compromesso: abbastanza frequente ma non inutile
- Gate Stage-Gate necessari: davano checkpoints chiari per management

---

## 🧠 Cosa deve ricordare un PM

- **Agile puro non funziona nell'hardware**: va adattato ai vincoli fisici
- Gli **sprint hardware sono più lunghi** (4-8 settimane tipicamente)
- Usa **approcci ibridi**: Stage-Gate macro + Agile micro
- **Kanban** spesso funziona meglio di Scrum per hardware
- **Collaborazione cross-funzionale** è il vero valore di Agile nell'hardware
- I **lead time e dipendenze esterne** vanno rispettati, non ignorati
- **Iterazione e feedback** funzionano anche nell'hardware ma più lentamente
- Il cambio culturale è più difficile del cambio di processo

---

**Prossimo capitolo**: [Comunicazione e stakeholder management](./07-comunicazione-e-stakeholder.md)
