# Errori classici del PM hardware

## 🎬 Momento Serie TV
> *"È buffo quanto le nostre intuizioni possano essere sbagliate."* – J.D. (Scrubs)

Tutti facciamo errori. I PM più esperti ne hanno fatti tantissimi, la differenza è che hanno imparato a riconoscerli, evitarli e correggerli velocemente. Spesso pensiamo di fare la cosa giusta, di avere la situazione sotto controllo, di aver pianificato bene. Poi la realtà ci dimostra quanto le nostre intuizioni fossero sbagliate. Questo capitolo raccoglie gli errori più comuni dei PM hardware: se li riconosci in tempo, puoi evitarli. Se li hai già fatti, sappi che sei in buona compagnia.

---

## Errori di pianificazione

### 1. Sottostimare i lead time

**L'errore:** Pianificare ordini componenti senza considerare i lead time reali. "Il componente lo ordiniamo quando serve" senza verificare che servano 12 settimane per averlo.

**Perché succede:** Abitudine del software dove tutto è immediato. Mancanza di esperienza con supply chain hardware.

**Conseguenze:** Ritardi di settimane o mesi. Progetti bloccati in attesa di componenti. Costi aggiuntivi per shipping express.

**Come evitarlo:**
- Verifica lead time su Octopart/distributori prima di finalizzare il design
- Ordina componenti long-lead time con largo anticipo
- Aggiorna regolarmente i lead time: cambiano frequentemente
- Pianifica buffer del 20-30% per componenti critici

---

### 2. Pianificazione troppo ottimistica

**L'errore:** Fare piani basati sullo scenario migliore possibile: "Se tutto va perfettamente, finiamo in 6 mesi". Poi non va perfettamente.

**Perché succede:** Pressione da stakeholder per date aggressive. Inesperienza nel stimare attività hardware. Wishful thinking.

**Conseguenze:** Aspettative irrealistiche. Ritardi continui. Perdita di credibilità. Stress del team.

**Come evitarlo:**
- Usa stime PERT (ottimistica + pessimistica + probabile) / 6
- Pianifica almeno 2-3 cicli di prototipazione, non uno solo
- Aggiungi buffer di progetto (10-20% del tempo totale)
- Basa le stime su dati storici di progetti simili
- Coinvolgi il team nelle stime: chi fa il lavoro sa quanto serve

---

### 3. Non pianificare per i fallimenti

**L'errore:** Pianificare come se ogni prototipo funzionasse al primo colpo, ogni test passasse, ogni fornitore consegnasse in tempo.

**Perché succede:** Ottimismo eccessivo. Non voler "vendere" un piano con problemi inclusi.

**Conseguenze:** Quando (non se) qualcosa va storto, non hai piano B e vai nel panico.

**Come evitarlo:**
- Identifica rischi principali e pianifica contingency
- Includi tempo per debug e iterazioni
- Prevedi budget per ordini urgenti o rifabbricazioni
- Comunica agli stakeholder che gli imprevisti sono normali in hardware

---

### 4. Ignorare le dipendenze

**L'errore:** Pianificare task in parallelo che in realtà hanno dipendenze seriali. "Intanto che aspettiamo i PCB, facciamo il firmware" quando il firmware dipende dall'hardware funzionante.

**Perché succede:** Voglia di andare veloci. Non analizzare bene le dipendenze.

**Conseguenze:** Task bloccati. Risorse allocate su attività che non possono procedere. Rework.

**Come evitarlo:**
- Mappa tutte le dipendenze nel Gantt
- Identifica il critical path e monitoralo
- Verifica con il team quali task dipendono da altri
- Usa il tempo di waiting per attività preparatorie, non per lavoro che poi va rifatto

---

## Errori di comunicazione

### 5. Non comunicare i problemi presto

**L'errore:** Scoprire un problema e pensare "lo risolvo io prima che qualcuno se ne accorga". Poi il problema peggiora e diventa una crisi.

**Perché succede:** Paura di sembrare incompetente. Non voler allarmare. Speranza che si risolva da solo.

**Conseguenze:** Gli stakeholder vengono colti di sorpresa. Perdita di fiducia. Meno tempo per trovare soluzioni.

