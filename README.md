# 🧬 Comparative ATAC-seq Analysis of Alzheimer's Disease and Medulloblastoma Microglia

## Project Overview

This repository contains a comparative ATAC-seq analysis pipeline designed to identify shared chromatin accessibility patterns between **Alzheimer's Disease (AD)** and **Medulloblastoma (MB)** microglia. The workflow integrates quality control, read alignment, peak calling, differential binding analysis, peak annotation, and motif enrichment to investigate common epigenetic regulatory mechanisms.

---

## Objectives

* Perform quality assessment of ATAC-seq sequencing data.
* Align sequencing reads to the human reference genome (GRCh38).
* Process and filter aligned reads.
* Identify accessible chromatin regions using MACS2.
* Perform differential chromatin accessibility analysis using DiffBind and DESeq2.
* Identify shared chromatin regions between AD and MB.
* Annotate genomic regions using HOMER.
* Perform transcription factor motif enrichment analysis.
* Visualize and interpret the biological significance of the results.

---

## Workflow

```text
Raw FASTQ Files
        │
        ▼
Quality Control (FastQC)
        │
        ▼
Read Alignment (BWA)
        │
        ▼
SAM → BAM Conversion
        │
        ▼
Sorting & Indexing (SAMtools)
        │
        ▼
PCR Duplicate Removal
        │
        ▼
Merge Biological Replicates
        │
        ▼
Peak Calling (MACS2)
        │
        ▼
Differential Binding Analysis (DiffBind + DESeq2)
        │
        ▼
Shared Peak Identification (BEDTools)
        │
        ▼
Peak Annotation (HOMER)
        │
        ▼
Motif Enrichment Analysis
        │
        ▼
Promoter Analysis & Visualization
```

---

## Software and Tools

| Software | Purpose |
|----------|---------|
| Ubuntu Linux | Operating system |
| Cell Ranger ATAC | Reference preparation |
| FastQC | Quality control |
| BWA | Read alignment |
| SAMtools | BAM processing |
| BEDTools | Genomic interval operations |
| MACS2 | Peak calling |
| HOMER | Peak annotation and motif analysis |
| R | Statistical analysis |
| DiffBind | Differential accessibility analysis |
| DESeq2 | Differential analysis |
| Python | Functional enrichment analysis |
| Jupyter Notebook | Interactive analysis environment |

### Software Versions

| Software | Version |
|----------|---------|
| Ubuntu Linux | 25.04 (Plucky Puffin) |
| SRA Toolkit | 3.2.1 |
| FastQC | 0.12.1 |
| BWA-MEM | 0.7.18-r1243 |
| SAMtools | 1.21 |
| BEDTools | 2.31.1 |
| MACS2 | 2.2.9.1 |
| HOMER | 4.x |
| R | 4.5.3 |
| DiffBind | 3.20.0 |
| DESeq2 | 1.50.2 |
| g:Profiler | Web Platform |
| IGV | Latest Stable Release |

---

## Repository Structure

```text
comparative-atac-seq-analysis/
│
├── comparative_atac_seq_analysis.ipynb      # ATAC-seq preprocessing, peak calling, shared chromatin region analysis, annotation and motif analysis
├── functional_enrichment_analysis.ipynb     # Differential analysis, GO, KEGG, Reactome enrichment, PCA and Volcano plot
├── README.md
├── figures/
├── LICENSE
```
---

## Repository Contents

### 📓 comparative_atac_seq_analysis.ipynb

This notebook contains the complete ATAC-seq analysis workflow, including:

- Downloading sequencing data
- Quality control (FastQC)
- Read alignment (BWA)
- SAM to BAM conversion
- Sorting and indexing BAM files
- PCR duplicate removal
- Peak calling using MACS2
- Shared chromatin region identification
- Peak annotation using HOMER
- Motif enrichment analysis

### 📓 functional_enrichment_analysis.ipynb

This notebook contains the downstream biological analysis, including:

- Differential accessibility analysis using DiffBind and DESeq2
- Gene Ontology (GO) enrichment analysis
- KEGG pathway enrichment
- Reactome pathway enrichment
- Volcano plot visualization
- PCA visualization
- Biological interpretation of differential genes

## Analysis Pipeline

1. Download Cell Ranger ATAC.
2. Download the GRCh38 reference genome.
3. Create working directories.
4. Prepare FASTQ files.
5. Perform FastQC.
6. Align reads using BWA.
7. Convert SAM files to BAM format.
8. Sort and index BAM files.
9. Remove PCR duplicates using SAMtools.
10. Merge AD and MB biological replicates.
11. Sort merged BAM files.
12. Call peaks using MACS2.
13. Perform differential binding analysis using DiffBind and DESeq2.
14. Identify shared peaks using BEDTools.
15. Annotate peaks using HOMER.
16. Perform motif enrichment analysis.
17. Analyze promoter-associated peaks.
18. Generate summary visualizations.

---

## Key Results

### Volcano Plot

Differential accessibility analysis highlighting significantly altered chromatin regions.

![Volcano Plot](figures/Volcano_Plot.png)

---

### Gene Ontology (Biological Process)

Top enriched biological processes identified from differential genes.

![GO Biological Process](figures/GO_BP_BarPlot.png)

---

### KEGG Pathway Enrichment

Significantly enriched KEGG pathways associated with differential genes.

![KEGG Pathway Enrichment](figures/KEGG_BarPlot.png)

---

### Reactome Pathway Enrichment

Top enriched Reactome pathways associated with differential genes.

![Reactome Pathway Enrichment](figures/Reactome_Barplot.png)
---

## Data Availability

The raw sequencing data used in this project are available from the NCBI Sequence Read Archive (SRA). This repository contains the analysis workflow and selected processed results; large raw sequencing files are not included.

---

## Future Improvements

* Functional enrichment analysis (GO/KEGG/Reactome)
* Genome browser (IGV) visualization
* Additional quality control metrics
* Workflow automation using Snakemake or Nextflow

---

## Citation

If you use this workflow or build upon this project, please cite:

**Ankita Bhosale.** *Comparative ATAC-seq Analysis of Alzheimer's Disease and Medulloblastoma Microglia*. GitHub Repository.

---

## Author

## Author

**Ankita Bhosale**

B.Sc. (Hons.) Bioinformatics  
Department of Bioinformatics  
Interested in Epigenomics, Computational Biology, Epigenomics, and ATAC-seq Data Analysis.

📧 **Email:** ankitabhosale031@gmail.com

💼 **LinkedIn:** https://www.linkedin.com/in/ankita-bhosale-92382a315/
---

## License

This project is released under the MIT License.
