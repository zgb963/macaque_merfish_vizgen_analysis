# MERFISH / Spatial Transcriptomics Analysis — Macaque Primary Visual Cortex (V1)

## Introduction

The [UMMS SCOPE facility](https://www.umassmed.edu/scope/) and [Vizgen](https://vizgen.com/) collaborated with our neurobiology lab to generate a large-scale MERFISH/Spatial Transcriptomics dataset (~6 TB) profiling the primary visual cortex (V1) of the Rhesus macaque (*Macaca mulatta*, rhemac10).

Using Excel and Python, I created a panel of **881 genes** curated from rhemac10 and human (GRCh38) references to identify major cell types in V1 — including excitatory, inhibitory, glial, and vascular populations. The panel also includes **75 activity-dependent genes** associated with ocular dominance columns (ODCs) [(citation)](#).

---

## What is MERFISH?

**MERFISH (Multiplexed Error-Robust Fluorescence In Situ Hybridization)** is a high-throughput spatial transcriptomics method that detects and quantifies individual RNA transcripts directly within intact tissue sections using fluorescently labeled probes.

### How it differs from snRNA-seq

While MERFISH/MERSCOPE and snRNA-seq both aim to quantify gene expression at single-cell resolution, they differ in approach:

| Feature | snRNA-seq | MERFISH/MERSCOPE |
|---|---|---|
| Method | Sequencing RNA molecules | Fluorescent probe imaging |
| Spatial info | ❌ Lost during dissociation | ✅ Preserved |
| Output | Read counts | Transcript counts per cell |
| Tissue context | ❌ No | ✅ Yes |

Gene expression counts in MERFISH represent the **number of RNA transcripts detected per gene per cell** via fluorescence imaging. These counts are used for:
- Cell type characterization
- Spatial mapping of cell populations
- Quality control and filtering

> ⚠️ **Filtering note:** Cells with very low total gene expression counts may reflect poor probe hybridization or low RNA capture efficiency. Filtering is essential for reliable downstream analysis but should be applied carefully alongside spatial considerations. *(Thresholds: TBD)*

---

## Dataset

**2 samples / slides:**

| Slide | Regions |
|---|---|
| Slide 4 | Regions 1, 2, 3, 4 |
| Slide 5 | Regions 1, 2, 3, 4, 5, 6 |

---

## Goals

- [ ] Identify cell types in macaque V1
- [ ] Map the spatial organization of cell types
- [ ] Predict activity states (active vs. inactive)
- [ ] Validate gene expression patterns against rhemac10 snRNA-seq and [Wei et al. 2022](https://www.nature.com/articles/s41467-022-34590-1)

---

## Methods

1. **Data transfer** — MERFISH data transferred from SCOPE to lab HPC cluster via `rsync`
2. **Analysis environment** — Jupyter notebooks, Python, [scanpy](https://scanpy.readthedocs.io/), [squidpy](https://squidpy.readthedocs.io/), conda
3. **Visualization** — Transcriptomic data exported from Jupyter into Vizgen MERSCOPE software *(version: TBD)* for spatial visualization

---
## Notebooks

All analyses are provided in both:
- Jupyter Notebook (.ipynb)
- HTML export (static report)

Download and view HTML files for best viewing experience. Download and view Jupyter Notebook for raw code.

---
## Results

> 🔬 Analysis ongoing

---

## References

- [Wei et al. 2022](https://www.nature.com/articles/s41467-022-34590-1)
- *(add additional references)*
