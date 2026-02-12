# Il ciclo di vita di un prodotto hardware

> *"Ogni viaggio inizia con un singolo passo. O con una bestemmia, dipende da come va."* – cit. sconosciuta ma veritiera

Sviluppare un prodotto hardware non è come scrivere codice: non puoi committare, pushare e vedere il risultato dopo cinque minuti. 
È un percorso lungo, fatto di fasi ben precise, ognuna con i suoi obiettivi, i suoi rischi e le sue trappole. Conoscere questo ciclo di vita è la base per fare bene il PM hardware.

---

## Le fasi principali

Un prodotto hardware attraversa diverse fasi, dalla prima scintilla dell'idea fino all'arrivo sullo scaffale (fisico o virtuale) e oltre. Le fasi principali sono:

1. **Ideazione e Concept**
2. **Feasibility Study** (Studio di fattibilità)
3. **Design e Sviluppo**
4. **Prototipazione e Test**
5. **NPI** (New Product Introduction)
6. **Produzione in serie**
7. **Lifecycle Management e EOL** (End of Life)

Ogni fase ha le sue particolarità, e il PM deve sapere cosa succede, cosa può andare storto e come tenere tutto sotto controllo.

---

## 1. Ideazione e Concept

Qui parte tutto: qualcuno ha un'idea. 
Magari il marketing ha visto un'opportunità di mercato, magari l'engineering ha pensato "sarebbe figo se...", magari un cliente ha chiesto qualcosa di specifico. 

L'idea può nascere ovunque, ma deve trasformarsi in qualcosa di concreto.

### Cosa succede in questa fase

Si definiscono i requisiti ad alto livello: cosa deve fare il prodotto? A chi si rivolge? Quali problemi risolve? 
Si fanno le prime valutazioni di mercato, si identificano i competitor, si capisce se c'è spazio per questo nuovo prodotto ma si inizia anche a ragionare su vincoli importanti come il costo target, le dimensioni, i consumi energetici.

### Il ruolo del PM

Il PM in questa fase lavora con il marketing, il management e il team tecnico per tradurre l'idea in requisiti chiari. 
Deve fare da filtro: non tutto ciò che viene proposto è fattibile o ha senso economico. Serve pragmatismo e capacità di dire "no" quando necessario, senza uccidere la creatività.

### Deliverable tipici
- Documento di requisiti iniziale
- Business case preliminare
- Prime stime di costo e time-to-market
- Identificazione dei rischi principali

---

## 2. Feasibility Study (Studio di fattibilità)

L'idea è bella sulla carta, ma è davvero realizzabile? Questa fase serve proprio a rispondere a questa domanda prima di investire (troppo) tempo e soldi nello sviluppo vero e proprio.

### Cosa succede in questa fase

Si fa un'analisi più approfondita della fattibilità tecnica ed economica del progetto. Si valutano le tecnologie disponibili, si identificano i componenti chiave, si fanno prove di concept (POC) per verificare che le idee base funzionino. 
Si studiano i fornitori potenziali, i vincoli normativi, le certificazioni necessarie. Si raffina la stima dei costi e dei tempi.

### Il ruolo del PM

Il PM coordina le analisi tecniche ed economiche, raccoglie input da tutte le funzioni coinvolte e prepara una valutazione completa da presentare al management per la decisione di go/no-go. Questa è una fase cruciale: è molto meglio fermarsi qui se il progetto non regge, piuttosto che scoprirlo dopo aver speso centinaia di migliaia di euro.

### Deliverable tipici
- Studio di fattibilità completo
- Proof of Concept (se necessario)
- Business case dettagliato
- Piano di progetto preliminare
- Decisione go/no-go

---

## 🎬 Momento Serie TV

> *"Chiudi il becco! Volevo che ti fermassi a riflettere su di te e volevo che lo facessi sul serio. In cosa sei bravo, in cosa fai schifo."* – Dr. Cox (Scrubs)

Durante lo studio di fattibilità, serve lo stesso approccio diretto di Cox: analisi onesta senza filtri. In cosa il progetto è forte? Dove zoppica? 
Questa è la fase per capirlo davvero, non per raccontarsi belle storie.

---

## 3. Design e Sviluppo

