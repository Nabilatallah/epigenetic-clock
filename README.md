# Interpretable Epigenetic Clock for Biological Age Prediction Using DNA Methylation Data

## Project Overview

Developed an interpretable machine learning pipeline for biological age prediction using genome-wide DNA methylation profiles from the publicly available GSE40279 cohort.

This project integrates epigenomics, machine learning, explainable AI (XAI), and pathway enrichment analysis to construct a scalable epigenetic clock capable of identifying aging-associated CpG biomarkers and biologically relevant aging pathways.

The workflow was designed with emphasis on:

- Reproducibility
- Model interpretability
- Translational bioinformatics
- HPC scalability
- Precision medicine applications

---

## Key Highlights

- Built an end-to-end epigenetic clock pipeline using ~473K CpG methylation features
- Trained and benchmarked multiple machine learning models including:
  - ElasticNet
  - Random Forest
  - XGBoost
- Identified XGBoost as the top-performing predictive model
- Applied SHAP explainability to identify high-impact aging-associated CpG sites
- Performed functional enrichment analysis using:
  - KEGG
  - Gene Ontology (GO)
  - GenAge
  - Enrichr
- Identified biologically relevant pathways including:
  - DNA damage repair
  - Telomere maintenance
  - Oxidative stress response
  - Cell cycle regulation
- Developed a modular and reproducible HPC-compatible workflow using Apptainer and SLURM-ready execution

---

## Technical Objectives

| Objective | Description |
|---|---|
| Data Preprocessing | Process and align high-dimensional methylation and phenotype data |
| Predictive Modeling | Train machine learning models to estimate chronological age |
| Explainable AI | Interpret model predictions using SHAP feature attribution |
| Functional Annotation | Map CpGs to genes and genomic regulatory regions |
| Pathway Analysis | Identify enriched aging-associated pathways and biological processes |
| Reproducibility | Develop scalable and modular workflows for HPC environments |

---

## Dataset

| Attribute | Details |
|---|---|
| Dataset | GEO: GSE40279 |
| Platform | Illumina HumanMethylation450K BeadChip |
| Samples | 656 blood-derived methylation profiles |
| Feature Space | ~473,034 CpG loci |
| Age Range | 19–101 years |

---

## Pipeline Architecture

### 1. Data Acquisition & Parsing
- Downloaded and processed GEO SOFT files using `GEOparse`
- Extracted beta methylation matrices and age metadata

### 2. Data Harmonization
- Aligned methylation matrices with phenotype labels
- Organized outputs into reproducible directory structures

### 3. Machine Learning Modeling
Implemented and benchmarked multiple regression models:

- ElasticNet
- Random Forest Regressor
- XGBoost Regressor

### 4. Model Evaluation
Compared model performance using:

- Mean Absolute Error (MAE)
- R² score
- Cross-validation metrics

### 5. Explainable AI (XAI)
- Applied SHAP (SHapley Additive exPlanations) to quantify feature importance
- Visualized top CpGs contributing to biological age prediction
- Generated interpretable methylation signatures associated with aging

### 6. Functional Genomic Annotation
- Annotated CpGs using Illumina 450K manifests
- Linked methylation sites to:
  - Genes
  - CpG islands
  - Regulatory regions

### 7. Pathway & Enrichment Analysis
Performed downstream systems biology analysis using:

- KEGG
- GO Biological Process
- GenAge
- Enrichr

### 8. Automation & HPC Integration
- Automated logging and reporting pipelines
- Built workflows compatible with:
  - SLURM clusters
  - Apptainer containers
  - HPC execution environments

---

## Results & Biological Insights

| Analysis | Outcome |
|---|---|
| Methylation Matrix | 656 samples × ~473K CpGs |
| Best Performing Model | XGBoost |
| Top Aging Biomarkers | `ELOVL2`, `FHL2`, and additional age-associated CpGs |
| Explainability | SHAP identified high-impact methylation signatures driving predictions |
| Enriched Pathways | DNA repair, telomere biology, oxidative stress, and cell-cycle regulation |
| Translational Insight | Detected biological age acceleration patterns associated with potential health-related variability |

### Notable Findings

- Several top-ranked CpGs mapped to well-established aging biomarkers
- Enrichment analyses revealed strong association with canonical hallmarks of aging
- SHAP analysis enabled biologically interpretable feature attribution rather than black-box prediction

---

## Tech Stack

### Programming Languages
- Python
- R
- Bash

### Machine Learning & Data Science
- scikit-learn
- XGBoost
- pandas
- NumPy
- SHAP

### Visualization
- matplotlib
- seaborn

### Bioinformatics & Enrichment
- GEOparse
- Enrichr
- GenAge
- GO
- KEGG

### Infrastructure
- Explorer HPC
- Apptainer
- SLURM workflows

---

## Reproducibility & Engineering Practices

- Modularized project architecture
- Version-controlled analysis workflows
- Automated runtime and output logging
- Reproducible HPC-ready execution
- Containerized computational environment
- Scalable pipeline design for large methylation cohorts

---

## Future Directions

| Direction | Research Impact |
|---|---|
| External Cohort Validation | Improve model generalizability across populations |
| Sex-Specific Epigenetic Clocks | Investigate sex-driven aging dynamics |
| Multi-Omics Integration | Integrate transcriptomics and proteomics with methylation data |
| Deep Learning Explainability | Compare SHAP with LIME, DALEX, and DeepSHAP |
| Clinical Translation | Explore biomarker applications in precision medicine and aging therapeutics |

---

## Research & Industry Relevance

This project demonstrates practical expertise in:

- Machine learning for biomedical data
- Explainable AI in healthcare
- Epigenomics and aging biology
- High-dimensional omics analysis
- Reproducible computational biology
- HPC-enabled bioinformatics workflows
- Translational precision medicine

Applications include:

- Biomarker discovery
- Longevity research
- Clinical bioinformatics
- Precision medicine workflows
- AI-driven healthcare analytics

---

## Conclusion

This project delivers a scalable and interpretable epigenetic clock framework that combines machine learning, explainable AI, and systems biology to model biological aging from genome-wide methylation data.

The workflow demonstrates how interpretable AI methods can support biomarker discovery and translational aging research through reproducible and HPC-ready bioinformatics pipelines.

---

## Author

**Nabil Atallah, Ph.D**  
📧 Nabilatallah@hotmail.com
