# Systematic Review: Foundation Models per l'integrazione Histopathology + Spatial Transcriptomics

## Panoramica

Systematic review che mappa i metodi basati su foundation model per l'integrazione di immagini istopatologiche (whole-slide image) e dati di spatial transcriptomics (uomo e topo, dal 2022 a oggi). Vengono caratterizzati architettura del modello, dataset di pretraining, task di valutazione e metriche di performance riportate, per valutarne la comparabilità.

Questo repo nasce come sezione sistematica (Sezione A) di un lavoro più ampio di review sui foundation model in patologia computazionale pan-cancer, che include anche una sezione narrativa sull'interpretabilità degli embedding (Sezione B) — vedi `docs/scope-note.md`.

## Stato del progetto

- [x] Definizione domanda di ricerca e framework PICOS
- [x] Definizione criteri di inclusione/esclusione
- [x] Ricerca su PubMed, Scopus, Europe PMC, arXiv
- [x] Import e deduplica su Rayyan
- [ ] Screening titolo/abstract (in corso)
- [ ] Secondo revisore da individuare
- [ ] Screening full text
- [ ] Estrazione dati
- [ ] Diagramma di flusso PRISMA
- [ ] Stesura

## Struttura del repo

- `docs/protocol.md` — domanda di ricerca, PICOS, criteri di inclusione/esclusione
- `docs/search-log.md` — stringhe di ricerca per database, date, numero di risultati
- `docs/scope-note.md` — come questa sezione si inquadra nella review più ampia
- `data/exports/` — file di export grezzi dai database (RIS/BibTeX/NBIB)
- `screening/` — link al progetto Rayyan e note di screening

## Review management

Screening e deduplica gestiti su [Rayyan](https://rayyan.ai) — progetto "foundation models" (biomedical, Systematic Review).

## Autrice

Ilaria Billato, Università di Padova