Qui entra in gioco l'engineering vero e proprio. Il prodotto inizia a prendere forma: si progettano circuiti, si scelgono componenti, si definiscono meccaniche, si sviluppa il firmware se necessario.

### Cosa succede in questa fase

Il team di progettazione lavora su schematic, layout PCB, disegni meccanici, software embedded. Si fanno continue revisioni e iterazioni per ottimizzare il design in termini di prestazioni, costi, producibilità. 
Si inizia anche a lavorare sulla supply chain: identificazione fornitori, richieste di quotazione (RFQ), negoziazione di prezzi e lead time.

Questa fase può durare settimane o mesi, a seconda della complessità del prodotto: per un semplice sensore IoT magari bastano un paio di mesi, per un dispositivo medicale o un sistema complesso possono volerci anche uno o due anni.

### Il ruolo del PM

Il PM coordina il lavoro del team di sviluppo, gestisce le milestone interne, tiene traccia dei rischi e delle modifiche. Organizza design review per assicurarsi che il progetto sia allineato ai requisiti e ai vincoli di costo e tempo. 
Tiene informati gli stakeholder sull'avanzamento e gestisce eventuali cambiamenti nei requisiti (con molta cautela, perché ogni modifica in questa fase può avere impatti significativi).

### Deliverable tipici
- Schematic elettrico
- Layout PCB
- Disegni meccanici (CAD 3D)
- BOM (Bill of Materials) preliminare
- Firmware/software embedded (se applicabile)
- Documentazione di progetto

---

## 4. Prototipazione e Test

Il design è pronto sulla carta ma funzionerà nella realtà? Questa fase serve a verificarlo attraverso la realizzazione di prototipi fisici e test approfonditi.

### Cosa succede in questa fase

Si ordinano i primi PCB e componenti, si assemblano i prototipi (spesso a mano o con piccoli lotti presso laboratori specializzati), si eseguono test funzionali, elettrici, termici, meccanici. Si verifica che il prodotto faccia quello che deve fare e che rispetti tutti i vincoli di progetto.

Quasi sempre i primi prototipi hanno problemi: un componente che si scalda troppo, un connettore che non entra, un firmware che si blocca in certe condizioni. È normale e fa parte del processo. L'importante è trovare i problemi ora, non dopo aver prodotto 10.000 pezzi.

### Il ruolo del PM

Il PM gestisce i cicli di prototipazione e test, coordina le modifiche necessarie (che possono richiedere nuove revisioni del design e nuovi prototipi), tiene traccia dei problemi aperti e delle azioni correttive. Questa fase può essere molto stressante perché i tempi si allungano facilmente e i costi possono salire se servono molte iterazioni.

### Deliverable tipici
- Prototipi funzionanti
- Report di test
- Design aggiornato post-test
- BOM aggiornata
- Documentazione di eventuali certificazioni (EMC, safety, ecc.)

---

## 💡 Concetto chiave

**In hardware il tempo è fisico.** Non puoi accelerare la produzione di un PCB che richiede 3 settimane di lead time. Non puoi far arrivare un componente dall'Asia in un giorno. Non puoi saltare i test di certificazione. Il PM deve conoscere questi vincoli e pianificare di conseguenza.

---

## 🎬 Momento Serie TV

> *""Nulla di buono è mai accaduto dopo le 2 di notte."*  – Ted Mosby (How I Met Your Mother)

Sviluppare un prodotto hardware richiede tempo, pazienza e impegno e chi cerca scorciatoie di solito le paga care più avanti. 
Il PM deve avere il polso della situazione e la pazienza di fare le cose per bene.

---

## 🧠 Cosa deve ricordare un PM

- Il ciclo di vita hardware ha **fasi ben definite**: concept, feasibility, design, prototipazione, NPI, produzione, EOL
- Ogni fase ha **obiettivi e deliverable specifici** che vanno rispettati
- La **prototipazione è iterativa**: pianifica almeno 2-3 cicli
- L'**NPI è critica**: problemi non risolti qui costano molto in produzione
- I **tempi sono fisici**: lead time, certificazioni, tooling non si possono comprimere a piacere
- Meglio **fermarsi nel feasibility study** se il progetto non regge, che scoprirlo dopo

---

**Prossimo capitolo**: [Pianificazione: WBS, Gantt, Milestone](./03-pianificazione-wbs-gantt-milestone.md)
