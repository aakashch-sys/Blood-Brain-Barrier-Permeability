# Blood-Brain-Barrier-Permeability
ML-based blood-brain barrier (BBB) permeability prediction pipeline with downstream computational screening for Huntington's Disease drug candidates. Random Forest/Gradient Boosting models (AUC 0.942) trained on 9,400+ compounds from B3DB, BBBP &amp; ChEMBL, with CNS-MPO scoring and ADMET profiling.

# BBB-HD-Screen: Blood-Brain Barrier Permeability Predictor & Huntington's Disease Drug Screening Pipeline

A computational pharmacology pipeline that predicts blood-brain barrier (BBB) permeability of drug compounds using machine learning, and applies it to prioritise drug candidates for Huntington's Disease (HD).

## Overview

This project trains ensemble ML classifiers (Random Forest, Gradient Boosting) on RDKit molecular descriptors to predict whether a compound can cross the BBB — a key bottleneck in CNS drug development. The trained model is then used as a screening tool, combined with CNS drug-likeness scoring (CNS-MPO) and ADMET profiling, to rank candidate drugs for Huntington's Disease.

## Pipeline

1. **Data** — Consolidated 9,413 unique compounds from B3DB, BBBP, and curated ChEMBL data
2. **Feature engineering** — 197 RDKit physicochemical descriptors per molecule
3. **Model training** — Random Forest (AUC 0.942) vs. Gradient Boosting (AUC 0.921)
4. **Drug screening** — Applied to 30 FDA-approved/experimental HD-relevant compounds
5. **CNS-MPO scoring** — 6-property CNS drug-likeness assessment
6. **ADMET profiling** — Lipinski, Veber, hERG, AMES, PAINS, CYP inhibition filters + SwissADME validation
7. **Output** — Ranked shortlist of top HD drug candidates

## Results

- **Best model**: Random Forest — Accuracy 88.3%, AUC-ROC 0.942
- **Top candidates**: Memantine, Amantadine, Riluzole, Caffeine, Fluoxetine (among others)

## Tech Stack

Python · RDKit · scikit-learn · pandas · matplotlib/seaborn

## Status

Early-stage research project — next steps include molecular docking (AutoDock Vina) against the HTT protein and MD simulation.

## Disclaimer

This is a computational screening tool for research purposes only. Results require experimental and clinical validation before any therapeutic application.
