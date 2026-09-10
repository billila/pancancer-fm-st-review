# Backbone foundation models (fuori scope per l'inclusione in Sezione A)

Questi sono foundation model general-purpose di patologia (non metodi FM+ST): non soddisfano il criterio di inclusione "integra esplicitamente istologia e spatial transcriptomics", quindi non vengono screenati nella systematic review. Restano però un riferimento importante perché spesso usati come encoder/backbone dentro i metodi FM+ST inclusi, e sono centrali per la Sezione B (interpretabilità).

| Modello | Paper | Anno | Note |
|---|---|---|---|
| UNI | Chen et al., "Towards a general-purpose foundation model for computational pathology", Nature Medicine | 2024 | Pretrained su >100M immagini da >100.000 WSI H&E, 20 tessuti; valutato su 34 task CPath |
| CONCH | Lu et al., "A visual-language foundation model for computational pathology", Nature Medicine | 2024 | Modello visual-language (immagine + testo) |
| Prov-GigaPath | Xu et al., "A whole-slide foundation model for digital pathology from real-world data", Nature | 2024 | Usato internamente nel lavoro di Ilaria su TCGA-OV/HiST pipeline |
| Virchow | Vorontsov et al., "Virchow: a million-slide digital pathology foundation model" | 2024 | Backbone usato da PICASSO per l'atlante pan-cancer di concetti istomorfologici |

## Nota d'uso

Quando si estraggono i dati dai paper inclusi in Sezione A, annotare in tabella quale di questi backbone (se presente) viene usato come encoder — utile per capire se la performance riportata dipende più dal backbone o dal metodo di integrazione ST proposto.