**Come evitarlo:**
- Comunica i problemi appena li identifichi
- Presenta problema + opzioni di soluzione + raccomandazione
- Meglio over-comunicare che under-comunicare
- La trasparenza costruisce fiducia, il silenzio la distrugge

---

### 6. Usare il linguaggio sbagliato con lo stakeholder sbagliato

**L'errore:** Spiegare al CEO i dettagli di impedenza della linea PCB. Dire al team engineering "dobbiamo andare più veloci" senza spiegare perché.

**Perché succede:** Non adattare la comunicazione al pubblico. Un solo modo di comunicare per tutti.

**Conseguenze:** Stakeholder confusi o annoiati. Decisioni prese su informazioni fraintese. Perdita di tempo.

**Come evitarlo:**
- Management vuole sintesi business: tempi, costi, rischi, decisioni
- Team tecnico vuole dettagli: specifiche, vincoli, motivazioni tecniche
- Adatta linguaggio, dettaglio e formato a chi hai di fronte
- Verifica comprensione: "Per essere sicuri di essere allineati..."

---

### 7. Non gestire le aspettative

**L'errore:** Promettere date ottimistiche per far contenti gli stakeholder. Non spiegare i vincoli. Far credere che tutto sia sotto controllo quando non lo è.

**Perché succede:** Voglia di compiacere. Paura di deludere. Pressione da management.

**Conseguenze:** Aspettative irrealistiche. Delusione quando la realtà emerge. Perdita di credibilità.

**Come evitarlo:**
- Sii realistico fin dall'inizio
- Spiega i vincoli (lead time, certificazioni, test necessari)
- Prometti meno, consegna di più
- Se le aspettative sono irrealistiche, sfidile con dati e fatti

---

## Errori tecnici e di design

### 8. Non coinvolgere la produzione abbastanza presto

**L'errore:** Design completato in isolamento, poi si passa alla produzione che dice "questo non è producibile" o "costerà il doppio così".

**Perché succede:** Silos organizzativi. Mentalità "prima progettiamo, poi produciamo".

**Conseguenze:** Design che richiede modifiche costose. Processi produttivi inefficienti. Resa bassa. Costi alti.

**Come evitarlo:**
- Design for Manufacturing (DFM) dal primo giorno
- Coinvolgi produzione nelle design review
- Fai DFMEA (Design Failure Mode and Effects Analysis)
- Pilot run prima della produzione serie per validare processi

---

### 9. Non validare le assunzioni

**L'errore:** Dare per scontato che un componente funzioni come da datasheet, che una tecnologia sia matura, che un fornitore sia affidabile. Senza verificare.

**Perché succede:** Fiducia eccessiva nei datasheet. Fretta di andare avanti. Non voler "perdere tempo" in verifiche.

**Conseguenze:** Scopri problemi tardi quando sono costosi da risolvere. Prototipi che non funzionano. Redesign.

**Come evitarlo:**
- Valida assunzioni critiche con POC (Proof of Concept)
- Testa componenti chiave su breadboard prima del design finale
- Verifica referenze dei fornitori
- Non dare mai nulla per scontato: "Trust but verify"

---

### 10. Cambiare troppo tra iterazioni

**L'errore:** Tra prototipo rev 1 e rev 2, cambiare 15 cose insieme. Poi rev 2 ha problemi e non sai quale delle 15 modifiche li ha causati.

**Perché succede:** Fretta di risolvere tutto insieme. Non documentare bene le modifiche.

**Conseguenze:** Impossibile fare root cause analysis. Rework multiplo. Sprechi.

**Come evitarlo:**
- Cambia una cosa alla volta quando possibile
- Se devi cambiare più cose, documentale tutte
- Testa sistematicamente per isolare problemi
- Usa change control anche sui prototipi

---

## Errori di gestione team e risorse

### 11. Micromanagement

**L'errore:** Controllare ogni minimo dettaglio del lavoro del team. Chiedere aggiornamenti continui. Non delegare.

**Perché succede:** Ansia di controllo. Non fidarsi del team. Paura che qualcosa vada storto.

**Conseguenze:** Team demotivato. Collo di bottiglia su di te. Burnout (tuo e del team). Rallentamento generale.

**Come evitarlo:**
- Delega con chiarezza: cosa, quando, criteri di successo
- Fidati del team: hai assunto persone competenti, lasciale lavorare
- Focalizzati su risultati, non su metodi
- Stand-up e check-in regolari sono sufficienti, non serve controllo continuo

