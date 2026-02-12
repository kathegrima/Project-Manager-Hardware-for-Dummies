# Comunicazione e stakeholder management

> *"Nella fiction la fotografia non deve essere più bella di quella della pubblicità, sennò la gente cambia canale"* – Duccio Patanè (Boris)

La comunicazione è come la fotografia di Duccio: devi adattarla al tuo pubblico. Non puoi parlare di impedenze, EMC e schematic con il marketing. Non puoi dire "è complicato" al management che vuole date precise. Il PM è il traduttore universale del progetto: deve saper comunicare con linguaggi diversi, mantenendo tutti allineati senza far cambiare canale a nessuno.

---

## Perché la comunicazione è critica

In un progetto hardware ci sono decine di persone coinvolte: ingegneri, produzione, fornitori, management, marketing, commerciali, finance, clienti. Ognuno ha priorità diverse, linguaggi diversi, aspettative diverse. Se il PM non comunica bene:
- Le aspettative diventano irrealistiche
- Le decisioni vengono prese su informazioni sbagliate
- I problemi emergono troppo tardi
- Il team perde fiducia e motivazione
- Gli stakeholder si sentono ignorati

La comunicazione non è "la parte facile" del lavoro del PM. È una delle più critiche e richiede competenza, strategia e attenzione continua.

---

## I diversi tipi di stakeholder

Ogni stakeholder ha bisogni informativi diversi. Il PM deve riconoscerli e adattare la comunicazione.

### Management / Executives
**Cosa vogliono:**
- Sintesi: stato progetto, rischi principali, decisioni necessarie
- Business impact: costi, tempi, ROI
- Problemi critici che richiedono escalation

**Come comunicare:**
- Executive summary (1 pagina massimo)
- RAG status (Red/Amber/Green)
- Focus su eccezioni e decisioni, non dettagli tecnici
- Preparati a giustificare ritardi o extra-costi con dati

**Frequenza:** Settimanale o bisettimanale

### Team tecnico (Engineering)
**Cosa vogliono:**
- Dettagli tecnici: specifiche, vincoli, problemi da risolvere
- Contesto delle decisioni: perché questa scelta?
- Feedback su proposte e design
- Chiarezza su priorità

**Come comunicare:**
- Linguaggio tecnico appropriato
- Documentazione dettagliata
- Meeting tecnici focalizzati
- Canali aperti per discussioni (Slack, email, stand-up)

**Frequenza:** Daily/frequent

### Produzione / Manufacturing
**Cosa vogliono:**
- Producibilità: questo design è fattibile?
- BOM chiara e stabile
- Processi definiti: come assemblare, testare, validare
- Lead time realistici
- Problemi di qualità da risolvere

**Come comunicare:**
- Coinvolgili presto (Design for Manufacturing)
- Documentazione operativa (work instructions, test procedures)
- Pilot run e feedback loop
- Trasparenza su modifiche (ogni cambio BOM li impatta)

**Frequenza:** Regolare durante design e NPI, poi su necessità

### Marketing / Sales
**Cosa vogliono:**
- Caratteristiche del prodotto: cosa fa, perché è meglio della concorrenza
- Date di lancio
- Prezzi target
- Materiale per comunicazione (foto, video, specifiche commerciali)

