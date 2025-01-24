# G4 Benchmark Datasets for Intracellular G4 Sequencing Data

This repository contains five sets of benchmark datasets for G-quadruplex (G4) sequence data. Each dataset corresponds to a specific GEO accession number, representing the G4 sequence data from different test conditions.

## Overview

The benchmark datasets were generated through the following process:

1. **Peak Calling and Ranking**:  
   Multiple peak-calling algorithms were applied to each dataset. For each algorithm, the identified peaks were ranked based on their p-values or corresponding significance scores.

2. **Selection of Top Peaks**:  
   For each algorithm, the top 100, top 1,000, top 10,000, and top 100,000 G4 sites were selected based on confidence (ranked by p-values or significance scores).

3. **Merging Results**:  
   The results from different peak-calling algorithms were then merged into separate files corresponding to the respective numbers of top peaks:
   - `Top_merge_100_merge.bed` (Top 100 peaks)
   - `Top_merge_1000_merge.bed` (Top 1,000 peaks)
   - `Top_merge_10000_merge.bed` (Top 10,000 peaks)
   - `Top_merge_100000_merge.bed` (Top 100,000 peaks)

4. **Inclusion Criteria for Benchmark**:  
   A peak was included in the final benchmark if it was identified by more than half of the peak-calling algorithms applied to the dataset.

## Data Processing

- **GSE107690 and GSE145090**: These two datasets are single-end sequencing datasets and were processed using five peak-calling algorithms: MACS2, HOMER, SICER, PeakRanger, and GEM. The benchmark datasets for these two groups consist of G4 sites identified by at least two of the five algorithms.

- **GSE133379**: This dataset was processed using six peak-calling algorithms: MACS2, HOMER, SICER, PeakRanger, GEM, and GoPeaks. The corresponding benchmark dataset includes G4 sites identified by at least three of the six algorithms.

- **Other datasets**: These datasets were processed using seven peak-calling algorithms: MACS2, HOMER, SICER, PeakRanger, GEM, GoPeaks, and SEACR. The benchmark datasets for these groups consist of G4 sites identified by at least three of the five algorithms used.

## Purpose

This project aims to facilitate the comparison and evaluation of peak-calling algorithms for G4 sequence identification. It provides a valuable resource for researchers working on cellular G4 data, offering high-confidence G4 site data for further analysis.

By consolidating results from multiple algorithms, these benchmark datasets serve as a reliable reference for assessing the performance and reliability of G4 peak-calling methods.

## Maintainers and Contributors

- **Project Leads**: Yuqi Wang and Ke Xiao

## Acknowledgments

Special thanks to the authors of the peak calling algorithms (MACS2, HOMER, GEM, SICER, PeakRanger, GoPeaks, SEACR) for their work.  
We also acknowledge the researchers who contributed to the development of G4 biology and its computational analysis.  
Particular thanks to **Ke Xiao**, **Tiantong Tao**, **Rongxin Zhang**, **Huiling Shu**, and **Professor Xiao Sun** for their valuable contributions to this project.

