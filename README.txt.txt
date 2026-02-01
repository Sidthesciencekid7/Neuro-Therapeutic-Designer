# The Neuro-Therapeutic Designer

## Project Overview
The **Neuro-Therapeutic Designer** is a Machine Learning tool designed to screen potential drug candidates for their ability to cross the **Blood-Brain Barrier (BBB)**.

By analyzing the physicochemical properties of a molecule (Lipophilicity, Molecular Weight, TPSA, H-Donors), this tool predicts whether a compound can successfully enter the brain to treat neurological conditions.

## Key Features
* **Predictive Modeling:** Uses a Random Forest Classifier trained on the MoleculeNet BBBP dataset (2,000+ compounds).
* **Cheminformatics Engine:** Integrates **RDKit** to convert raw SMILES strings into quantitative molecular descriptors.
* **Hybrid Safety Protocols:** Implements "Human-in-the-Loop" engineering constraints (e.g., blocking molecules >400 Da) to prevent false positives.
* **Case Study:** Successfully identified **Curcumin Difluoride** as a high-potency analog (100% confidence) for potential Alzheimer's treatment, compared to generic Curcumin (<50% confidence).

## Tech Stack
* **Language:** Python
* **Machine Learning:** Scikit-Learn (Random Forest)
* **Chemistry:** RDKit
* **Interface:** ipywidgets (Interactive Dashboard)

## Results
* **Accuracy:** 85.5% on Test Set
* **False Positive Rate:** <15%
* **Key Finding:** Fluorination of Curcumin significantly increases predicted BBB permeability due to optimized lipophilicity without violating molecular weight constraints.

## How to Run
1. Install dependencies:
   `pip install -r requirements.txt`
2. Run the notebook or script to launch the dashboard.
3. Enter a SMILES string (e.g., Aspirin or Curcumin) to see the prediction.