**Come comunicare:**
- Linguaggio business, non tecnico
- Focus su benefici per l'utente, non su dettagli implementativi
- Sii chiaro su cosa è confermato vs ancora incerto
- Gestisci aspettative su tempi (non promettere l'impossibile)

**Frequenza:** Milestone-based

### Finance / Procurement
**Cosa vogliono:**
- Budget: spese previste e consuntivo
- Forecast: quando servono i soldi
- Giustificazioni per extra-costi
- ROI e business case

**Come comunicare:**
- Numeri precisi e tracciabili
- Confronto budget vs actual con spiegazioni degli scostamenti
- Forecast aggiornati regolarmente
- Documentazione per approvazioni

**Frequenza:** Mensile o su milestone

### Fornitori
**Cosa vogliono:**
- Ordini chiari (BOM, quantità, date)
- Forecast per pianificare produzione
- Feedback su qualità e servizio
- Pagamenti puntuali

**Come comunicare:**
- Professionale e chiaro
- RFQ formali per ordini importanti
- Trasparenza su piani futuri (aiuta a ottenere lead time migliori)
- Rispetto reciproco: sono partner, non nemici

**Frequenza:** Su necessità, più frequente in fase NPI/produzione

### Clienti (se applicabile)
**Cosa vogliono:**
- Il prodotto funziona come promesso?
- Quando lo ricevo?
- Supporto in caso di problemi

**Come comunicare:**
- Trasparenza su stato e tempi
- Gestione aspettative realistica
- Proattività nel comunicare ritardi o problemi
- Linguaggio orientato al valore

**Frequenza:** Milestone-based e su richiesta

---

## 🎬 Momento Serie TV

> *"Ragazzi, nella vita di un uomo ogni esperienza è come un puntino in un quadro impressionista!"* – Ted Mosby (How I Met Your Mother)

Ogni stakeholder vede solo il suo puntino: finance vede i costi, engineering vede la tecnologia, marketing vede le feature. Il PM è l'unico che vede (e deve mostrare) il quadro completo. La tua comunicazione deve aiutare ognuno a capire come il suo puntino contribuisce al dipinto finale.

---

## Gli strumenti di comunicazione del PM

### Status report

Il classico documento di aggiornamento, tipicamente settimanale o bisettimanale. Deve essere:
- **Conciso**: 1-2 pagine, non un romanzo
- **Strutturato**: formato standard che tutti si aspettano
- **Chiaro**: RAG status visivo, highlight, lowlight

**Template tipico:**
> **📋 PROJECT STATUS REPORT**
>
> ---
>
> **Project Name:** [Nome progetto]  
> **Report Week:** [gg/mm/yyyy - gg/mm/yyyy]  
> **PM:** [Nome Project Manager]  
> **Overall Status:** 🟢 Green | 🟡 Amber | 🔴 Red
>
> ---
>
> ### 📊 Executive Summary
> [1-2 righe che riassumono lo stato generale del progetto e eventuali punti critici]
>
> ---
>
> ### Highlights (Successi della settimana)
> - Prototipo rev 2 ricevuto e testato con successo
> - Design review completata con feedback positivi dal team
> - Certificazione EMC superata al primo tentativo
>
> ---
>
> ### Lowlights (Problemi e criticità)
>
> | Problema | Impatto | Azione in corso |
> |----------|---------|-----------------|
> | Componente X in shortage | Lead time +4 settimane | Identificato componente alternativo |
> | Test termici oltre specifiche | Rischio riprogettazione | Meeting tecnico martedì |
>
> ---
>
> ### Next Steps (Prossima settimana)
> 1. Implementare modifiche design per problema termico
> 2. Ordine componenti alternativi per X
> 3. Avvio pilot run con fornitore Y
> 4. Completare documentazione per certificazioni
>
> ---
>
> ### Decisions Needed (Decisioni richieste)
>
> | Decisione | Owner | Deadline |
> |-----------|-------|----------|
> | Approvazione extra-budget €5.000 | Finance / Management | Fine settimana |
> | Priorità: tempi vs costi? | Steering Committee | 20/02/2026 |
>
> ---
>
> ### Key Metrics
>
> | Metrica | Target | Actual | Status |
> |---------|--------|--------|--------|
> | **Budget** | €100.000 | €75.000 (75%) | 🟢 On track |
> | **Timeline** | 12 mesi | 9 mesi (75%) | 🟢 On track |
> | **Open Risks** | < 3 high | 2 High, 5 Medium | 🟡 Monitor |
>
> **Milestone Progress:**  
> Concept approval | Design freeze | Prototype validation (in corso) | Pilot run | Production ready
>
> ---
>
> ### Top Risks
>
> | Rischio | P | I | Strategia |
> |---------|---|---|-----------|
> | Shortage componente critico | Alta | Alto | Alternative + doppio sourcing |
> | Ritardo certificazioni | Media | Alto | Pre-test + consulente esterno |
>
> ---

### Dashboard e KPI

Per progetti complessi, un dashboard visivo è più efficace di report testuali. Strumenti come Smartsheet, Monday, Jira permettono di creare dashboard condivisi con:
- Timeline e milestone
- Budget (planned vs actual)
- Rischi aperti
- Task in progress
- Burn-down charts

Il vantaggio: stakeholder possono consultare quando vogliono, tu risparmi tempo in status update.

### Meeting strutturati

**Stand-up / Sync meeting (15-30 min, 2-3x settimana)**
- Cosa ho fatto
- Cosa farò
- Blocchi/problemi
- Veloce, in piedi, focalizzato

**Design review (1-2h, su necessità)**
- Review tecnica approfondita di design
- Team tecnico + stakeholder rilevanti
- Output: approvazioni, feedback, azioni

**Steering committee (1h, mensile)**
- Review strategica con management
- Budget, timeline, rischi, decisioni chiave
- Preparazione importante: porta dati, non opinioni

**Retrospettiva (1-2h, a fine fase)**
- Cosa ha funzionato bene
- Cosa può migliorare
- Azioni concrete per prossima fase
- Ambiente safe, no blame game

### Comunicazione informale

Non sottovalutare: caffè, chiacchierate corridoio, messaggi Slack. Spesso qui emergono problemi prima che diventino crisi. Mantieni canali aperti e approccio accessibile.

---

## Come gestire le aspettative

Uno dei compiti più difficili del PM è gestire le aspettative degli stakeholder, specialmente quando le cose non vanno come previsto (e non andranno come previsto).

### Sii realistico fin dall'inizio

Non vendere sogni. Se il progetto richiede 12 mesi, non dire "forse 8" per far contenti tutti. Meglio promettere 12 e consegnare in 11, che promettere 8 e consegnare in 14. La credibilità persa è difficile da recuperare.

### Comunica i problemi presto

Quando emerge un problema, non aspettare che si risolva da solo o che diventi una crisi. Comunica subito:
- Qual è il problema
- Qual è l'impatto (tempi, costi, qualità)
- Quali sono le opzioni
- Cosa proponi come soluzione

Gli stakeholder perdonano i problemi comunicati presto con proposte di soluzione. Non perdonano sorprese dell'ultimo minuto.

### Usa i dati, non le opinioni

"Secondo me andrà bene" non convince nessuno. "I test mostrano che il design passa le specifiche termiche con margine del 15%" sì. Porta dati, misure, evidenze. Rendi oggettivo ciò che è oggettivabile.

### Spiega il contesto

Non dare solo il risultato, spiega il perché. "Il componente è in shortage globale per incremento domanda settore automotive, tutti i fornitori hanno 16 settimane di lead time" è molto più efficace di "il componente arriva tardi".

---

## 🎬 Momento Serie TV

> *"In Italia vale la regola delle tre G: la Giusta telefonata, al Giusto momento, alla Giusta persona!"* – (Boris)

La comunicazione non è solo cosa dici ma quando e a chi lo dici. Un problema critico va comunicato subito al decision maker, non in un report settimanale che legge dopo 3 giorni. Una proposta di ottimizzazione può aspettare il prossimo steering committee. Saper scegliere il momento e il canale giusto è competenza fondamentale.

---

## Gestire comunicazioni difficili

Non tutte le comunicazioni sono facili. Ecco come gestire situazioni complesse.

### Comunicare ritardi

**Cosa fare:**
- Spiega le cause (oggettive, con dati)
- Quantifica il ritardo (non "un po'" ma "3 settimane")
- Proponi soluzioni o mitigazioni
- Aggiorna le milestone e il piano
- Comunica l'impatto su budget se applicabile

**Cosa non fare:**
- Dare la colpa ad altri
- Minimizzare ("sono solo pochi giorni")
- Promettere recuperi irrealistici
- Aspettare l'ultimo minuto per dirlo

### Comunicare problemi tecnici

**Cosa fare:**
- Usa linguaggio appropriato allo stakeholder (semplifica per non-tecnici)
- Spiega l'impatto business (non solo il problema tecnico)
- Proponi alternative o workaround
- Dai tempi realistici per la risoluzione

**Cosa non fare:**
- Dire "è complicato" senza spiegare
- Usare gergo tecnico con chi non lo capisce
- Spaventare con scenari catastrofici senza dati
- Nascondere la gravità

### Gestire richieste impossibili

Stakeholder: "Possiamo anticipare il lancio di 2 mesi?"

**Risposta efficace:**
"Capisco l'opportunità di mercato. Analizziamo le opzioni:
1. Mantenere scope completo: delivery stimata tra 12 mesi (scenario ottimistico) e 14 mesi (realistico)
2. Ridurre scope (eliminare feature X e Y): delivery stimata tra 10-11 mesi
3. Aumentare team (+2 persone): delivery stimata tra 11-12 mesi, +€50K budget

Anticipo di 2 mesi (8 mesi totali) non è fattibile senza compromettere qualità o completezza. Quale opzione preferiamo esplorare?"

**Cosa NON fare:**
- Dire semplicemente "no, impossibile"
- Accettare l'impossibile per far contento lo stakeholder (poi fallisci)
- Sentirti in colpa per limiti oggettivi

---

## Concetto chiave

**Il silenzio è il peggior tipo di comunicazione.** Quando non comunichi, gli stakeholder riempiono il vuoto con supposizioni, quasi sempre negative. Meglio over-comunicare che under-comunicare.

---

## Comunicazione in situazioni di crisi

Quando le cose vanno male (prototipo fallisce, shortage critico, budget esploso), la comunicazione diventa ancora più importante.

### Principi di crisis communication

**1. Velocità**
Comunica subito, anche se non hai tutte le risposte. "Abbiamo identificato un problema X, stiamo analizzando, aggiornerò entro domani con dettagli" è meglio del silenzio.

**2. Trasparenza**
Non minimizzare, non nascondere. Sii onesto sulla gravità. La fiducia si costruisce con la trasparenza, soprattutto nei momenti difficili.

**3. Piano d'azione**
Non solo il problema ma cosa stai facendo per risolverlo. Gli stakeholder vogliono sapere che sei in controllo.

**4. Frequenza**
In crisi, aumenta la frequenza di comunicazione. Daily update se necessario. Riduce ansia e mostra che la situazione è monitorata.

**5. Leadership**
Tu sei il punto di riferimento. Mantieni la calma, mostra competenza, evita panico. Il tuo atteggiamento influenza quello del team.

---

## Best practice per comunicazione efficace

### Per report scritti

 **Usa executive summary**: chi ha poco tempo legge solo quello  
 **Struttura chiara**: titoli, bullet point, non blocchi di testo  
 **Evidenzia eccezioni**: cosa è rosso/giallo, non ripetere tutto il verde  
 **Usa visual**: grafici, dashboard, timeline visuali comunicano più di tabelle  
 **Scrivi per il lettore**: adatta linguaggio e dettaglio allo stakeholder  

 **Non scrivere romanzi**: nessuno li legge  
 **Non nascondere problemi in mezzo al testo**: evidenziali  
 **Non usare gergo inutile**: se puoi dire "ritardo" invece di "slippage temporale", fallo  

### Per meeting

 **Prepara agenda**: tutti sanno di cosa si parla  
 **Rispetta i tempi**: inizia e finisci in orario  
 **Focalizza**: un meeting un obiettivo  
 **Documenta decisioni**: chi fa cosa entro quando  
 **Follow-up**: invio note con action items entro 24h  

 **Non fare meeting senza obiettivo**: "ci aggiorniamo" non è un obiettivo  
 **Non lasciare che il meeting vada off-topic**: riporta focus  
 **Non fare meeting che potevano essere email**  

### Per comunicazione informale

 **Sii accessibile**: rispondi in tempi ragionevoli  
 **Sii chiaro**: anche su Slack/email, chiarezza prima di tutto  
 **Usa il canale giusto**: urgenze al telefono, non via email  
 **Conferma comprensione**: "per essere sicuro di aver capito, tu dici che..."  

 **Non ignorare messaggi**: anche "visto, ci torno sopra" è meglio del silenzio  
 **Non dare per scontato**: conferma che il messaggio sia arrivato chiaro  

---

## Tool per la comunicazione

**Project management:**
- Jira, Asana, Monday: task, status, timeline condivisi
- Smartsheet: ottimo per dashboard e report visuali
- MS Project: per Gantt e pianificazione dettagliata

**Documentazione:**
- Confluence, Notion: wiki di progetto, documentation hub
- Google Docs: collaborazione real-time
- SharePoint: per aziende Microsoft-centric

**Comunicazione real-time:**
- Slack, Teams: chat, canali tematici, integrazione tool
- Zoom, Meet: videocall per review e meeting

**Reportistica:**
- PowerPoint/Google Slides: presentazioni executive
- Tableau, Power BI: dashboard analitici avanzati
- Excel/Sheets: report numerici e budget

La scelta del tool dipende dall'ecosistema aziendale e dalle preferenze del team. L'importante è che tutti lo usino e che sia aggiornato.

---

## 🧠 Cosa deve ricordare un PM

- Il PM è il **traduttore** tra mondi diversi: adatta linguaggio e contenuto allo stakeholder
- Ogni stakeholder ha **bisogni informativi diversi**: management vuole sintesi, engineering vuole dettagli
- **Comunica i problemi presto**: mai nascondere o aspettare che si risolvano da soli
- Usa **dati e fatti**, non opinioni o sensazioni
- La **gestione delle aspettative** è continua: sii realistico fin dall'inizio
- In crisi, **aumenta la frequenza** di comunicazione
- Il **silenzio è peggio** di cattive notizie comunicate bene
- **Timing e canale** sono importanti quanto il contenuto

---

**Prossimo capitolo**: [Errori classici del PM hardware](./08-errori-classici-del-pm.md)



