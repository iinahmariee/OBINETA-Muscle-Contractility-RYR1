# Muscle Contractility Lab — RYR1

**Name:** Obiñeta, Inah Marie  
**Date Completed:** October 28, 2026  
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

<img width="2400" height="1500" alt="01_amino_acid_composition" src="https://github.com/user-attachments/assets/ba8a1f86-1115-47ca-82dc-1293be80dbd2" />

**Figure 2.** RYR1 amino‑acid composition showing abundance of charged and large hydrophobic residues consistent with a cytoplasmic ion‑channel structure.

## Step 5 — ClinVar Record (Variation 12977)

<img width="1917" height="847" alt="Screenshot 2026-10-28 001046" src="https://github.com/user-attachments/assets/fcffe5c9-1a18-4701-b9ce-3234587185db" />

**Figure 3.** ClinVar classification of RYR1 variant NM_000540.3:c.6617C>T (p.Thr2206Met), classified Pathogenic by expert panel.

## Step 6 — Second Biological Visualization

<img width="2400" height="750" alt="02_variant_position" src="https://github.com/user-attachments/assets/a2b2ff4a-0c69-4cb0-9830-6f392379e9dd" />

**Figure 4.** Variant position plot showing p.Thr2206Met at residue 2206 on the 5,038‑amino‑acid RYR1 reference protein.

## Step 7 — Explain the Molecular Mechanism

**1. Describe what your normal protein does in skeletal, cardiac, or smooth muscle (as appropriate). Identify whether it drives the actin–myosin cycle, regulates calcium, or maintains muscle structure.**  
RYR1 encodes the skeletal muscle ryanodine receptor 1, a homotetrameric calcium‑release channel embedded in the sarcoplasmic reticulum membrane. Its primary role is to regulate calcium signaling during excitation–contraction coupling — it does not directly form the contractile machinery or maintain structural integrity.

**2. Explain what is known about the assigned variant, separating observed experimental evidence from computational prediction and clinical association.**

*Variant Evidence — p.Thr2206Met*
- **Clinical:** Classified Pathogenic by ClinGen expert panel; linked to Malignant Hyperthermia Susceptibility and central core disease 
- **Predictions:** SIFT/PolyPhen‑2 both call it damaging; sits in confirmed MH mutational hotspot (2163–2458)
- **Uncertain:** Direct functional tests specific to T2206M are limited; structural change not yet solved experimentally

**3. Write a short causal chain: gene → protein → molecular function → assigned variant → possible effect on contraction, relaxation, or muscle integrity.**  
RYR1 → RyR1 Ca²⁺ channel → E–C coupling → T2206M (Thr→Met at 2206) → closed state destabilized → resting Ca²⁺ leak → anesthetic trigger → uncontrolled Ca²⁺ release → Malignant Hyperthermia

**4. Propose one experiment that could test your interpretation, such as ATPase measurement, calcium imaging, binding assay, microscopy, or force measurement.**  
Express wild‑type and T2206M RYR1 in cells with no endogenous RyR. Use calcium imaging to measure resting Ca²⁺ levels and responses to caffeine/halothane; compare channel activity via patch‑clamp.  
**Expected:** T2206M shows higher baseline Ca²⁺ and exaggerated release, confirming leaky gating causes the phenotype.

---

## Questions to Answer in README.md

**1. What does your assigned gene encode, and how does this protein contribute to muscle function?**  
RYR1 encodes the ryanodine receptor 1, a large homotetrameric calcium‑release channel located in the sarcoplasmic reticulum membrane of skeletal muscle. During excitation–contraction coupling: depolarization triggers RyR1 to open, releasing stored Ca²⁺ into the cytoplasm; Ca²⁺ binds troponin → actin–myosin cycling → contraction. Channel closure allows Ca²⁺ reuptake and relaxation. RyR1 regulates calcium signaling — it does not form the contractile filaments directly.

**2. What was the exact protein accession and length retrieved with R?**
- Protein accession: NP_000531.2
- Length: 5,038 amino acids

