# DNA Extraction: Principles, Methods, Plant-Focused Notes & Quality Control

## Overview

DNA extraction is one of the most fundamental techniques in molecular biology. The goal is to isolate DNA from biological samples while removing proteins, RNA, lipids, salts, polysaccharides, phenolic compounds, and other contaminants.

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
- [18. Things to remember ](#18-Things-to-remember)
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
| Downstream application | Use DNA for PCR, sequencing, genotyping, cloning, etc. |

> **Plant Lab Note:**  
> In plant DNA extraction, contaminant removal is often the hardest part. Plant lysates can contain polysaccharides, polyphenols, pigments, starch, oils, and secondary metabolites that co-purify with DNA and inhibit downstream reactions.

---

## 4. Main Steps of DNA Extraction

### 4.1 Sample Collection and Preservation

Good DNA extraction starts before the actual extraction. DNA can degrade if the sample is poorly stored or handled.

Important factors include:

- Temperature
- Time before extraction
- Nuclease activity
- Tissue type
- Microbial contamination
- Repeated freeze-thaw cycles
- Mechanical damage during handling

For many animal and plant tissues, samples are stored at:

- **−20°C** for short-term storage
- **−80°C** for long-term storage
- **Liquid nitrogen** for high-quality DNA preservation
- **Ethanol or specialized preservation buffers** for field samples

For long-read sequencing, sample handling is especially important because long DNA molecules are easily broken.

#### Plant-Focused Notes

For plant DNA extraction, sample quality strongly affects final DNA quality.

Young leaves are often preferred because they usually contain:

- Less lignin
- Fewer oxidized phenolics
- Lower levels of secondary metabolites
- Softer tissue that is easier to grind

However, this depends on the species. Woody, oily, aromatic, and succulent plants can still be difficult even when young tissue is used.

| Sample Type | Potential Problem |
| :--- | :--- |
| Young leaves | Usually best, but may still contain phenolics |
| Old leaves | More lignin, phenolics, and secondary metabolites |
| Woody tissue | High lignin and polyphenols |
| Seeds | Starch, oils, and storage proteins |
| Succulent tissue | Mucilage and polysaccharides |
| Aromatic or medicinal plants | High secondary metabolite content |

> **Important:**  
> Plant tissue should ideally remain frozen during grinding. Thawing during grinding can activate nucleases and allow phenolic oxidation, which may damage DNA or reduce purity.

---

### 4.2 Cell Lysis

The first major step is **lysis**, which means breaking open cells.

Cells are surrounded by membranes. In plants, fungi, and bacteria, cells may also have a rigid cell wall.

The purpose of lysis is to release DNA from:

- Nucleus
- Mitochondria
- Chloroplasts in plants
- Bacterial cytoplasm

Common lysis components include:

| Component | Function |
| :--- | :--- |
| Detergents such as SDS or CTAB | Break membranes |
| Proteinase K | Digests proteins, including nucleases |
| EDTA | Chelates Mg²⁺ and inhibits DNases |
| Tris-HCl | Maintains stable pH |
| Salt | Helps protein removal and DNA purification |
| RNase A | Degrades RNA |
| PVP | Helps bind plant polyphenols |
| β-mercaptoethanol or DTT | Reduces oxidation of phenolic compounds |

A simplified diagram:

```text
Before lysis:

[ Cell membrane ]      [ Nucleus ]      DNA protected inside cells

After lysis:

Membrane broken → DNA released into solution
```

#### Plant-Focused Lysis Notes

Plant cells are harder to lyse because of the cell wall.

```text
Plant cell:

[ Cell wall ]  [ Plasma membrane ]  [ Chloroplasts ]  [ Vacuole ]  [ Nucleus with DNA ]
```

Chemical lysis alone is often not enough. Plant tissue usually requires mechanical disruption first, such as:

- Liquid nitrogen grinding
- Mortar and pestle grinding
- Bead beating
- TissueLyser homogenization
- Tissue homogenizer

For high molecular weight DNA, rough mechanical treatment should be minimized because long DNA molecules are fragile.

---

### 4.3 Protein Removal

Cells contain many proteins, including:

- Histones bound to DNA
- Enzymes
- Structural proteins
- DNases that can degrade DNA

Protein removal is usually achieved by:

- Proteinase K digestion
- Organic extraction, such as phenol-chloroform
- Salt precipitation of proteins
- Silica column purification
- Magnetic bead purification

Histones are especially important because eukaryotic DNA is wrapped around histone proteins to form chromatin.

```text
Eukaryotic DNA organization:

DNA → wraps around histones → nucleosomes → chromatin → chromosome
```

During extraction, proteins must be removed so that DNA becomes accessible and usable.

---

### 4.4 RNA Removal

Most DNA extraction also releases RNA. If the downstream application requires pure DNA, RNA should be removed.

This is usually done using **RNase A**, an enzyme that degrades RNA but not DNA.

Without RNase treatment, DNA concentration may be overestimated because RNA also absorbs UV light at 260 nm.

| Without RNase A | With RNase A |
| :--- | :--- |
| RNA remains in sample | RNA is degraded |
| NanoDrop DNA concentration may look falsely high | DNA quantification is more accurate |
| Downstream library prep may be affected | Cleaner DNA preparation |

---

### 4.5 DNA Purification

After lysis and protein digestion, DNA must be separated from contaminants.

Common purification strategies include:

- Phenol-chloroform extraction
- Silica column purification
- Magnetic bead purification
- CTAB extraction
- Salting-out methods
- Alcohol precipitation
- Commercial plant DNA kits

For plant samples, purification often needs extra attention because contaminants such as polysaccharides and polyphenols can co-purify with DNA.

---

## 5. Major DNA Extraction Methods

### 5.1 Phenol-Chloroform Extraction

Phenol-chloroform extraction is a classic method widely described in molecular biology manuals such as *Molecular Cloning* by Sambrook and Russell.

The principle is **phase separation**.

```text
After centrifugation:

Top aqueous phase:      DNA and RNA
Middle interphase:      proteins
Bottom organic phase:   lipids and hydrophobic molecules
```

Simplified diagram:

```text
Tube after phenol-chloroform extraction:

|----------------------|
| Aqueous phase        |  ← DNA
|----------------------|
| Interphase           |  ← proteins
|----------------------|
| Organic phase        |  ← phenol/chloroform, lipids
|----------------------|
```

Advantages:

- Can produce very pure DNA
- Useful for high molecular weight DNA
- Historically important and flexible

Disadvantages:

- Uses hazardous chemicals
- Time-consuming
- Requires careful phase separation
- Residual phenol can inhibit PCR or sequencing

---

### 5.2 Silica Column Extraction

Silica column kits are commonly used because they are easy, fast, and reproducible.

Principle:

> In the presence of chaotropic salts, DNA binds to silica. Contaminants are washed away, and DNA is eluted with water or low-salt buffer.

Workflow:

```text
Lysate
  ↓
Add binding buffer
  ↓
DNA binds silica membrane
  ↓
Wash contaminants
  ↓
Elute DNA
```

Advantages:

- Fast
- Convenient
- Good for PCR and short-read sequencing
- No phenol/chloroform required
- Suitable for routine DNA extraction

Disadvantages:

- DNA may be fragmented
- Often not ideal for ultra-long DNA
- Columns can shear DNA
- Binding capacity is limited

#### Plant Lab Note

For plant samples, silica column kits are convenient for short-read sequencing or PCR. However, difficult plant tissues may still require:

- CTAB pre-treatment
- PVP addition
- Extra wash steps
- Bead clean-up after extraction
- Careful removal of ethanol and salts

---

### 5.3 Magnetic Bead Extraction

Magnetic beads are widely used in modern molecular biology and sequencing workflows.

DNA binds to coated magnetic particles under certain salt and PEG conditions. A magnet is then used to collect the beads.

```text
DNA + magnetic beads
        ↓ magnet
Beads collect on side of tube
        ↓
Wash
        ↓
Elute DNA
```

Advantages:

- Scalable
- Automation-friendly
- Good for many samples
- Can be used for size selection
- Useful for post-extraction clean-up

Disadvantages:

- Bead carryover can affect downstream steps
- Conditions must be optimized
- Very long DNA may still be sheared if handled roughly
- Over-drying beads can reduce DNA recovery

---

### 5.4 CTAB Extraction

CTAB stands for **cetyltrimethylammonium bromide**. It is commonly used for plant DNA extraction.

Plants contain many difficult contaminants, especially:

- Polysaccharides
- Polyphenols
- Secondary metabolites
- Pigments
- Starch
- Mucilage
- Oils

CTAB helps separate DNA from polysaccharides and other plant compounds.

CTAB extraction was popularized by protocols such as those from Doyle and Doyle and related plant molecular biology methods.

Advantages:

- Excellent for many plant tissues
- Good for samples rich in polysaccharides
- Can produce high-quality genomic DNA
- Useful for difficult or recalcitrant plant species

Disadvantages:

- More labor-intensive
- May require optimization for different plant species
- Some plant metabolites still interfere
- Often requires careful clean-up before sequencing

#### Why CTAB Is Important for Plant DNA Extraction

Plant DNA extraction is difficult because many plant compounds behave badly during purification.

| Contaminant | Problem |
| :--- | :--- |
| Polysaccharides | Make DNA solution viscous and interfere with pipetting and sequencing |
| Polyphenols | Oxidize and bind DNA, causing brown color and poor purity |
| Pigments | Co-purify and reduce A260/A230 ratio |
| Starch | Can co-precipitate with DNA |
| Secondary metabolites | Inhibit PCR, ligation, and sequencing enzymes |

CTAB helps remove many of these contaminants, especially polysaccharides.

Common CTAB buffer additives:

| Additive | Purpose |
| :--- | :--- |
| CTAB | Detergent; helps separate DNA from polysaccharides |
| NaCl | Helps keep polysaccharides soluble |
| EDTA | Inhibits DNases |
| Tris-HCl | Maintains pH |
| PVP | Binds polyphenols |
| β-mercaptoethanol or DTT | Reduces phenolic oxidation |

---

### 5.5 Salting-Out Method

In salting-out methods, high salt concentrations cause proteins to precipitate while DNA remains in solution.

Advantages:

- No organic solvents
- Relatively inexpensive
- Good for blood or animal tissue

Disadvantages:

- Purity may vary
- May not remove all contaminants
- Less common for difficult plant tissues

---

## 6. Animal DNA Extraction vs Plant DNA Extraction

Animal and plant cells are different, so extraction strategies also differ.

---

### 6.1 Animal Cells

Animal cells have:

- Plasma membrane
- Nucleus
- Mitochondria
- No cell wall

Because animal cells lack a rigid cell wall, they are usually easier to lyse.

Common animal samples:

- Blood
- Muscle
- Liver
- Tail clips
- Buccal swabs
- Cultured cells
- Tissue biopsies

Main challenges:

| Challenge | Explanation |
| :--- | :--- |
| Proteins | Animal tissues are protein-rich |
| Lipids | Brain and adipose tissue contain many lipids |
| Heme | Blood contains heme, which can inhibit PCR |
| Collagen | Connective tissue can be hard to digest |
| Nucleases | Some tissues contain active DNases |

Basic animal cell lysis:

```text
Animal cell:

[ membrane ]    [ nucleus with DNA ]

Detergent + Proteinase K
        ↓
Membrane broken, proteins digested
        ↓
DNA released
```

Animal samples often work well with:

- Silica column kits
- Magnetic beads
- Phenol-chloroform extraction
- Salting-out methods

---

### 6.2 Plant Cells

Plant cells are more difficult because they contain:

- Cell wall made of cellulose
- Large vacuoles
- Chloroplasts
- Polysaccharides
- Polyphenols
- Secondary metabolites

Plant cell structure:

```text
Plant cell:

[ Cell wall ]  [ Plasma membrane ]  [ Chloroplasts ]  [ Vacuole ]  [ Nucleus with DNA ]
```

To extract plant DNA, you often need stronger mechanical disruption.

Examples:

- Grinding with liquid nitrogen
- Bead beating
- Mortar and pestle grinding
- Tissue homogenization

Main plant-specific problems:

| Problem | Why It Matters |
| :--- | :--- |
| Cell wall | Physically protects cells from lysis |
| Polysaccharides | Co-purify with DNA and make samples viscous |
| Polyphenols | Oxidize and bind DNA |
| Secondary metabolites | Inhibit PCR and sequencing |
| Chloroplast DNA | May contaminate nuclear DNA preparations |

CTAB buffer is often used because it helps remove polysaccharides.

A simplified plant workflow:

```text
Plant tissue
  ↓
Freeze / grind
  ↓
CTAB or plant kit lysis
  ↓
Remove proteins and polysaccharides
  ↓
Precipitate or bind DNA
  ↓
Wash
  ↓
Elute DNA
```

---

## 7. DNA Extraction for Short-Read vs Long-Read Sequencing

DNA extraction strategy depends strongly on sequencing technology.

The biggest difference is DNA fragment length.

---

### 7.1 Short-Read Sequencing

Short-read sequencing, such as Illumina sequencing, typically reads short DNA fragments.

Common read lengths:

- 50 bp
- 75 bp
- 100 bp
- 150 bp
- 250 bp

For many Illumina workflows, genomic DNA is intentionally fragmented into smaller pieces during library preparation.

```text
Original genomic DNA:

------------------------------------------------------------

Fragmented for short-read sequencing:

-----   -----   -----   -----   -----   -----   -----
```

For short-read sequencing, DNA should be:

- Pure
- Free of inhibitors
- Adequate in concentration
- Not extremely degraded
- Compatible with enzymatic fragmentation or tagmentation

But it does not always need to be ultra-long.

Suitable extraction methods often include:

- Silica column kits
- Magnetic bead kits
- Standard genomic DNA kits
- CTAB for plants, followed by cleanup

Important quality concerns:

| QC Factor | Importance for Short Reads |
| :--- | :--- |
| Purity | Very important |
| Concentration | Important |
| Fragment length | Moderate importance |
| RNA contamination | Should be minimized |
| Inhibitors | Must be removed |

Short-read sequencing is often more forgiving of moderate DNA fragmentation.

---

### 7.2 Long-Read Sequencing

Long-read sequencing includes technologies such as:

- Oxford Nanopore sequencing
- PacBio HiFi sequencing
- PacBio continuous long reads

These methods benefit from high molecular weight DNA.

Long-read sequencing can produce reads from thousands to hundreds of thousands of bases.

```text
Short-read DNA fragments:

----- ----- ----- ----- -----

Long-read DNA fragments:

----------------------------------------------------------------------------------------------------------------------------------------------------
```

For long-read sequencing, DNA must be:

- High molecular weight
- Minimally sheared
- Free of contaminants
- Free of proteins and polysaccharides
- Accurately quantified
- Often free of small DNA fragments

The biggest challenge is avoiding mechanical shearing.

DNA is physically fragile when very long. Rough pipetting, vortexing, bead beating, or repeated freeze-thaw cycles can break it.

For long-read sequencing, labs often use:

- Gentle nuclei isolation
- Wide-bore pipette tips
- Slow mixing by inversion
- Avoiding vortexing
- Agarose plug methods for ultra-high molecular weight DNA
- Magnetic bead cleanup with careful handling
- CTAB-based or nuclei-based methods for plants

Important quality concerns:

| QC Factor | Importance for Long Reads |
| :--- | :--- |
| Molecular weight | Extremely important |
| Purity | Extremely important |
| Concentration | Important |
| RNA contamination | Should be low |
| Mechanical shearing | Must be minimized |
| Small-fragment contamination | Often undesirable |

---

## 8. Visual Comparison: Short-Read vs Long-Read DNA Requirements

```text
Short-read sequencing:

Input DNA can be moderately fragmented.

Genome:
============================================================

Extracted DNA:
==========  ========  ======  ==========  ========

Library fragments:
--- --- --- --- --- --- --- --- --- --- ---


Long-read sequencing:

Input DNA should remain very long.

Genome:
============================================================

Extracted DNA:
============================================================================================================================

Library molecules:
=====================================================================================================
```

Key idea:

> **Short-read sequencing mainly needs clean DNA.**  
> **Long-read sequencing needs clean DNA and long DNA.**

---

## 9. Why DNA Quality Matters

Poor-quality DNA can cause:

- Failed PCR
- Low sequencing yield
- Biased genome coverage
- Shorter read lengths
- Poor library preparation
- Inaccurate quantification
- Enzyme inhibition

Common contaminants and their effects:

| Contaminant | Common Source | Effect |
| :--- | :--- | :--- |
| Protein | Incomplete digestion | Low purity, enzyme inhibition |
| RNA | No RNase treatment | Overestimated DNA concentration |
| Phenol | Organic extraction | Inhibits PCR/sequencing |
| Ethanol | Incomplete drying | Inhibits enzymes |
| Salt | Incomplete washing | Poor library prep |
| Polysaccharides | Plants | Viscous DNA, poor sequencing |
| Polyphenols | Plants | DNA oxidation/binding |
| Heme | Blood | PCR inhibition |
| Humic acids | Soil/environmental samples | PCR inhibition |

---

## 10. DNA Quality Control

After extraction, DNA should be checked before downstream experiments.

---

### 10.1 Concentration Measurement

Common tools:

| Method | Measures | Notes |
| :--- | :--- | :--- |
| NanoDrop | UV absorbance | Fast but can overestimate DNA |
| Qubit | Fluorescence | More accurate for DNA concentration |
| Gel electrophoresis | Size and integrity | Visual check |
| TapeStation / Bioanalyzer / Femto Pulse | Size distribution | Useful for sequencing QC |

NanoDrop measures absorbance at 260 nm because nucleic acids absorb UV light.

However, NanoDrop cannot easily distinguish DNA from RNA or some contaminants.

Qubit uses fluorescent dyes that bind specifically to DNA, so it is usually more accurate for DNA concentration.

---

### 10.2 Purity Ratios

NanoDrop gives two important ratios.

#### A260/A280

This ratio estimates protein contamination.

Typical pure DNA:

```text
A260/A280 ≈ 1.8
```

Lower values may indicate:

- Protein contamination
- Phenol contamination
- Incomplete purification

#### A260/A230

This ratio estimates contamination from salts, phenol, carbohydrates, or organic compounds.

Typical pure DNA:

```text
A260/A230 ≈ 2.0–2.2
```

Low A260/A230 is common in plant DNA extractions due to:

- Polysaccharides
- Phenolic compounds
- Guanidine salts
- Ethanol carryover
- Other plant secondary metabolites

---

### 10.3 Gel Electrophoresis

Agarose gel electrophoresis can show DNA integrity.

Example:

```text
High-quality genomic DNA:

Well | V
[########]  strong high molecular weight band near top
[        ]
[        ]
[        ]


Degraded DNA:

Well | V
[###     ]
[ #####  ]
[  ##### ]
[   #### ]  smear down the gel
```

High molecular weight DNA stays near the top of the gel because it moves slowly.

Degraded DNA appears as a smear.

For long-read sequencing, standard agarose gels may not fully resolve very large DNA. Pulsed-field gel electrophoresis or instruments such as **Femto Pulse** are often more informative.

---

## 11. Nuclear DNA, Mitochondrial DNA, and Chloroplast DNA

DNA extraction usually does not extract only one type of DNA unless the protocol is specifically designed to do so.

Animal cells contain:

- Nuclear DNA
- Mitochondrial DNA

Plant cells contain:

- Nuclear DNA
- Mitochondrial DNA
- Chloroplast DNA

```text
Animal cell DNA sources:

Nucleus       → nuclear genome
Mitochondria  → mitochondrial genome


Plant cell DNA sources:

Nucleus       → nuclear genome
Mitochondria  → mitochondrial genome
Chloroplasts  → chloroplast genome
```

For whole-genome sequencing, this matters because organelle DNA can occupy part of the sequencing output.

In plant samples, chloroplast DNA can be abundant, especially in leaf tissue.

> **Plant Lab Note:**  
> If the goal is nuclear genome sequencing, high chloroplast DNA content can reduce the proportion of sequencing reads mapped to the nuclear genome. Tissue type and extraction strategy can influence organellar DNA carryover.

---

## 12. Special Considerations for Animal Samples

### Blood

Blood can provide high-quality DNA, especially from white blood cells.

However, red blood cells in mammals lack nuclei, so most genomic DNA comes from leukocytes.

Potential inhibitors:

- Heme
- Anticoagulants
- Proteins

### Muscle

Muscle contains many proteins and mitochondria. Good digestion is important.

### Liver

Liver is rich in enzymes and nucleases, so rapid preservation is important.

### Brain or Fat-Rich Tissue

These tissues contain many lipids, which may require extra cleanup.

---

## 13. Special Considerations for Plant Samples

Because this is a plant-focused lab, plant sample type should be considered carefully before extraction.

### Young Leaves

Young leaves are often preferred because they may contain fewer secondary metabolites than older tissue.

Advantages:

- Easier to grind
- Usually higher nuclear DNA quality
- Often fewer inhibitors
- Less lignified tissue

### Woody Plants

Woody plants can be difficult due to:

- Lignin
- Polyphenols
- Polysaccharides
- Tough tissue structure

Potential solutions:

- Stronger grinding with liquid nitrogen
- CTAB extraction
- PVP addition
- Antioxidants such as β-mercaptoethanol or DTT
- Extra clean-up steps

### Seeds

Seeds may contain:

- Starch
- Oils
- Storage proteins

These contaminants can interfere with DNA extraction and downstream library preparation.

### Succulent Plants

Succulent tissues may contain mucilage and polysaccharides, which can co-purify with DNA and make the DNA solution viscous.

### Medicinal or Aromatic Plants

These may contain high levels of secondary metabolites that inhibit downstream reactions.

Common issues include:

- Brown or dark-colored lysate
- Low A260/A230 ratio
- Poor PCR amplification
- Poor sequencing library prep
- Viscous eluate

---

## 14. Choosing a DNA Extraction Method

A simple decision guide:

```text
Need DNA for PCR?
      ↓
Silica column or quick extraction often works.


Need DNA for Illumina short-read sequencing?
      ↓
Clean DNA is most important.
Silica column, magnetic beads, CTAB + cleanup can work.


Need DNA for Nanopore or PacBio long-read sequencing?
      ↓
High molecular weight DNA is critical.
Use gentle handling, avoid vortexing,
consider nuclei-based or HMW methods.


Working with plants?
      ↓
Consider CTAB, plant-specific kits,
PVP/antioxidants, and bead cleanup.


Working with animal tissue?
      ↓
Proteinase K digestion + column/bead/organic extraction often works.
```

---

## 15. Common Mistakes in DNA Extraction

| Mistake | Consequence |
| :--- | :--- |
| Poor sample storage | DNA degradation |
| Too much starting material | Incomplete lysis, dirty DNA |
| Insufficient grinding of plant tissue | Low yield |
| Harsh vortexing for long-read DNA | DNA shearing |
| Incomplete protein digestion | Low purity |
| Skipping RNase when needed | RNA contamination |
| Incomplete ethanol removal | Enzyme inhibition |
| Over-drying DNA pellet or beads | DNA hard to dissolve |
| Using NanoDrop alone | Inaccurate concentration |
| Ignoring A260/A230 | Hidden contaminants |
| Overloading spin columns | Low purity and poor recovery |
| Disturbing pellet during transfer | Contaminant carryover |

---

## 16. Summary Table

| Feature | Short-Read DNA Extraction | Long-Read DNA Extraction |
| :--- | :--- | :--- |
| Main goal | Clean DNA | Clean and very long DNA |
| Fragment size | Moderate is acceptable | High molecular weight required |
| Handling | Standard careful handling | Very gentle handling |
| Vortexing | Sometimes acceptable | Avoid |
| Pipetting | Normal pipetting often okay | Wide-bore tips recommended |
| Common methods | Column, beads, CTAB | HMW kits, nuclei prep, plug methods, gentle CTAB |
| QC | Qubit, NanoDrop, gel | Qubit, NanoDrop, PFGE/Femto Pulse/TapeStation |
| Typical use | Illumina, PCR, genotyping | Nanopore, PacBio, de novo genome assembly |

---

## 17. Plant-Focused Example: Pistachio DNA Extraction for Short-Read Sequencing

This section provides a practical example of plant DNA extraction using a column-based workflow, suitable for short-read sequencing.

### 17.1 Overview

**Protocol:** Pistachio DNA Extraction for Short-Read Sequencing  
**Estimated time:** Approximately 4 hours hands-on

Approximate time distribution:

| Step | Estimated Time |
| :--- | :--- |
| Liquid nitrogen grinding and tissue preparation | ~15 min |
| Lysis at 65°C | 20 min |
| P3 incubation | 10–15 min |
| QIAshredder and DNeasy column spins | ~15 min |
| Wash spins | ~10 min |
| Elution | ~5 min |
| QC | Variable |

This workflow is mostly column-spin work after lysis and is relatively fast compared with high molecular weight DNA protocols.

There are no overnight steps.

The slowest step is usually the 65°C lysis incubation; most other steps are short centrifugations and washes.

---

### 17.2 Resources

#### Equipment

- Centrifuge
- TissueLyser
- Heating block or water bath
- Magnetic rack, if performing bead clean-up

#### Kits

- DNeasy Plant Mini Kit

#### Reagents

- 70% ethanol
- 80% ethanol, freshly prepared
- MES buffer
- Polyvinylpyrrolidone, PVP
- RNase A
- Buffer AP1
- Buffer P3
- Buffer AW1
- Buffer AW2
- Buffer EB
- Collibri beads, for clean-up if needed

#### Consumables

- 2 mL microtubes
- 1.5 mL microcentrifuge tubes
- QIAshredder spin columns
- DNeasy Mini spin columns
- Collection tubes
- Pipette tips
- Beads for tissue grinding

#### Related Protocols

- Quick DNA Extraction for PCR, Buffer A Method
- HiFi DNA Extraction, DIY
- HMW extraction for challenging plants

---

### 17.3 Pre-Treatment

Before starting:

- Perform all centrifugation steps at room temperature, **15–25°C**.
- Add ethanol to Buffer AW1 and Buffer AW2 as instructed by the manufacturer.
- Redissolve any precipitates in Buffer AP1 and Buffer AW1 concentrates.
- Preheat Buffer EB to **65°C** in a heating block or water bath.
- Keep plant tissues frozen before grinding.

---

### 17.4 Main Extraction Protocol

1. Weigh **80–100 mg** of fresh tissue.

2. Put two medium-sized beads into each **2 mL microtube**.

3. Keep the tubes submerged in liquid nitrogen to prevent thawing.

4. Grind the samples into a fine powder using a TissueLyser.

5. Add:

   - **800 μL Buffer AP1**, lysis buffer
   - **10 μL RNase A**

6. Vortex vigorously.

7. Incubate for **20 min at 65°C**.

8. Invert the tube every **3–5 min** during incubation.

9. Add **260 μL Buffer P3**.

10. Mix thoroughly by inverting or vortexing.

11. Incubate for **10–15 min at room temperature** to precipitate polysaccharides and proteins.

12. Centrifuge the lysate for **5 min at 20,000 × g**, approximately **14,000 rpm**.

13. Pipette the lysate into a QIAshredder spin column placed in a 2 mL collection tube.

    - Load approximately **650 μL per spin**.
    - Repeat if there is remaining lysate.

14. Centrifuge for **2 min at 20,000 × g**.

15. Carefully transfer the flow-through into a new tube without disturbing the pellet.

16. Estimate or measure the exact volume of the flow-through.

17. Add exactly **1.5 volumes of Buffer AW1** to the flow-through.

18. Mix thoroughly by pipetting.

19. Transfer **650 μL** of the mixture into a DNeasy Mini spin column.

20. Centrifuge for **1 min at ≥6000 × g**, approximately **≥8000 rpm**.

21. Discard the flow-through.

22. Repeat until all mixture is processed.

23. Place the spin column into a new 2 mL collection tube.

24. Add **500 μL Buffer AW2**.

25. Close the cap securely and invert the tube to wash the inner walls.

26. Centrifuge for **1 min at ≥6000 × g**.

27. Discard the flow-through.

28. Add another **500 μL Buffer AW2**.

29. Invert the tube again.

30. Centrifuge for **2 min at 20,000 × g**.

31. Add **500 μL freshly prepared 80% ethanol**.

32. Centrifuge for **1 min at ≥6000 × g**.

33. Discard the flow-through.

34. Add another **500 μL 80% ethanol**.

35. Centrifuge for **2 min at 20,000 × g**.

36. Discard the flow-through.

37. Centrifuge the empty column again for **2 min at 20,000 × g** to completely dry the membrane.

38. Open the cap and let the column sit on a heat block at **65°C for 3–5 min** to allow residual ethanol to evaporate.

39. Transfer the spin column to a new **1.5 mL microcentrifuge tube**.

40. Add **35 μL pre-warmed Buffer EB**, approximately **55–65°C**, directly to the center of the membrane.

41. Incubate for **5 min** at room temperature or 55°C.

42. Centrifuge for **1 min at ≥6000 × g** to elute DNA.

---

### 17.5 Bead Clean-Up Pre-Treatment

Before bead clean-up:

- Remove Collibri beads from 4°C storage and allow them to reach room temperature, **15–25°C**, for at least **30 min**.
- Prepare fresh **80% ethanol** for wash steps.
- Preheat Buffer EB to **55–65°C**.
- Vortex the beads thoroughly before use to fully resuspend them.

---

### 17.6 Bead Clean-Up Protocol

1. Add **1.65 volumes** of Collibri beads to the extracted DNA solution.

   Example:

   ```text
   For 33 μL eluate:
   33 μL × 1.65 = 54.45 μL beads
   ```

2. Mix thoroughly by vortexing or pipetting.

3. Incubate at room temperature for **5 min** to allow DNA binding to beads.

4. Place tubes on a magnetic rack.

5. Wait until the solution becomes clear, approximately **2–3 min**.

6. If the solution appears clear, wait an additional **30 sec** to ensure complete bead separation.

7. Carefully remove and discard the supernatant without disturbing the bead pellet.

8. Add **1 mL freshly prepared 80% ethanol** to the beads.

9. Invert the tubes **10–15 times** to wash.

10. Return tubes to the magnetic rack and wait until the solution is clear.

11. Carefully remove and discard the ethanol.

12. Repeat the ethanol wash one more time.

13. After the second wash, briefly spin down the tubes and place them back on the magnetic rack.

14. Remove as much residual ethanol as possible.

    A useful strategy is to gradually use pipettes with decreasing volume ranges:

    - 100–1000 μL pipette
    - 20–200 μL pipette
    - 0.2–2 μL pipette

15. Air-dry the beads at room temperature for **3–5 min**, until no ethanol residue is visible.

    > Do not over-dry the beads.

16. Add **22 μL pre-warmed Buffer EB**, approximately **55–65°C**, directly to the bead pellet.

17. Pipette up and down to resuspend the beads.

18. Incubate for **5 min at room temperature**.

19. Place tubes on the magnetic rack.

20. Wait until the solution is clear, approximately **2 min**.

21. Carefully transfer the eluted DNA solution to a new **1.5 mL microcentrifuge tube** without disturbing the bead pellet.

---

### 17.7 Practical Notes for Pistachio and Other Difficult Plant Samples

Based on experience with short-read sequencing DNA extractions of Kerman pistachio samples:

- Performing **1–2 rounds of bead clean-up** after Plant Mini Kit extraction is generally sufficient to obtain clean DNA.
- For problematic samples that consistently yield poor results, a **CTAB wash or CTAB-based pre-treatment** is recommended.
- Difficult plant samples may require extra attention to polysaccharides and phenolics.
- Low A260/A230 often indicates plant-derived contaminants.
- If the eluate is viscous, polysaccharide contamination may be present.
- If the sample is brown or dark, phenolic oxidation may have occurred.

Recommended troubleshooting:

| Problem | Possible Cause | Solution |
| :--- | :--- | :--- |
| Low yield | Poor grinding or incomplete lysis | Improve liquid nitrogen grinding |
| Viscous DNA | Polysaccharide contamination | CTAB treatment or extra cleanup |
| Brown DNA solution | Polyphenol oxidation | Use PVP and reducing agents |
| Low A260/A230 | Salt, polysaccharides, phenolics | Additional bead cleanup or ethanol wash |
| Poor PCR/library prep | Inhibitor carryover | Repeat cleanup or use CTAB pre-treatment |
| Weak Qubit reading but high NanoDrop | RNA or contaminants affecting NanoDrop | Trust Qubit more; check RNase step |

---

## 18. Things to remember 

DNA extraction is the process of separating DNA from cells and contaminants.

All DNA extraction methods include:

- Lysis
- Purification
- Washing
- Elution
- Quality control

Animal DNA extraction is usually easier because animal cells lack cell walls.

Plant DNA extraction is harder because plant tissues contain:

- Cell walls
- Polysaccharides
- Polyphenols
- Secondary metabolites
- Pigments
- Starch
- Chloroplast DNA

Short-read sequencing mainly requires **clean DNA**.

Long-read sequencing requires **clean, high molecular weight DNA**.

DNA quality should be checked using:

- Concentration measurement
- Purity ratios
- Gel or instrument-based size analysis

The best extraction method depends on:

- Sample type
- Plant species
- Tissue type
- Downstream application
- Required DNA fragment length
- Tolerance of downstream enzymes to inhibitors

For a plant-focused lab, the most important principle is:

> **Good plant DNA extraction is not only about releasing DNA. It is mainly about removing plant-specific contaminants while preserving enough DNA quality for the downstream application.**

---

## References and Recommended Reading

1. Sambrook, J., & Russell, D. W. (2001). *Molecular Cloning: A Laboratory Manual*. 3rd ed. Cold Spring Harbor Laboratory Press.  
   Classic molecular biology reference for DNA extraction, purification, restriction digestion, cloning, and nucleic acid handling.

2. Green, M. R., & Sambrook, J. (2012). *Molecular Cloning: A Laboratory Manual*. 4th ed. Cold Spring Harbor Laboratory Press.  
   Updated version of the classic laboratory manual.

3. Ausubel, F. M., Brent, R., Kingston, R. E., Moore, D. D., Seidman, J. G., Smith, J. A., & Struhl, K. (eds.). *Current Protocols in Molecular Biology*. Wiley.  
   Detailed protocols and explanations for nucleic acid extraction and molecular biology techniques.

4. Doyle, J. J., & Doyle, J. L. (1987). A rapid DNA isolation procedure for small quantities of fresh leaf tissue. *Phytochemical Bulletin*, 19, 11–15.  
   A widely cited CTAB-based plant DNA extraction method.

5. Murray, M. G., & Thompson, W. F. (1980). Rapid isolation of high molecular weight plant DNA. *Nucleic Acids Research*, 8(19), 4321–4325.  
   Important early paper on plant high molecular weight DNA extraction.

6. Dellaporta, S. L., Wood, J., & Hicks, J. B. (1983). A plant DNA minipreparation: Version II. *Plant Molecular Biology Reporter*, 1, 19–21.  
   Classic plant DNA miniprep method.

7. Healey, A., Furtado, A., Cooper, T., & Henry, R. J. (2014). Protocol: A simple method for extracting next-generation sequencing quality genomic DNA from recalcitrant plant species. *Plant Methods*, 10, 21.  
   Useful for difficult plant tissues and sequencing-quality DNA.

8. Mayjonade, B., et al. (2016). Extraction of high-molecular-weight genomic DNA for long-read sequencing of single molecules. *BioTechniques*, 61(4), 203–205.  
   Discusses high molecular weight DNA extraction for long-read sequencing.

9. Loman, N. J., & Watson, M. (2015). Successful test launch for nanopore sequencing. *Nature Methods*, 12, 303–304.  
   Background on nanopore sequencing development.

10. Logsdon, G. A., Vollger, M. R., & Eichler, E. E. (2020). Long-read human genome sequencing and its applications. *Nature Reviews Genetics*, 21, 597–614.  
    Review of long-read sequencing applications and importance.

11. Metzker, M. L. (2010). Sequencing technologies — the next generation. *Nature Reviews Genetics*, 11, 31–46.  
    Overview of next-generation sequencing technologies.

12. Heather, J. M., & Chain, B. (2016). The sequence of sequencers: The history of sequencing DNA. *Genomics*, 107(1), 1–8.  
    Accessible review of sequencing technologies.
