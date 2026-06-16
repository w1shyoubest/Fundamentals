# DNA Extraction: Principles, Methods, Plant-Focused Notes & Quality Control

## Overview

DNA extraction is one of the most fundamental techniques in molecular biology.  
The goal is to isolate DNA from biological samples while removing proteins, RNA, lipids, salts, polysaccharides, phenolic compounds, and other contaminants.

Because our lab mainly works with plants, this document emphasizes **plant DNA extraction**, especially the challenges caused by plant cell walls, polysaccharides, polyphenols, pigments, starch, and secondary metabolites.

---

## Table of Contents

- [1. What Is DNA Extraction?](#1-what-is-dna-extraction)
- [2. Basic Structure of DNA Relevant to Extraction](#2-basic-structure-of-dna-relevant-to-extraction)
- [3. The General Logic of DNA Extraction](#3-the-general-logic-of-dna-extraction)
- [4. Main Steps of DNA Extraction](#4-main-steps-of-dna-extraction)
  - [4.1 Sample Collection and Preservation](#41-sample-collection-and-preservation)
  - [4.2 Cell Lysis](#42-cell-lysis)
  - [4.3 Protein Removal](#43-protein-removal)
  - [4.4 RNA Removal](#44-rna-removal)
  - [4.5 DNA Purification](#45-dna-purification)
- [5. Major DNA Extraction Methods](#5-major-dna-extraction-methods)
  - [5.1 Phenol-Chloroform Extraction](#51-phenol-chloroform-extraction)
  - [5.2 Silica Column Extraction](#52-silica-column-extraction)
  - [5.3 Magnetic Bead Extraction](#53-magnetic-bead-extraction)
  - [5.4 CTAB Extraction](#54-ctab-extraction)
  - [5.5 Salting-Out Method](#55-salting-out-method)
- [6. Animal DNA Extraction vs Plant DNA Extraction](#6-animal-dna-extraction-vs-plant-dna-extraction)
  - [6.1 Animal Cells](#61-animal-cells)
  - [6.2 Plant Cells](#62-plant-cells)
- [7. DNA Extraction for Short-Read vs Long-Read Sequencing](#7-dna-extraction-for-short-read-vs-long-read-sequencing)
  - [7.1 Short-Read Sequencing](#71-short-read-sequencing)
  - [7.2 Long-Read Sequencing](#72-long-read-sequencing)
- [8. Visual Comparison: Short-Read vs Long-Read DNA Requirements](#8-visual-comparison-short-read-vs-long-read-dna-requirements)
- [9. Why DNA Quality Matters](#9-why-dna-quality-matters)
- [10. DNA Quality Control](#10-dna-quality-control)
  - [10.1 Concentration Measurement](#101-concentration-measurement)
  - [10.2 Purity Ratios](#102-purity-ratios)
  - [10.3 Gel Electrophoresis](#103-gel-electrophoresis)
- [11. Nuclear DNA, Mitochondrial DNA, and Chloroplast DNA](#11-nuclear-dna-mitochondrial-dna-and-chloroplast-dna)
- [12. Special Considerations for Animal Samples](#12-special-considerations-for-animal-samples)
- [13. Special Considerations for Plant Samples](#13-special-considerations-for-plant-samples)
- [14. Choosing a DNA Extraction Method](#14-choosing-a-dna-extraction-method)
- [15. Common Mistakes in DNA Extraction](#15-common-mistakes-in-dna-extraction)
- [16. Summary Table](#16-summary-table)
- [17. Plant-Focused Example: Pistachio DNA Extraction for Short-Read Sequencing](#17-plant-focused-example-pistachio-dna-extraction-for-short-read-sequencing)
- [18. Final Summary](#18-final-summary)
- [References and Recommended Reading](#references-and-recommended-reading)

---

## 1. What Is DNA Extraction?

DNA extraction is the process of isolating DNA from biological material such as:

- Animal tissue
- Plant leaves
- Blood
- Cultured cells
- Bacteria
- Fungi

The goal is to separate DNA from:

- Cell membranes
- Proteins
- RNA
- Lipids
- Polysaccharides
- Phenolic compounds
- Salts
- Other contaminants

The purified DNA can then be used for downstream applications such as:

- PCR
- qPCR
- Genotyping
- Sanger sequencing
- Illumina short-read sequencing
- PacBio or Oxford Nanopore long-read sequencing
- Genome assembly
- Restriction enzyme digestion
- Cloning

At a basic level, DNA extraction answers this question:

> **How do we break open cells and keep the DNA while removing everything else?**

For plant work, the question becomes more specific:

> **How do we break open tough plant tissue, release DNA, and remove plant-specific contaminants such as polysaccharides, polyphenols, pigments, starch, and secondary metabolites?**

---

## 2. Basic Structure of DNA Relevant to Extraction

DNA is a long polymer made of nucleotides. Each nucleotide contains:

- A phosphate group
- A deoxyribose sugar
- A nitrogenous base: A, T, G, or C

DNA is **negatively charged** because of its phosphate backbone.

```text
Simplified DNA structure:

5' - A - T - G - C - C - A - T - 3'
     |   |   |   |   |   |   |
3' - T - A - C - G - G - T - A - 5'

Sugar-phosphate backbone = negatively charged
Base pairs = genetic information
```

This negative charge is very important because many DNA purification methods rely on charge-based interactions.

For example, under high-salt conditions, DNA can bind to:

- Silica membranes
- Silica columns
- Magnetic beads
- Other solid-phase purification matrices

This is the principle behind many commercial DNA extraction kits.

---

## 3. The General Logic of DNA Extraction

Most DNA extraction methods follow the same conceptual workflow:

```text
Biological sample
       ↓
Cell disruption / lysis
       ↓
Protein and contaminant removal
       ↓
DNA binding or precipitation
       ↓
Washing
       ↓
DNA elution / resuspension
       ↓
Quality control
       ↓
Downstream application
```

Each step has a specific purpose.

| Step | Purpose |
| :--- | :--- |
| Sample preparation | Preserve DNA and prepare the sample for extraction |
| Cell disruption / lysis | Break open cells and release DNA |
| Protein and contaminant removal | Remove proteins, nucleases, polysaccharides, and other contaminants |
| DNA binding or precipitation | Separate DNA from the lysate |
| Washing | Remove salts, ethanol, proteins, and inhibitors |
| Elution / resuspension | Recover purified DNA |
| Quality control | Check DNA concentration, purity, and fragment size |
| Downstream application | Use DNA for
