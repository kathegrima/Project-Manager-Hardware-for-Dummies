# Risk Management e Change Control

> *"Sei un idiota?" "No signore, sono un sognatore"* – Scrubs

Nel mondo hardware c'è una differenza fondamentale tra essere un sognatore e un idiota: il sognatore fa risk management. L'idiota spera semplicemente che tutto vada bene. Spoiler: non andrà bene.

---

## Cos'è il Risk Management

Il Risk Management è il processo di identificare, valutare e gestire i rischi che possono impattare il progetto. Non è pessimismo, è realismo. In un progetto hardware i rischi sono ovunque: fornitori che ritardano, componenti che vanno in shortage, test che falliscono, costi che esplodono, specifiche che cambiano.

Il PM che ignora i rischi non li elimina, semplicemente si fa trovare impreparato quando si materializzano. E si materializzeranno.

### Perché il Risk Management è cruciale nell'hardware

Nel software, molti problemi si risolvono con un fix e un deploy. Nell'hardware:
- Gli errori costano molto di più (rifabbricazione, ritardi, certificazioni da rifare)
- I tempi di recupero sono più lunghi (lead time, cicli di prototipazione)
- Le dipendenze esterne sono maggiori (fornitori, produzione, logistica)
- Le modifiche sono più costose e complesse

Un rischio non gestito in hardware può affondare il progetto o renderlo economicamente insostenibile.

---

## Il processo di Risk Management

Il Risk Management non è un'attività una tantum, è un processo continuo che accompagna tutto il progetto.

### 1. Identificazione dei rischi

Il primo passo è identificare tutti i possibili rischi. Fai brainstorming con il team, guarda progetti simili del passato (lessons learned), consulta esperti. I rischi possono essere tecnici, commerciali, operativi, esterni.

**Categorie tipiche di rischi in hardware:**

**Rischi tecnici**
- Design non funziona come previsto
- Componenti non performano secondo datasheet
- Interferenze elettromagnetiche (EMC/EMI)
- Problemi termici
- Affidabilità inferiore alle aspettative

**Rischi di supply chain**
- Componenti in shortage
- Lead time che si allungano
- Fornitori che chiudono o cambiano produzione
- Obsolescenza componenti
- Problemi qualità fornitori

**Rischi di produzione**
- Processi produttivi non validati
- Resa produttiva bassa
- Problemi di assemblaggio
- Tooling inadeguato

**Rischi di progetto**
- Team sotto-dimensionato o con competenze mancanti
- Budget insufficiente
- Timeline troppo aggressive
- Cambiamenti requisiti
- Stakeholder non allineati

**Rischi esterni**
- Normative e certificazioni
- Cambiamenti di mercato
- Competitor
- Geopolitica (dazi, guerre commerciali)

### 2. Valutazione dei rischi

Una volta identificati, i rischi vanno valutati secondo due dimensioni:

**Probabilità (P)**
Quanto è probabile che il rischio si materializzi?
- Bassa (10-30%): poco probabile
- Media (30-60%): possibile
- Alta (60-90%): probabile

**Impatto (I)**
Se il rischio si materializza, quanto impatta il progetto?
- Basso: impatto gestibile (giorni di ritardo, costi marginali)
- Medio: impatto significativo (settimane di ritardo, aumento costi 10-20%)
- Alto: impatto critico (mesi di ritardo, aumento costi >30%, rischio fallimento progetto)

La combinazione di Probabilità e Impatto determina la **priorità** del rischio.

| Probabilità / Impatto | Basso | Medio | Alto |
|----------------------|-------|-------|------|
| **Alta** | Media | Alta | Critica |
| **Media** | Bassa | Media | Alta |
| **Bassa** | Bassa | Bassa | Media |

I rischi critici e ad alta priorità richiedono attenzione immediata. Quelli a bassa priorità vanno comunque monitorati ma non richiedono azioni immediate.

### 3. Pianificazione della risposta

Per ogni rischio significativo, definisci una strategia di risposta. Ci sono quattro approcci principali:

**Evitare (Avoid)**
Elimina il rischio cambiando il piano o il design. Esempio: se un componente critico ha rischio shortage alto, scegli un componente alternativo più disponibile.