---

### 12. Non proteggere il team dalle interruzioni

**L'errore:** Ogni richiesta urgente dagli stakeholder viene immediatamente passata al team. Cambio priorità continuo. Nessun filtro.

**Perché succede:** Voglia di rispondere subito a tutti. Non voler dire "no" agli stakeholder.

**Conseguenze:** Team costantemente interrotto. Lavoro frammentato. Niente si finisce. Frustrazione.

**Come evitarlo:**
- Tu sei il filtro tra stakeholder e team
- Valuta le richieste urgenti: sono davvero urgenti?
- Proteggi il focus del team su priorità concordate
- Dire "no" o "dopo" agli stakeholder è parte del tuo lavoro

---

### 13. Non celebrare i successi

**L'errore:** Il team lavora duro, raggiunge una milestone importante, e tu sei già proiettato sui prossimi problemi. Nessun riconoscimento.

**Perché succede:** Focus eccessivo su cosa manca ancora. Dare per scontato il buon lavoro.

**Conseguenze:** Team demotivato. Sensazione di non essere apprezzati. Burnout.

**Come evitarlo:**
- Celebra i successi, anche quelli intermedi
- Riconosci pubblicamente il buon lavoro
- Dopo una milestone, prenditi un momento per guardare indietro e apprezzare
- Un "grazie, ottimo lavoro" costa zero e vale tantissimo

---

## Errori di risk e change management

### 14. Non fare risk management

**L'errore:** "Pensiamo positivo, andrà tutto bene". Nessun risk register. Nessun piano B.

**Perché succede:** Ottimismo. Non voler sembrare pessimisti. Inesperienza.

**Conseguenze:** Quando i rischi si materializzano (e si materializzeranno), vai nel panico.

**Come evitarlo:**
- Identifica rischi fin dall'inizio
- Risk register aggiornato regolarmente
- Piano di contingenza per rischi ad alto impatto
- Risk management è realismo, non pessimismo

---

### 15. Accettare troppe change request

**L'errore:** Dire "sì" a ogni richiesta di modifica. "Aggiungiamo questa feature", "cambiamo questo componente", "facciamo anche quest'altra cosa".

**Perché succede:** Voglia di accontentare tutti. Non valutare l'impatto delle modifiche. Scope creep progressivo.

**Conseguenze:** Progetto che non finisce mai. Budget esploso. Timeline infinita. Prodotto che perde focus.

**Come evitarlo:**
- Ogni change request va valutata: costo, tempo, beneficio
- Dire "no" a modifiche non essenziali è OK
- Dopo design freeze, barra alta per accettare modifiche
- Usa change control formale per valutare impatti

---

## Errori di budget e costi

### 16. Sottostimare i costi

**L'errore:** Budget basato solo sul costo BOM, senza considerare: prototipi, tooling, certificazioni, scarto, rework, gestione, contingency.

**Perché succede:** Inesperienza. Pressione per mostrare ROI alto. Non conoscere i costi nascosti dell'hardware.

**Conseguenze:** Budget che esplode a metà progetto. Tagli al progetto. Stress finanziario.

**Come evitarlo:**
- Budget deve includere: BOM + prototipi (3-5 cicli) + tooling + certificazioni + test + scarto (5-10%) + contingency (15-20%)
- Chiedi a chi ha fatto progetti simili: quanto è costato davvero?
- Aggiorna budget regolarmente con consuntivo vs forecast
- Comunica extra-costi appena emergono, non a fine progetto

---

### 17. Non tracciare le spese

**L'errore:** Budget allocato all'inizio, poi nessuno traccia quanto si spende davvero. A fine progetto: sorpresa, abbiamo sforato del 40%.

**Perché succede:** Focus su tecnica, non su finance. Nessun sistema di tracking. "Qualcun altro lo sta tracciando".

**Conseguenze:** Scopri troppo tardi di aver finito i soldi. Difficoltà a giustificare extra-budget.

**Come evitarlo:**
- Traccia tutte le spese in tempo reale
- Report mensile: budget vs actual
- Forecasting: quanto spenderò ancora?
- Alert quando ti avvicini al budget limit

---

## 🎬 Momento Serie TV

