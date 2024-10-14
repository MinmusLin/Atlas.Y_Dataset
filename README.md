# Atlas.Y Dataset

> Atlas.Y Dataset is licensed under the [Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license](https://creativecommons.org/licenses/by-nc/4.0). You are free to share and adapt the dataset for non-commercial purposes, as long as proper attribution is given. For commercial use, please [contact us](mailto:tongji_china2019@163.com) to request permission.

English | [简体中文](README_zh.md)

![](assets/Logo.png)

## Signal Peptide Dataset

The Signal Peptide Dataset is designed to facilitate research on protein subcellular localization and transport. Signal peptides are short sequences located at the N-terminus of newly synthesized proteins, responsible for determining the subcellular localization of these proteins. The data in this database is sourced from the dataset used in the development of the DeepLoc 2.1 deep learning model by Marius Thrane Ødum et al. To align with the goals of our project, we specifically filtered the dataset to include only proteins from eukaryotic organisms, extracted the signal peptides, categorized them, and assigned unique identifiers to enable efficient querying. This dataset is particularly suitable for bioinformatics research, protein design, and cell biology experiments focused on predicting subcellular localization.

[Signal_Peptide.csv](Signal_Peptide.csv)

## Linker Dataset

This Linker Dataset is designed to study the linkers between signal peptides and target proteins, assisting in the design and optimization of fusion proteins, particularly in research related to protein subcellular localization and transport. The dataset is divided into two tables: the Classical Linker Data Table and the Natural Linker Data Table.

* **Classical Linker Table**: This table contains linkers that have been extensively reviewed in the literature and categorized based on their rigidity and flexibility. The linker sequences in this table are suitable for use in protein design, molecular biology, and synthetic biology engineering projects.

  [Classical_Linker.csv](Classical_Linker.csv)

* **Natural Linker Table**: This table consists of short peptides derived from natural protein sequences without artificial optimization. These natural linkers are generated by removing signal peptides and conserved regions, following the method used by the 2021 Sun Yat-sen University iGEM team. We used protein sequences from the DeepLoc 2.1 dataset, and identified conserved regions using NCBI's Conserved Domain Database (CDD) and its Batch CD-Search tool.

  [Natural_Linker.csv](Natural_Linker.csv)

This dataset has broad applications, including protein engineering, molecular design, signal peptide function research, and bioinformatics analysis. The two tables in the dataset provide scientists with a foundational resource for efficiently querying and utilizing linker sequences.