**Mitigare (Mitigate)**
Riduci la probabilità o l'impatto del rischio. Esempio: per ridurre il rischio di ritardi fornitori, ordina componenti critici con più anticipo o mantieni buffer di scorta.

**Trasferire (Transfer)**
Sposta il rischio a terzi. Esempio: usa assicurazioni, garanzie fornitori, clausole contrattuali.

**Accettare (Accept)**
Riconosci il rischio ma decidi consapevolmente di non agire, perché il costo della mitigazione supera il beneficio. Mantieni comunque un piano di contingenza.

### 4. Monitoraggio continuo

I rischi cambiano durante il progetto: nuovi rischi emergono, altri si materializzano, altri si risolvono. Il PM deve:
- Rivedere il risk register regolarmente (almeno settimanale/bisettimanale)
- Monitorare indicatori di warning (es. lead time che si allungano, problemi ricorrenti nei test)
- Aggiornare probabilità e impatto in base all'evoluzione del progetto
- Attivare piani di contingenza quando necessario

---

## 💡 Concetto chiave

**Il miglior risk management è proattivo, non reattivo.** Identificare e mitigare i rischi prima che si materializzino costa molto meno che gestire le crisi quando esplodono.

---

## Il Risk Register (o Risk Log)

Il Risk Register è il documento dove tracciare tutti i rischi del progetto. È lo strumento operativo del risk management.

### Cosa contiene un Risk Register

| Campo | Descrizione |
|-------|-------------|
| **ID** | Identificativo univoco del rischio |
| **Descrizione** | Cosa è il rischio in dettaglio |
| **Categoria** | Tecnico, supply chain, produzione, ecc. |
| **Probabilità** | Bassa / Media / Alta |
| **Impatto** | Basso / Medio / Alto |
| **Priorità** | Calcolata da P x I |
| **Strategia** | Avoid / Mitigate / Transfer / Accept |
| **Azioni di mitigazione** | Cosa fai per ridurre il rischio |
| **Owner** | Chi è responsabile di monitorare e gestire |
| **Stato** | Aperto / In monitoraggio / Chiuso / Materializzato |
| **Data review** | Ultima volta che è stato rivisto |

Mantieni il Risk Register aggiornato e condividilo con il team e gli stakeholder. Deve essere un documento vivo, non un file dimenticato in una cartella.

---

## 🎬 Momento Serie TV

> *"VEDI COSA SUCCEDE CARLA? VEDI COSA SUCCEDE QUANDO TI METTI CON UN GUERRIERO?!"* – Scrubs

Quando un rischio che avevi identificato si materializza e nessuno ti aveva ascoltato, questa è la reazione. Ma il PM professionale non dice "ve l'avevo detto", attiva il piano di contingenza che aveva preparato. Perché aveva preparato un piano di contingenza, vero?

---

## Esempi pratici di rischi hardware e relative mitigazioni

### Rischio: Componente critico in shortage
**Probabilità:** Media-Alta (dipende dal mercato)  
**Impatto:** Alto (blocca la produzione)  
**Mitigazione:**
- Identifica componenti alternativi pin-compatible già in fase di design
- Ordina componenti con 2-3 mesi di anticipo rispetto al bisogno
- Monitora costantemente disponibilità su Octopart/Findchips
- Mantieni buffer di scorta per componenti critici
- Lavora con più fornitori/distributori

### Rischio: Prototipo non passa test EMC
**Probabilità:** Media (se è il primo design di questo tipo)  
**Impatto:** Alto (richiede redesign e nuovi prototipi)  
**Mitigazione:**
- Fai pre-compliance test in-house prima dei test formali
- Coinvolgi esperti EMC già in fase di design
- Prevedi margine nel design (filtri, schermature, grounding robusto)
- Pianifica tempo e budget per 2 cicli di test EMC
- Usa design guidelines consolidati

### Rischio: Resa produttiva bassa
**Probabilità:** Media (specialmente in NPI)  
**Impatto:** Medio-Alto (aumenta costi, ritarda consegne)  
**Mitigazione:**
- Coinvolgi produzione già in fase di design (DFM - Design for Manufacturing)
- Fai pilot run prima della produzione serie
- Prevedi scarto del 5-10% nelle prime produzioni
- Identifica e risolvi problemi di processo durante NPI
- Forma adeguatamente gli operatori

