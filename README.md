# InhA_Drug_Discovery_QSAR
This project develops a reproducible QSAR pipeline to predict InhA inhibitor potency against *Mycobacterium tuberculosis*. ChEMBL bioactivity data were analyzed for chemical properties and drug-likeness, statistically compared, and used to train a Random Forest model with Morgan fingerprints for pIC50 prediction.
Overview

Tuberculosis remains the leading cause of infectious-disease mortality worldwide. Isoniazid, one of the two cornerstone first-line TB drugs, acts by inhibiting InhA (enoyl-[acyl-carrier-protein] reductase), a key enzyme in mycolic acid biosynthesis. This project builds a lightweight, fully reproducible, open-data pipeline to:

Curate bioactivity (IC50) data for InhA inhibitors directly from ChEMBL
Characterize the chemical space and drug-likeness (Lipinski) profile of active vs. inactive compounds
Statistically compare active/inactive compound properties (Mann–Whitney U)
Train a Random Forest QSAR model that predicts inhibitory potency (pIC50) directly from molecular structure (Morgan/ECFP4 fingerprints)

This is a companion project to an earlier comparative genomics analysis of rpoB (the target of rifampicin, TB's other first-line drug) across nine Mycobacterium species — together covering complementary computational approaches applied to both pillars of first-line TB chemotherapy.

Key Results
Metric	Value
Raw IC50 records retrieved (ChEMBL target CHEMBL1849)	488
Curated dataset	399 compounds (145 active / 140 inactive / 114 intermediate)
Significant descriptors (active vs. inactive, Mann–Whitney U, p ≤ 0.05)	pIC50, MW, NumHDonors, NumHAcceptors
Not significant	LogP (p = 0.435)
QSAR model (Random Forest, ECFP4 fingerprints)	Test R² = 0.65
Full write-up with methodology, literature review and discussion: report/InhA_QSAR_Project_Report.pdf
[InhA_QSAR_Project(Biogrademy).pdf](https://github.com/user-attachments/files/32795364/InhA_QSAR_Project.Biogrademy.pdf)