**3. What did the amino‑acid composition chart show? What can it NOT tell you?**
- **Showed:** Leucine (L, 558) is most abundant, followed by Glutamic acid (E, 476) and Alanine (A, 384); high content of charged/polar residues consistent with a large cytoplasmic‑facing ion channel structure.
- **Cannot tell:** Folding, domain arrangement, gating behavior, or variant effect — composition alone does not predict molecular function or disease impact.

**4. What is your fixed ClinVar variant, and what is its current classification and evidence strength?**
- **Variant:** NM_000540.3(RYR1):c.6617C>T p.(Thr2206Met) — ClinVar ID 12977 
- **Classification:** Pathogenic
- **Evidence strength:** Reviewed by ClinGen expert panel (March 2022); located in confirmed MH mutational hotspot; consistent clinical segregation; in silico predictors (SIFT=Damaging, PolyPhen‑2=Probably Damaging)

**5. What is the scientifically supported mechanism linking this variant to muscle function, and what remains uncertain?**
- **Mechanism:** p.Thr2206Met sits in the central cytoplasmic regulatory domain (residues 2163–2458 MH hotspot; **Figure 4**). Polar threonine → larger hydrophobic methionine destabilizes the closed channel state, causing resting Ca²⁺ leak from the sarcoplasmic reticulum. Under volatile anesthetics, this amplifies → uncontrolled Ca²⁺ release → muscle rigidity, hypermetabolism, hyperthermia (Malignant Hyperthermia crisis).
- **Uncertain:** Direct functional measurements specific to T2206M remain limited; whether the variant causes only gain‑of‑function (leak) or also partially impairs normal closure; exact structural interactions at residue 2206 are not fully resolved.

**6. What additional experiment would help test the proposed mechanism?**  
Express wild‑type and T2206M RyR1 in cells lacking endogenous ryanodine receptors. Use calcium imaging to measure resting cytosolic Ca²⁺ and responses to caffeine/halothane; compare single‑channel activity via patch‑clamp.  
**Expected result:** T2206M channels show higher baseline open probability and exaggerated responses — directly confirming the leaky gating mechanism.

## Discussions 
The p.Thr2206Met variant in RYR1 is a good example of how a tiny change in a protein can end up mattering for a patient. To understand it properly, though, it helps to keep three kinds of evidence separate: what has been shown in experiments, what has been seen in patients, and what computer programs predict.

On the side changes in the part of the protein known as the central cytoplasmic regulatory domain near residue 2206 seem to make it harder for the channel to stay closed. The result is a steady leak of calcium out of the sarcoplasmic reticulum. In studies using cells channels with this change open often even when calcium is at normal levels and they respond too strongly to triggers such as caffeine or volatile anesthetics. The likely explanation is that swapping a polar threonine for a bulkier hydrophobic methionine disrupts how nearby parts of the protein fit together. This disruption weakens the contacts that normally keep the channel closed. However direct tests of T2206M itself are still limited so part of this picture comes from changes.

Clinically, the link is much clearer. p.Thr2206Met is strongly associated with malignant hyperthermia susceptibility (MHS), a condition where certain anesthetics or muscle relaxants can set off a dangerous, runaway reaction. Most carriers are perfectly fine day to day and only run into trouble during anesthesia. The variant has turned up in several unrelated patients and tracks with the condition within families, which is a big reason it is classified as pathogenic. It isn’t fully penetrant, though, since some carriers never have an episode. It also isn’t tied to ongoing muscle weakness, which sets it apart from the RYR1 variants that cause congenital myopathies.

inally the computer predictions all point the way. SIFT labels the change as damaging PolyPhen-2 labels it as damaging and structural models suggest it breaks the protein’s shape. These tools agree with the lab and clinical findings. On their own they are only predictions, not proof. Taken together the three lines of evidence make a case that T2206M is a functionally important MHS variant. Whether someone actually reacts depends on exposure to triggers and probably, on genetic factors.


## References Link:
ClinVar: https://www.ncbi.nlm.nih.gov/clinvar/variation/12977/ 

NCBI Gene: https://www.ncbi.nlm.nih.gov/gene/6261

NCBI Protein: https://www.ncbi.nlm.nih.gov/protein/NP_000531.2