### Rischio: Cambio normativo che impatta certificazioni
**Probabilità:** Bassa-Media  
**Impatto:** Alto (può richiedere modifiche design e ricertificazione)  
**Mitigazione:**
- Monitora roadmap normative del settore
- Coinvolgi consulenti normativi esperti
- Progetta con margini rispetto ai limiti normativi
- Prevedi flessibilità nel design per adattamenti futuri

---

## Change Control (gestione delle modifiche)

Nel mondo ideale, definisci le specifiche all'inizio, progetti, produci, finito. Nel mondo reale, le cose cambiano continuamente: requisiti che evolvono, problemi che emergono nei test, componenti che vanno obsoleti, opportunità di miglioramento.

Il Change Control è il processo formale per gestire queste modifiche in modo controllato, evitando il caos.

### Perché serve un processo formale

Senza change control succede questo:
- Modifiche non documentate che nessuno ricorda dopo 6 mesi
- BOM e documentazione fuori sync con il design reale
- Impatti su costi e tempi non valutati
- Stakeholder non informati
- Problemi che si scoprono in produzione

Il change control serve a:
- Valutare l'impatto di ogni modifica prima di approvarla
- Documentare cosa cambia e perché
- Assicurare che le modifiche siano comunicate a tutti i coinvolti
- Mantenere allineati design, BOM, documentazione, produzione

---

## 🎬 Momento Serie TV

> *"Come scienziato preferisco arrivare a conclusioni basate su osservazioni ed esperimenti."* – Sheldon Cooper (The Big Bang Theory)

Il change control segue lo stesso principio: le modifiche non si approvano sulla base di "secondo me" o "proviamo" ma su analisi oggettiva di impatti, costi, benefici. Serve metodo, non improvvisazione.

---

## Il processo di Change Control

### 1. Change Request (CR)

Ogni modifica inizia con una Change Request formale. Chiunque può proporre una modifica (engineering, produzione, qualità, cliente) ma deve formalizzarla.

**Una CR contiene:**
- Descrizione della modifica proposta
- Motivazione (perché serve questa modifica?)
- Impatto tecnico (cosa cambia: design, BOM, firmware, meccanica)
- Impatto su tempi (ritardi? anticipa?)
- Impatto su costi (componenti più costosi? tooling nuovo?)
- Impatto su qualità/prestazioni
- Alternative considerate
- Proponente e data

### 2. Valutazione impatti

Il PM (con il supporto del team tecnico) valuta gli impatti della modifica:
- **Tecnico**: la modifica è fattibile? Richiede test aggiuntivi? Impatta certificazioni?
- **Costi**: quanto costa implementare la modifica? (componenti, prototipazione, tooling, test, certificazioni)
- **Tempi**: quanto ritarda (o anticipa) il progetto?
- **Supply chain**: impatta disponibilità componenti?
- **Produzione**: richiede modifiche ai processi produttivi?
- **Documentazione**: cosa va aggiornato?

### 3. Approvazione

In base all'impatto, la CR viene approvata o rigettata. Per modifiche significative serve l'approvazione del management o del cliente.

**Criteri di decisione:**
- Il beneficio giustifica il costo e il ritardo?
- La modifica è necessaria (fix di un problema critico) o opzionale (nice-to-have)?
- Quali sono i rischi di NON fare la modifica?

Modifiche critiche (es. fix di bug che impatta sicurezza) si approvano quasi sempre. Modifiche "nice-to-have" che ritardano e costano tanto si rigettano spesso.

### 4. Implementazione

Se approvata, la modifica viene implementata seguendo un processo controllato:
- Aggiorna design, BOM, firmware
- Aggiorna documentazione
- Comunica la modifica a tutti i coinvolti (produzione, fornitori, qualità, supporto)
- Esegui test di verifica
- Aggiorna il numero di revisione del prodotto (es. da v1.2 a v1.3)

### 5. Chiusura

Una volta implementata e verificata, la CR viene chiusa e archiviata. La tracciabilità di tutte le modifiche è fondamentale per capire l'evoluzione del prodotto.

---

## ECO / ECN (Engineering Change Order/Notice)

Nei contesti produttivi strutturati, il change control usa terminologia specifica:

**ECN (Engineering Change Notice)**
Notifica di una modifica proposta. È la fase di proposta e valutazione.

**ECO (Engineering Change Order)**
Ordine di implementare la modifica approvata. È la fase esecutiva.

