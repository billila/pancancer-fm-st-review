# Protocollo della Systematic Review

## Domanda di ricerca

Quali foundation model sono stati sviluppati per integrare istopatologia (whole-slide image) e spatial transcriptomics, con quali architetture/dati di pretraining, e con quali performance su quali task?

## Framework PICOS

- **Population/dato**: coppie immagine istologica + dato di spatial transcriptomics, qualsiasi piattaforma (Visium, Visium HD, Xenium, Slide-seq, MERSCOPE, CosMx, Stereo-seq), tessuto umano o murino
- **Intervention/metodo**: un foundation model — pre-addestrato su larga scala, self-supervised o multimodale, generalizzabile oltre un singolo dataset/organo — usato per predire, integrare o allineare imaging e trascrittomica spaziale
- **Comparator**: altri foundation model, metodi classici di deconvoluzione/predizione, o nessuno (studi puramente metodologici)
- **Outcome**: metriche riportate — correlazione per gene (Pearson/Spearman), AUC, C-index, ARI/NMI per clustering di domini spaziali, accuratezza di deconvoluzione cellulare
- **Study design**: paper metodologici di sviluppo/validazione, inclusi preprint (bioRxiv/medRxiv/arXiv)

## Criteri di inclusione

1. Presenta un metodo che integra esplicitamente immagini istologiche e dati ST tramite un modello con componente foundation (pretraining ampio, non solo un modello supervisionato addestrato da zero su un singolo dataset)
2. Riporta almeno una valutazione quantitativa
3. Full text disponibile in inglese
4. Pubblicato/pre-pubblicato dal 2022 alla data della ricerca (settembre 2026)
5. Tessuto umano o murino, entrambi inclusi

Nota: gli studi pre-2022 concettualmente affini (es. HE2RNA, DeepSpaCE, ST-Net) sono trattati come "pre-FM baseline" storici in tabella, distinti dai veri foundation model, non come inclusioni piene.

## Criteri di esclusione

1. Metodi che usano ST solo come validazione downstream senza foundation model per l'imaging (es. deconvoluzione classica tipo cell2location, SPOTlight, senza backbone pretrained)
2. Review, commentari, editoriali (tenuti da parte per la sezione narrativa/discussione, non nell'estrazione sistematica)
3. Solo proof-of-concept qualitativo, nessuna metrica quantitativa riportata
4. Non in lingua inglese
5. Solo abstract disponibile, nessun full text reperibile

## Screening

Doppia lettura indipendente (titolo/abstract, poi full text), gestita su Rayyan in modalità blind. Disaccordi risolti per consenso o terzo revisore. Accordo inter-rater misurato con Cohen's κ (target: κ > 0.6).

Fasi:
1. Raccolta e deduplica
2. Screening titolo/abstract (Include / Exclude / Maybe)
3. Risoluzione conflitti
4. Screening full text, con motivo di esclusione annotato per ogni escluso
5. Diagramma di flusso PRISMA finale

## Estrazione dati (per studio incluso)

Tipo tumorale, pan-cancer sì/no, N campioni/slide, piattaforma ST, architettura del foundation model, dataset/dimensione di pretraining, task valutati, metrica, confronto con baseline, disponibilità del codice.

## Secondo revisore

Da individuare (nota aperta al 2026-09-10).
