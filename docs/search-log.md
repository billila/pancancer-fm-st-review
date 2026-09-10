# Search Log

Ultimo aggiornamento: 2026-09-10

## Stringa di base (logica comune)

```
("foundation model" OR "self-supervised" OR "pretrained model" OR "pre-trained model")
AND
("spatial transcriptomics" OR Visium OR Xenium OR "spatial omics" OR "Slide-seq" OR MERSCOPE OR CosMx OR "Stereo-seq")
AND
(histology OR "H&E" OR "whole slide image" OR "whole-slide image" OR pathology OR histopathology)
```

Filtro temporale: 2022-01-01 → presente (2026-09-10).

## Risultati per fonte

| Database | Data ricerca | Query | Risultati grezzi | File export | Note |
|---|---|---|---|---|---|
| PubMed | 2026-09-10 | vedi sopra, con tag `[tiab]`, filtro data 2022–presente | 26 | `data/exports/pubmed_2026-09-10.nbib` | — |
| Scopus | 2026-09-10 | vedi sopra, sintassi `TITLE-ABS-KEY`, `PUBYEAR > 2021` | 69 | `data/exports/scopus_2026-09-10.ris` | Prima esportazione senza campo Abstract, ri-esportata correggendo (v2) |
| Europe PMC | 2026-09-10 | vedi sopra, sintassi `TITLE:`/`ABSTRACT:`, `PUB_YEAR` | 40 | `data/exports/europepmc_2026-09-10.ris` | Include bioRxiv/medRxiv: 24/40 risultati sono preprint (fonte "PPR"). Nessuna ricerca separata su bioRxiv necessaria. |
| arXiv (ricerca A) | 2026-09-10 | `"spatial transcriptomics"` AND `"foundation model"`, campo Abstract, categorie q-bio/eess/cs, 2022–presente | 14 | `data/exports/arxiv_2026-09-10.bib` | Export manuale (bibtex per singolo paper, senza campo abstract) |
| arXiv (ricerca B) | 2026-09-10 | `"spatial transcriptomics"` AND `"self-supervised"`, stessi filtri | 0 | — | Nessun risultato; copertura comunque garantita da Scopus/Europe PMC |

**Totale record grezzi importati in Rayyan: 149**

## Deduplica (Rayyan)

- Record importati: 149
- Duplicati rilevati: 65
- Duplicati confermati ed eliminati: 42
- **Record unici per lo screening: 107**

## Problemi noti e risoluzioni

- **arXiv bibtex senza abstract**: l'export "bibtex citation" di arXiv non include il campo abstract di default → per i 14 record servirà integrazione manuale dell'abstract in Rayyan prima/durante lo screening.
- **Scopus export iniziale senza abstract**: 50 record risultavano senza abstract su Rayyan dopo il primo import — causa: casella "Abstract" non selezionata nel dialog di export RIS di Scopus. Risoluzione: ri-esportare con "Abstract" esplicitamente spuntato, sostituire i record (eliminare i 50 vecchi, ricaricare il nuovo file, ri-deduplicare).
