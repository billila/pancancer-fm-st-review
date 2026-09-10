# Inquadramento nella review più ampia

Questa systematic review (mappatura dei metodi foundation model per l'integrazione histopathology + spatial transcriptomics) è la **Sezione A** di un progetto di review più ampio su foundation model in patologia computazionale, in ottica pan-cancer.

## Struttura complessiva prevista

- **Sezione A (sistematica, PRISMA — questo repo)**: mappatura dei metodi FM+ST — architettura, dataset di pretraining, task, performance, confrontabilità
- **Sezione B (narrativa)**: cosa "vedono" i foundation model — sintesi dei lavori di interpretabilità/decomposizione degli embedding (es. PICASSO — atlante pan-cancer di concetti istomorfologici da sparse dictionary learning; confronto tra embedding e feature handcrafted classiche tipo dimensione/eccentricità dei nuclei; representational similarity analysis tra modelli diversi)
- **Sezione C (discussione/ponte)**: dove le due cose si incontrano — l'interpretabilità aiuta a capire perché un modello FM+ST funziona meglio di un modello di deconvoluzione classico

## Razionale della scelta di scope

Una review generalista sui foundation model di patologia è già ampiamente coperta in letteratura recente (2025-2026: PMC, Komura et al. CSBJ, JMA Journal, survey Springer, Mayo Clinic Proceedings). L'angolo FM+spatial transcriptomics + interpretabilità/validità (assi 2 e 3 del brainstorming iniziale) risulta invece meno saturato e più vicino al lavoro di ricerca già in corso (Visium HD, TCGA pan-cancer, imageTCGA).

Gli assi "standardizzazione input" e "risorse computazionali" restano come tabelle di supporto/metodologia dentro la Sezione A, non come sezioni-risultato a sé stanti. L'asse "dati longitudinali" è probabilmente troppo scarso in letteratura per una sezione propria a questo stadio — da rivalutare dopo lo screening completo.
