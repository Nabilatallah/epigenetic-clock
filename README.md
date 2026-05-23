# Development and Interpretation of an Epigenetic Clock Using DNA Methylation Data from GSE40279

## Project Overview

This project focuses on building and interpreting a machine learning–based epigenetic clock using the publicly available GSE40279 methylation dataset. An epigenetic clock estimates biological age by analyzing methylation levels at CpG sites across the genome.

The primary objective was to:

- Develop a predictive aging model
- Identify biologically meaningful CpGs associated with aging
- Explore enrichment in known age-related pathways

---

## Objectives

| Goal | Description |
|---|---|
| 1 | Preprocess DNA methylation and age data from GSE40279 |
| 2 | Train machine learning models to predict chronological age |
| 3 | Interpret model predictions using SHAP values |
| 4 | Annotate top-ranked CpGs to genes and functional regions |
| 5 | Conduct pathway enrichment analysis using GenAge and KEGG |
| 6 | Compare model performance and interpretability |

---

## Methodology

### Dataset

- **Source:** GEO accession GSE40279
- **Samples:** 656 blood samples
- **Platform:** Illumina HumanMethylation450K BeadChip
- **Age Range:** 19–101 years

---

## Pipeline Stages

| Stage | Description |
|---|---|
| 1. Data Extraction | Downloaded and parsed SOFT files using GEOparse. Extracted beta values and age metadata. |
| 2. Alignment | Aligned beta matrix and age labels; saved outputs to structured directories (`data_dir`, `results_dir`). |
| 3. Model Training | Trained models including ElasticNet, Random Forest, and XGBoost. |
| 4. Model Evaluation | Compared Mean Absolute Error (MAE) and R² across models. |
| 5. Feature Importance | Applied SHAP to extract and visualize influential CpGs. |
| 6. Annotation | Mapped top CpGs to genes and genomic coordinates using the Illumina 450K manifest. |
| 7. Enrichment | Conducted pathway enrichment using Enrichr, GenAge, GO Biological Process, and KEGG. |
| 8. Logging & Reporting | Automated logging of runtime, matrix dimensions, and output paths. |

---

## Results

| Task | Output |
|---|---|
| Aligned Beta Matrix | 656 samples × ~473,034 CpGs |
| Best Model (MAE) | *[Insert best model and MAE]* |
| Top CpGs Identified | `cg16867657 (ELOVL2)`, `cg22454769 (FHL2)`, etc. |
| Enriched Pathways | DNA damage response, telomere maintenance, cell cycle regulation |
| SHAP Interpretation | Visualized top 100 CpGs driving age prediction |

---

## Biological Insights

- Several top CpGs mapped to well-established aging genes.
- Enriched pathways included:
  - Cell cycle regulation
  - DNA repair
  - Oxidative stress response
- Age acceleration analysis identified biological age outliers potentially linked to health status.

---

## Tools & Technologies

### Languages
- Python 3
- R
- Bash

### Libraries
- GEOparse
- pandas
- scikit-learn
- shap
- matplotlib
- joblib

### Platforms
- Explorer HPC
- Apptainer containerization

### Enrichment Tools
- Enrichr
- GenAge
- GO
- KEGG

---

## Future Directions

| Direction | Rationale |
|---|---|
| Validate on external cohorts | Assess generalizability |
| Build sex-specific clocks | Explore differential aging by gender |
| Extend to multi-omics integration | Link methylation to gene expression or proteomics |
| Deep learning interpretability | Compare SHAP with LIME, DALEX, and DeepSHAP |

---

## Repository & Reproducibility

- All code is modularized and documented.
- Logs are saved per module.
- Compatible with containerized and SLURM-based HPC workflows.

---

## Conclusion

This project successfully constructs an epigenetic clock using public methylation data, demonstrates interpretability through SHAP analysis, and derives biological insights via pathway enrichment.

The workflow provides a scalable and reproducible framework for precision aging research and lays the foundation for future biomarker discovery and therapeutic targeting.

---

## Author

**Nabil Atallah, Ph.D**  
📧 Nabilatallah@hotmail.com
