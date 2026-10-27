# Muscle Contractility Lab — RYR1

**Name:** Obiñeta, Inah Marie  
**Date Completed:** October 27, 2026  
**Course:** Cell and Molecular Biology - B

## Assignment Details
**Gene:** 21. RYR1 — NM_000540.3:c.6617C>T (p.Thr2206Met) — ClinVar 12977 [missense]  
**Protein Accession:** NP_000531.2  
**Protein Length:** 5,038 amino acids

## Process — R Workflow

<img width="1871" height="902" alt="Screenshot 2026-10-28 001500" src="https://github.com/user-attachments/assets/2d718a24-7a93-4575-8e0f-9d0573a09cb8" />

**Figure 1.** RStudio environment showing complete script execution; no runtime errors, confirming the workflow runs successfully.

## Step 1 — Project Setup
gene_symbol = "RYR1"
transcript_accession = "NM_000540.3"
clinvar_id = "12977"
variant_protein = "p.Thr2206Met"

## Step 2 — NCBI Gene Record
- Gene symbol: RYR1
- NCBI Gene ID: 6261
- Official name: ryanodine receptor 1 (skeletal muscle)
- Chromosome: 19q13.2

## Step 3 — Protein Sequence
- NP accession: NP_000531.2
- FASTA file: https://github.com/iinahmariee/OBINETA-Muscle-Contractility-RYR1/blob/GROUP-4/data/RYR1%20Protein
- Full R script: https://github.com/iinahmariee/OBINETA-Muscle-Contractility-RYR1/blob/GROUP-4/analysis.R

## Step 4 — Amino‑Acid Composition

**Table 1.** Full amino‑acid composition of RYR1 (NP_000531.2; 5,038 amino acids)

| AminoAcid | Count |
|---|---|
| A | 384 |
| C | 100 |
| D | 253 |
| E | 476 |
| F | 207 |
| G | 363 |
| H | 133 |
| I | 203 |
| K | 228 |
| L | 558 |
| M | 145 |
| N | 170 |
| P | 271 |
| Q | 205 |
| R | 294 |
| S | 296 |
| T | 231 |
| V | 317 |
| W | 63 |
| Y | 141 |

**Top 3 Most Abundant Residues:**
1. Leucine (L) — 558
2. Glutamic acid (E) — 476
3. Alanine (A) — 384

*Note: Composition alone does not prove protein function or variant effect.*

<img width="2400" height="1500" alt="01_amino_acid_composition" src="https://github.com/user-attachments/assets/ba8a1f86-1115-47ca-82dc-1293be80dbd2" />

**Figure 2.** RYR1 amino‑acid composition showing abundance of charged and large hydrophobic residues consistent with a cytoplasmic ion‑channel structure.

## Step 5 — ClinVar Record (Variation 12977)

<img width="1917" height="847" alt="Screenshot 2026-10-28 001046" src="https://github.com/user-attachments/assets/fcffe5c9-1a18-4701-b9ce-3234587185db" />

**Figure 3.** ClinVar classification of RYR1 variant NM_000540.3:c.6617C>T (p.Thr2206Met), classified Pathogenic by expert panel.

## Step 6 — Second Biological Visualization

<img width="2400" height="750" alt="02_variant_position" src="https://github.com/user-attachments/assets/a2b2ff4a-0c69-4cb0-9830-6f392379e9dd" />

**Figure 4.** Variant position plot showing p.Thr2206Met at residue 2206 on the 5,038‑amino‑acid RYR1 reference protein.

---

## I. Questions & Answers

**1. What does your assigned gene encode, and how does this protein contribute to muscle function?**  
RYR1 encodes the ryanodine receptor 1, a large homotetrameric calcium‑release channel in the sarcoplasmic reticulum membrane of skeletal muscle. During excitation–contraction coupling: depolarization triggers RyR1 to open, releasing stored Ca²⁺ into the cytoplasm; Ca²⁺ binds troponin → actin–myosin cycling → contraction. Channel closure allows Ca²⁺ reuptake and relaxation. RyR1 regulates calcium signaling — it does not form contractile filaments directly.

**2. What was the exact protein accession and length retrieved with R?**
- Protein accession: NP_000531.2
- Length: 5,038 amino acids

**3. What did the amino‑acid composition chart show? What can it NOT tell you?**
- **Showed:** Leucine (L, 558) is most abundant, followed by Glutamic acid (E, 476) and Alanine (A, 384); high charged/polar residue content matches a large cytoplasmic‑facing ion channel structure (**Figure 2**, **Table 1**).
- **Cannot tell:** Protein folding, domain arrangement, gating behavior, or variant effect — composition alone does not predict molecular function or disease impact.

**4. What is your fixed ClinVar variant, and what is its current classification and evidence strength?**
- Variant: NM_000540.3(RYR1):c.6617C>T p.(Thr2206Met) — ClinVar ID 12977 (**Figure 3**)
- Classification: **Pathogenic**
- Evidence strength: Reviewed by ClinGen expert panel (March 2022); located in confirmed MH mutational hotspot; consistent clinical segregation; in silico predictors (SIFT=Damaging, PolyPhen‑2=Probably Damaging)

**5. What is the scientifically supported mechanism linking this variant to muscle function, and what remains uncertain?**
- **Mechanism:** p.Thr2206Met sits in the central cytoplasmic regulatory domain (residues 2163–2458 MH hotspot; **Figure 4**). Polar threonine → larger hydrophobic methionine destabilizes the closed channel state → resting Ca²⁺ leak from the sarcoplasmic reticulum. Under volatile anesthetics, this amplifies → uncontrolled Ca²⁺ release → muscle rigidity, hypermetabolism, hyperthermia (Malignant Hyperthermia crisis).
- **Uncertain:** Direct functional measurements specific to T2206M remain limited; whether the variant causes only gain‑of‑function (leak) or also partially impairs normal closure; exact structural interactions at residue 2206 are not fully resolved.

**6. What additional experiment would help test the proposed mechanism?**  
Express wild‑type and T2206M RyR1 in cells lacking endogenous ryanodine receptors. Use calcium imaging to measure resting cytosolic Ca²⁺ and responses to caffeine/halothane; compare single‑channel activity via patch‑clamp.  
**Expected:** T2206M channels show higher baseline open probability and exaggerated responses — confirming leaky gating.