> *"Dopo quello che era successo feci quello che avrebbe fatto qualsiasi brava persona: andai in cerca di conferme che non era colpa mia."* – J.D. (Scrubs)

Questo è l'errore più umano: quando qualcosa va storto, la prima reazione è cercare giustificazioni esterne. "È colpa del fornitore", "Non mi hanno dato le risorse", "I requisiti erano poco chiari". A volte è vero ma spesso c'è anche una nostra responsabilità. Il PM maturo si chiede: cosa potevo fare diversamente? Cosa posso imparare? Come evito di ripetere l'errore?

---

## Come imparare dagli errori

Gli errori non sono fallimenti se ci insegna qualcosa. Ecco come trasformare gli errori in opportunità di crescita.

### 1. Riconosci l'errore

Il primo passo è ammettere che hai sbagliato. Non giustificare, non minimizzare, non dare la colpa ad altri. "Ho sottostimato i lead time", "Non ho comunicato il rischio abbastanza presto", "Ho accettato troppi cambiamenti senza valutare l'impatto".

### 2. Analizza la root cause

Perché è successo? Non fermarti alla causa superficiale. Usa i "5 Perché":
- Il progetto è in ritardo. Perché?
- Perché i componenti sono arrivati tardi. Perché?
- Perché non li abbiamo ordinati in tempo. Perché?
- Perché non conoscevamo i lead time reali. Perché?
- Perché non abbiamo verificato con i fornitori prima di pianificare.

Root cause: mancanza di verifica lead time in fase di pianificazione.

### 3. Definisci azioni correttive

Cosa fai diversamente la prossima volta?
- Verifico lead time con fornitori prima di finalizzare il piano
- Aggiungo buffer del 20% per componenti long-lead time
- Creo checklist di verifica per pianificazione progetti

### 4. Documenta e condividi

Scrivi una breve lessons learned:
- Cosa è successo
- Root cause
- Cosa abbiamo fatto per risolvere
- Cosa faremo diversamente

Condividi con il team e l'organizzazione. Gli errori documentati diventano asset: altri possono imparare senza rifarli.

### 5. Retrospettive regolari

Dopo ogni fase importante (prototipo, NPI, lancio), fai retrospettiva:
- Cosa ha funzionato bene?
- Cosa non ha funzionato?
- Cosa possiamo migliorare?

Ambiente safe: no blame, focus sul miglioramento. Se qualcuno ha paura di ammettere errori, non imparerete mai.

---

## 💡 Concetto chiave

**I PM migliori non sono quelli che non fanno errori ma quelli che li riconoscono velocemente, li correggono, e non li ripetono.** L'errore occasionale è normale. L'errore ripetuto è negligenza.

---

## Checklist anti-errore per PM hardware

Usa questa checklist per evitare gli errori più comuni:

### Pianificazione
- [ ] Ho verificato i lead time di tutti i componenti critici?
- [ ] Ho pianificato almeno 2-3 cicli di prototipazione?
- [ ] Ho aggiunto buffer di progetto (10-20%)?
- [ ] Ho identificato il critical path?
- [ ] Ho coinvolto il team nelle stime?

### Risk Management
- [ ] Ho un risk register aggiornato?
- [ ] Ho identificato i top 5 rischi del progetto?
- [ ] Ho piano di contingenza per rischi ad alto impatto?
- [ ] Rivedo i rischi almeno ogni 2 settimane?

### Comunicazione
- [ ] Gli stakeholder conoscono lo stato reale del progetto?
- [ ] Ho comunicato i problemi appena identificati?
- [ ] Adatto la comunicazione al pubblico?
- [ ] Ho gestito le aspettative in modo realistico?

### Design e Tecnica
- [ ] Ho coinvolto produzione nelle design review?
- [ ] Ho validato le assunzioni critiche?
- [ ] Ho fatto DFM (Design for Manufacturing)?
- [ ] Ho tracciato tutte le modifiche al design?

### Budget
- [ ] Sto tracciando tutte le spese?
- [ ] Il budget include: BOM + prototipi + tooling + certificazioni + contingency?
- [ ] Faccio forecast regolari?
- [ ] Comunico extra-costi appena emergono?

### Team
- [ ] Sto delegando o sto facendo micromanagement?
- [ ] Proteggo il team dalle interruzioni continue?
- [ ] Celebro i successi del team?
- [ ] Il team si sente supportato?

