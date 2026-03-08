# Scoring Weights & Rationale Documentation
## HIV-1 Protease Drug Discovery Pipeline

This document explains the technical and scientific basis for the **weighted composite scoring system** used to rank potential drug candidates in the DENOVO-HIV project.

---

## ⚖️ Weight Distribution Overview

The final composite score is calculated by normalizing each metric to a 0-1 scale and applying the following weights:

| Metric | Weight | Category | Primary Goal |
| :--- | :--- | :--- | :--- |
| **Molecular Docking** | **30%** | Efficacy | Binding Affinity (kcal/mol) |
| **ADMET (QED)** | **25%** | Safety | Drug-likeness & Bioavailability |
| **AI Prediction Score** | **20%** | Structural | Model Confidence & Relevance |
| **Synthesizability (SA)** | **15%** | Feasibility | Manufacturing Ease |
| **HOMO-LUMO Gap** | **10%** | Stability | Electronic Stability & Reactivity |

---

## 🔍 Detailed Rationale

### 1. Molecular Docking (30%) – *The "Efficacy" Priority*
*   **Basis:** This is the most direct measure of **Target Engagement**.
*   **Rationale:** In structural drug design, the primary goal is to ensure the molecule actually fits into the active site of the HIV-1 Protease enzyme. If it doesn't bind strongly (measured in kcal/mol), the drug won't work regardless of how stable or easy it is to make. 
*   **Threshold:** Scores below **-8.0 kcal/mol** are generally considered strong inhibitors for this target.

### 2. ADMET / QED (25%) – *The "Safety" Priority*
*   **Basis:** **Clinical Viability** (Absorption, Distribution, Metabolism, Excretion, and Toxicity).
*   **Rationale:** "Good chemistry ≠ Good drug." Many molecules bind well in a lab but fail in humans because they are toxic or don't dissolve. The **Quantitative Estimation of Drug-Likeness (QED)** score integrates Lipinski’s rules and other pharmacokinetic factors.
*   **Threshold:** A QED score above **0.50** indicates high drug-likeness.

### 3. AI Prediction Score (20%) – *The "Scientific Sanity" Priority*
*   **Basis:** **Structural Relevance**.
*   **Rationale:** This represents how confident the LSTM neural network is that the generated structure aligns with the chemical grammar of known HIV drugs. It serves as a pattern-matching validation against the 9,480 molecules in the training set.

### 4. Synthesizability / SA Score (15%) – *The "Practical Feasibility" Priority*
*   **Basis:** **Manufacturing Difficulty**.
*   **Rationale:** This metric prevents the selection of "fantasy molecules" that are mathematically sound but impossible to synthesize in a laboratory. It considers fragment frequency and structural complexity.
*   **Threshold:** An SA Score below **5.0** is considered practically synthesizable.

### 5. HOMO-LUMO Gap (10%) – *The "Fine-Tuning" Priority*
*   **Basis:** **Electronic Stability**.
*   **Rationale:** Calculated via quantum chemistry (Hartree-Fock), this gap measures the energy difference between frontier orbitals. It is a secondary indicator of reactivity and long-term chemical stability.

---

## ⚖️ Why do the weights vary?

The weights are not equal because **every metric has a different impact on the failure rate** of a drug discovery project. In pharmaceutical R&D, we prioritize metrics that represent "Project Killers"—factors that, if they fail, make it scientifically impossible for the drug to ever reach the market.

### 1. High Impact Metrics (30% - 25%): The "Must-Haves"
*   **Docking (30%):** Because efficacy is non-negotiable. A drug that doesn't bind to HIV Protease is not a drug, just an expensive chemical. It has the highest weight because it determines the **fundamental purpose** of the molecule.
*   **ADMET (25%):** Because safety is the #2 reason drugs fail in clinical trials. A drug that works but is toxic or doesn't dissolve will never be approved. We weight this almost as high as docking to ensure our "winners" are safe for humans.

### 2. Medium Impact Metrics (20%): The "Validation"
*   **AI Prediction (20%):** This validates if the molecule "looks like" a drug based on 9,000+ historical examples. It is important, but we trust **physical simulation (Docking)** more than **pattern matching (AI)**, which is why it is weighted lower than Docking.

### 3. Low Impact Metrics (15% - 10%): The "Optimization"
*   **Synthesizability (15%):** Difficulty in making a drug is a **challenge of cost and time**, not a scientific dead-end. Unlike "No Binding" (Docking), which is a hard "No," high synthetic complexity is just a hurdle that can often be solved with more research.
*   **HOMO-LUMO Gap (10%):** Electronic stability is a **fine-tuning** metric. While it helps predict reactivity, a molecule with a sub-optimal gap might still be a great drug. It is used as a tie-breaker rather than a primary filter.

---

## 🏁 Conclusion
The weights are intentionally skewed toward **Docking and ADMET** because efficacy (working) and safety (not killing the patient) are the two most common reasons for drug failure in the pharmaceutical industry. This balanced approach ensures the final recommended candidate is robust, safe, and realistic.
