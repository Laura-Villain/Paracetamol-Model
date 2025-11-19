### Absorption <a id="model-parameters-and-assumptions-absorption"></a>

The solubility of paracetamol and its metabolites was taken from previously published PBPK model [Mian 2020](#main-references) (see [Section 2.2.1](#invitro-and-physico-chemical-data)).

Paracetamol is a highly-soluble compound, therefore, for most studies dissolution was modeled as a dissolved formulation. However, a few studies containing Tablets, Capsules or Modified-release Tablets used an optimized empirical Weibull dissolution approach.

### Distribution <a id="model-parameters-and-assumptions-distribution"></a>

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim, observed clinical data was best described by choosing the partition coefficient calculation by `Rodgers and Rowland` and cellular permeability calculation by `PK-Sim Standard`. 

### Metabolism and Elimination <a id="model-parameters-and-assumptions-metabolism-and-elimination"></a>

Clearance of paracetamol was described through enzymatic pathways either with Michaelis Menten Kinetics or Specific clearance, with only a negligible contribution from renal excretion of unchanged parent drug  ([Mian 2020](#main-references)). In vivo, isoenzymes of the Cytochrome P-450 (CYP), UDP-glucuronosyltransferase (UGT), and cytosolic sulfotransferases (SULT) enzyme families contribute to the hepatic metabolism of paracetamol with approximately 8 %, 58 %, and 30 %, respectively ([Clements 1984](#main-references),([Jiang 2013](#main-references)),([Johnson 2018](#main-references)),([Mian 2020](#main-references)). CYP enzymes were implemented as CYP1A2, CYP2C19, CYP2C9, CYP3A4, CYP2E1 and CYP2D6. SULT was implemented as a lumped process representing metabolism from SULT1A1, SULT1A2, SULT1A3 and SULT2A1. SULT2A1 was used to characterize the expression profile of the lumped SULT metabolism, representing an assumption of liver as the major organ governing SULT-related metabolism. The expression profiles for these enzymes were loaded from the [PK-Sim Ontogeny Database Version 7.3](#main-references)) using RT-PCR as data source for each enzyme, except for the reduced relative expression of CYP2C19 in gut was described (see evaluation report of omeprazole for more details). The fraction of drug eliminated unchanged in urine is expected to be approximately 0.04 ([Mian 2020](#main-references)). `Km` and `Vmax` were simultaneously fitted to in vivo pharmacokinetic data of healthy subjects to describe the contribution of each biotransformation pathway to overall elimination ([Mian 2020](#main-references)). The fraction of paracetamol metabolites eliminated unchanged in urine is expected to be 1 ([Mian 2020](#main-references)).

### Automated Parameter Identification <a id="model-parameters-and-assumptions-parameter-identification"></a>

This is the result of the final parameter identification.

| Model Parameter      | Optimized Value | Unit |
| -------------------- | --------------- | ---- |
| **Paracetamol** |  |  |
| `GFR Fraction` |       0.19          |     |
| `Km UGT1A1` |       462.00          |  μmol/l    |
| `Vmax UGT1A1` |     37.19            |  μmol/l/min    |
| `Km SULT1A1` |       115.00          |  μmol/l    |
| `Vmax SULT1A1` |     9.62            |  μmol/l/min    |
| `Km CYP3A4` |       130.00          |  μM   |
| `Vmax CYP3A4` |     0.49            |  1/min    |
| `Specific clearance CYP2E1` |   0.0057             |  1/min  |
| `Km CYP1A2` |       220.00          |  μM   |
| `Vmax CYP1A2` |     0.56            |  1/min    |
| `Km CYP2C9` |       660.00          |  μM   |
| `Vmax CYP2C9` |     0.11            |  1/min    |
| `Km CYP2C19` |       2000.00          |  μM   |
| `Vmax CYP2C19` |     1.48            |  1/min    |
| `Km CYP2D6` |       440.00          |  μM   |
| `Vmax CYP2D6` |     0.56            |  1/min    |
| **Paracetamol glucuronide** |  |  |
| `Specific clearance for tubular secretion` | 0.352  | mL/min per ml tissue |
| `Specific clearance for tubular secretion` | 0.352  | 1/min per ml tissue |
| **Paracetamol sulfate** |  |  |
| `Km Renal Clearance` | 41.4 |  μmol/l  |
| `TSmax_spec` |  82.93 |  μmol/l/min |
| **Methoxyacetaminophen** and **NAPQI**|  |  |
| `Specific clearance for tubular secretion` | 22.85  | 1/min per ml tissue |

TSmax_spec stands for specific maximum rate for tubular secretion