Il processo ECN → valutazione → ECO è standard in molte aziende manifatturiere.

---

## 💡 Concetto chiave

**Non tutte le modifiche vanno implementate.** Dire "no" a modifiche non essenziali che ritardano o costano troppo è parte del lavoro del PM. Il change control serve anche a proteggere il progetto da scope creep continuo.

---

## Gestire il trade-off tra flessibilità e controllo

C'è una tensione naturale nel change management:
- Troppo rigido: il progetto non si adatta a problemi reali o opportunità
- Troppo flessibile: il caos, scope creep, nessuno sa più cosa sta facendo

Il PM deve trovare il giusto equilibrio:

**Quando essere flessibili:**
- Fase iniziale di design: è normale iterare e cambiare
- Fix di problemi critici: vanno risolti subito
- Miglioramenti con ROI chiaro e impatto limitato

**Quando essere rigidi:**
- Dopo il design freeze: le modifiche devono essere giustificate bene
- In fase di certificazione: ogni modifica può invalidare test
- In produzione: modifiche richiedono validazione completa

La regola d'oro: **più avanti sei nel ciclo di vita, più alto è il costo delle modifiche**. Un cambio componente in fase di design costa ore di lavoro. Lo stesso cambio in produzione costa migliaia di euro (aggiornamento tooling, validazione processo, gestione scorte obsolete, ecc.).

---

## Tool per Risk e Change Management

**Per Risk Management:**
- **Excel/Google Sheets**: per progetti piccoli, un foglio ben strutturato funziona
- **Jira, Asana, Monday**: tool di project management hanno sezioni per risk tracking
- **Registro rischi dedicato**: molte aziende hanno template standard

**Per Change Management:**
- **PLM (Product Lifecycle Management)**: Arena, Propel, PTC Windchill gestiscono ECO/ECN formali
- **Sistemi di versionamento**: Git per firmware/software, PDM per file CAD
- **Tool di workflow**: per approvazioni e tracking

Per progetti piccoli, anche un file condiviso ben organizzato può bastare. Per progetti complessi o contesti regolamentati (medicale, automotive, aerospace) servono sistemi formali e audit trail completi.

---

## Best practice

### Per Risk Management

 **Identifica rischi presto**: non aspettare che si materializzino  
 **Rivedi il risk register regolarmente**: almeno ogni 1-2 settimane  
 **Assegna owner ai rischi**: qualcuno deve essere responsabile di monitorare  
 **Prepara piani di contingenza**: cosa fai se il rischio si materializza?  
 **Comunica i rischi agli stakeholder**: trasparenza, non nascondere problemi  

 **Non ignorare i rischi "scomodi"**: negarli non li elimina  
 **Non fare risk management solo all'inizio**: è un processo continuo  
 **Non basarti solo sull'intuizione**: usa dati e analisi  

### Per Change Control

 **Formalizza tutte le modifiche significative**: no a cambi "al volo" non documentati  
 **Valuta impatti prima di approvare**: costi, tempi, rischi  
 **Comunica le modifiche a tutti i coinvolti**: produzione, qualità, fornitori  
 **Versiona il prodotto**: ogni modifica significativa = nuova revisione  
 **Traccia la storia**: perché è stata fatta questa modifica? Scrivi le motivazioni  

 **Non accettare tutte le change request**: saper dire no è importante  
 **Non modificare senza documentare**: tra 6 mesi nessuno ricorderà perché  
 **Non sottovalutare l'impatto delle modifiche "piccole"**: si accumulano  

---

## 🧠 Cosa deve ricordare un PM

- Il **Risk Management è proattivo**: identifica e mitiga i rischi prima che esplodano
- Usa un **Risk Register** aggiornato per tracciare tutti i rischi
- Valuta i rischi per **Probabilità e Impatto**, poi prioritizza
- Per ogni rischio significativo, definisci una **strategia di risposta**
- Il **Change Control** serve a gestire le modifiche in modo controllato
- Non tutte le modifiche vanno fatte: valuta **costi, tempi, benefici**
- Più avanti sei nel progetto, **più costano le modifiche**
- Documenta tutto: tracciabilità è fondamentale in hardware

---

**Prossimo capitolo**: [Agile per hardware: si può fare?](./06-agile-per-hardware.md)
