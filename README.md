# Phylogenetic-Tree-Analysis-MEGA12
Phylogenetic tree reconstruction and alignment analysis using MEGA12 GUI
# Circular Phylogenetic Tree Analysis Using MEGA12

## 📌 Project Overview
This repository contains a complete bioinformatic and phylogenetic investigation executed entirely using the graphical interface of **MEGA12 (Molecular Evolutionary Genetics Analysis)**. 

The project evaluates sequence homology, alignment, substitution model parameters, and constructs Maximum Likelihood (ML) phylogenetic trees for **20 target accessions**[cite: 1]. Results are rendered in a radial/circular tree layout[cite: 1].

---

## 🧬 Analyzed Accession Dataset (20 Sequences)

The dataset consists of the following 20 accession records analyzed in this study[cite: 1]:

* `YP_161207.1`[cite: 1]
* `YP_161181.1`[cite: 1]
* `YP_003673.1`[cite: 1]
* `YP_161220.1`[cite: 1]
* `YP_161233.1`[cite: 1]
* `YP_161194.1`[cite: 1]
* `YP_161259.1`[cite: 1]
* `YP_011095906.1`[cite: 1]
* `YP_011103439.1`[cite: 1]
* `YP_011103528.1`[cite: 1]
* `YP_011101262.1`[cite: 1]
* `YP_011101275.1`[cite: 1]
* `YP_011104168.1`[cite: 1]
* `YP_011087230.1`[cite: 1]
* `YP_011103850.1`[cite: 1]
* `NP_659248.1`[cite: 1]
* `YP_011108383.1`[cite: 1]
* `YP_011102885.1`[cite: 1]
* `YP_011102450.1`[cite: 1]
* `YP_011103426.1`[cite: 1]

---

## 🔬 Complete Workflow Followed in MEGA12 GUI

### Step 1: Sequence Data Acquisition
1. Downloaded 20 homologous target sequences in FASTA format from the NCBI database.
2. Saved the raw file as `raw_sequences.fasta`.

### Step 2: Multiple Sequence Alignment (MSA)
1. Opened **MEGA12** $\rightarrow$ Clicked **Align** $\rightarrow$ **Edit/Build Alignment**.
2. Choose **Retrieve sequences from a file** and loaded `raw_sequences.fasta`.
3. Selected all sequences (`Ctrl + A`) and clicked **Alignment** $\rightarrow$ **Align by MUSCLE / ClustalW**.
4. Saved alignment via **Data** $\rightarrow$ **Export Alignment** $\rightarrow$ **MEGA Format** as `aligned_sequences.meg`.

### Step 3: Best-Fit Substitution Model Selection
1. On the main MEGA12 toolbar, clicked **Models** $\rightarrow$ **Find Best DNA/Protein Models**.
2. Opened `aligned_sequences.meg`.
3. Evaluated candidate models using **BIC (Bayesian Information Criterion)** scores to pick the optimal substitution model.

### Step 4: Phylogenetic Tree Reconstruction
1. Clicked **Phylogeny** $\rightarrow$ **Construct/Test Maximum Likelihood Tree...**
2. Selected `aligned_sequences.meg`.
3. Configured **Test of Phylogeny** to **Bootstrap Method** with **1000 replicates**.
4. Clicked **Compute** to generate the tree.

### Step 5: Circular Tree Formatting & Graphic Export
1. Opened the tree inside MEGA12 **Tree Explorer**.
2. Clicked the **Radiation / Circular Layout** button on the top menu to display the tree radially[cite: 1].
3. Clicked **View** $\rightarrow$ **Show/Hide** and unchecked `Branch Lengths` to remove decimal numbers and keep labels clean[cite: 1].
4. Exported the image via **Image** $\rightarrow$ **Save as PNG Image** as `circular_tree.png`[cite: 1].

---

## 📜 License
This project is open-source and available under the **MIT License**.
