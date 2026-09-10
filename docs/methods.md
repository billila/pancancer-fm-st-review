# Methods

> Draft — written in manuscript-ready prose, to be refined during writing. Follows PRISMA 2020 reporting structure. Section numbers/subheadings can be adapted to target journal format.

## Search strategy and information sources

We conducted a systematic search across four databases — PubMed, Scopus, Europe PMC, and arXiv — to identify studies describing foundation model-based methods for integrating histopathology whole-slide imaging with spatial transcriptomics (ST) data. Europe PMC was used as the primary source for preprint literature, as it indexes bioRxiv and medRxiv alongside peer-reviewed records; a dedicated bioRxiv search was therefore not performed separately, avoiding redundant retrieval (24 of 40 Europe PMC records were preprints from these servers). The search covered publications from January 1, 2022 to September 10, 2026, reflecting the emergence of the first self-supervised pathology foundation models in this period.

The core search string combined three concept blocks — (i) foundation model/self-supervised terminology, (ii) spatial transcriptomics platforms and terminology, and (iii) histopathology/imaging terminology — connected by Boolean AND, with synonyms within each block connected by OR:

```
("foundation model" OR "self-supervised" OR "pretrained model" OR "pre-trained model")
AND
("spatial transcriptomics" OR Visium OR Xenium OR "spatial omics" OR "Slide-seq" OR MERSCOPE OR CosMx OR "Stereo-seq")
AND
(histology OR "H&E" OR "whole slide image" OR "whole-slide image" OR pathology OR histopathology)
```

This string was adapted to the syntax of each database (title/abstract field tags for PubMed and Europe PMC, `TITLE-ABS-KEY` for Scopus). For arXiv, whose advanced search interface does not reliably parse nested Boolean expressions with multiple synonyms, the query was decomposed into simpler paired searches (e.g., `"spatial transcriptomics" AND "foundation model"`, `"spatial transcriptomics" AND "self-supervised"`) restricted to the q-bio, eess, and cs (cross-listed) categories.

## Study records and data management

Records were exported from each database (NBIB format from PubMed, RIS from Scopus and Europe PMC, BibTeX from arXiv) and imported into Rayyan (rayyan.ai) for deduplication and screening. Automated duplicate detection was followed by manual confirmation of each candidate pair.

## Eligibility criteria

Eligibility was defined using a PICOS framework. Studies were included if they: (1) presented a method explicitly integrating histopathology images and ST data using a model with a foundation-model component (i.e., pretrained at scale, not a supervised model trained from scratch on a single dataset); (2) reported at least one quantitative evaluation; (3) were available in full text in English; (4) were published or preprinted between January 2022 and the search date; (5) used human or murine tissue (both included).

Studies were excluded if they: (1) used ST data solely as downstream validation without a foundation-model component for image encoding (e.g., classical deconvolution methods such as cell2location or SPOTlight applied without a pretrained backbone); (2) were reviews, commentaries, or editorials (these were retained separately to inform the discussion, but not included in systematic data extraction); (3) reported only qualitative proof-of-concept results without quantitative metrics; (4) were not available in English; (5) had no retrievable full text.

General-purpose pathology foundation models not evaluated on an ST-related task in their original publication (e.g., UNI, CONCH, Prov-GigaPath, Virchow) were not eligible as primary inclusions, but are tracked separately as reference backbone models (see `backbone-models.md`), as they are frequently used as encoders within eligible studies.

## Screening process

Screening was conducted in two stages. In the first stage, two reviewers independently screened titles and abstracts against the eligibility criteria above, blinded to each other's decisions, using Rayyan's blind review mode. Conflicts were resolved by discussion and consensus, with a third reviewer available for unresolved disagreements. Inter-rater agreement was quantified using Cohen's κ. In the second stage, full texts of records retained after title/abstract screening were independently assessed by the same two reviewers against the full eligibility criteria, with reasons for exclusion recorded for each excluded study. A PRISMA flow diagram summarizing the study selection process was generated from the resulting counts.

## Data extraction

For each included study, the following data were extracted: tumor type(s) studied and whether the analysis was pan-cancer; sample size (number of patients/slides); ST platform(s) used; foundation model architecture and backbone (if applicable); pretraining dataset and its size; evaluation task(s) and reported metric(s); comparison against baseline methods; and code/data availability.