---

## Storie di errori reali (e cosa hanno insegnato)

### Caso 1: Il componente fantasma

**Cosa è successo:** PM pianifica progetto con componente perfetto sulla carta. A metà sviluppo, scopre che il componente ha 26 settimane di lead time e solo un fornitore al mondo. Progetto bloccato.

**Root cause:** Scelto componente senza verificare supply chain.

**Lezione:** Verifica disponibilità, lead time e multi-sourcing PRIMA di basare il design su un componente.

### Caso 2: Il prototipo perfetto (sulla carta)

**Cosa è successo:** Design review perfetta, tutti d'accordo. Primo prototipo assemblato: non si accende nemmeno. Problema di alimentazione evidente che nessuno aveva notato.

**Root cause:** Design review fatta solo a livello alto, senza check di dettagli critici.

**Lezione:** Design review deve includere verifica dettagliata di: power, grounding, EMC, thermal. Non solo funzionalità.

### Caso 3: La certificazione sorpresa

**Cosa è successo:** Prodotto quasi pronto per produzione. Cliente chiede: "Avete la certificazione X?". PM: "Quale certificazione?". Quella obbligatoria per legge per quel mercato. 6 mesi di ritardo per certificare.

**Root cause:** Requisiti normativi non identificati all'inizio.

**Lezione:** Coinvolgi esperti normativi in fase di concept. Le certificazioni vanno pianificate, non scoperte.

### Caso 4: Lo scope creep silenzioso

**Cosa è successo:** Progetto parte con 10 feature. Durante sviluppo, stakeholder propongono "piccole aggiunte". PM accetta sempre. A metà progetto: 23 feature, budget esploso, timeline raddoppiata.

**Root cause:** Nessun change control. Incapacità di dire "no".

**Lezione:** Ogni modifica va valutata formalmente. Dire "no" a feature non essenziali protegge il progetto.

---

## L'errore più grande: non ammettere di non sapere

C'è un errore che sta alla base di molti altri: **la paura di dire "non lo so"**.

Il PM junior pensa di dover avere tutte le risposte. Quando non sa qualcosa, improvvisa, fa finta di sapere, o peggio, decide senza informazioni.

Il PM senior sa dire: "Non lo so ma scoprirò". E poi chiede agli esperti, fa ricerca, consulta chi ha più esperienza.

**Nessuno sa tutto.** L'hardware è complesso, ogni progetto ha specificità, il mercato cambia continuamente. Non sapere qualcosa non è un difetto, è normale. Non chiede aiuto quando serve è un difetto.

---

## 🎬 Momento Serie TV

> *"Il meglio che si possa sperare è di aver imparato qualcosa. Qualunque cosa. Anche di poco conto."* – J.D. (Scrubs)

Fare il PM hardware significa affrontare problemi nuovi, tecnologie in evoluzione, situazioni impreviste. Non uscirai da un progetto senza errori. Ma se esci avendo imparato qualcosa - anche una piccola lezione su lead time, su come comunicare meglio, su come gestire un fornitore difficile - allora non è stato tempo sprecato. Gli errori sono tuition fees per l'esperienza. Pagali, impara, e diventa un PM migliore.

---

## 🧠 Cosa deve ricordare un PM

- **Tutti fanno errori**: l'importante è riconoscerli presto e imparare
- Gli errori più comuni: **sottostimare lead time, pianificazione ottimistica, non comunicare problemi presto**
- **Coinvolgi produzione presto**: DFM dal primo giorno
- **Valida le assunzioni critiche**: non dare nulla per scontato
- Usa **change control**: non accettare tutte le modifiche
- **Traccia budget e tempi** regolarmente: no sorprese a fine progetto
- **Proteggi il team** da interruzioni e micromanagement
- **Ammetti quando non sai**: chiedi aiuto, è segno di maturità non di debolezza
- Fai **retrospettive** e documenta **lessons learned**
- Il miglior PM non è chi non sbaglia, è chi **impara e non ripete gli errori**

---

**Fine della guida!** Ora hai gli strumenti per fare il PM hardware con competenza, pragmatismo e un pizzico di sana ironia. Ricorda: **Dai, dai, dai!** 🚀
