# Paracetamol-Model
Whole-body PBPK model for paracetamol.

## Repository files
This repository contains:

- a PK-Sim snapshot (*.json) file of the current whole-body PBPK model of paracetamol. The current model corresponds to a modified version of Mian et al [1].
- static content (e.g. text blocks, *.md files) as inputs for an evaluation plan
- an evaluation plan (evaluation_plan.json) to create an evaluation report using the snapshot and static text blocks to display the performance of the model

The model was developed and evaluated for paracetamol using data from several clinical studies covering IV administration (equivalent dose range of 365 to 1460 mg) and oral administration (equivalent dose range 300 mg to 1460 mg in the fasted state or fed state). 

The PK-Sim snapshot file contains simulations and the observed data of all clinical studies used for model development and evaluation.

The presented model and evaluation focus on assessing the PBPK model performance for paracetamol. The model includes the main paracetamol metabolites—paracetamol glucuronide, paracetamol sulfate, methoxyacetaminophen, and NAPQI. Evaluation of the PBPK model’s predictive performance for these metabolites, particularly NAPQI and methoxyacetaminophen, would require further investigation.

## Code of conduct
Everyone interacting in the Open Systems Pharmacology community (codebases, issue trackers, chat rooms, mailing lists etc...) is expected to follow the Open Systems Pharmacology [code of conduct](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CODE_OF_CONDUCT.md#contributor-covenant-code-of-conduct).

## Contribution
We encourage contribution to the Open Systems Pharmacology community. Before getting started please read the [contribution guidelines](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CONTRIBUTING.md#ways-to-contribute). If you are contributing code, please be familiar with the [coding standard](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CODING_STANDARDS.md#visual-studio-settings).

## License
The model code is distributed under the [GPLv2 License](https://github.com/Open-Systems-Pharmacology/Suite/blob/develop/LICENSE).

## References
[1] Mian P, van den Anker JN, van Calsteren K, Annaert P, Tibboel D, Pfister M, Allegaert K, Dallmann A. Physiologically Based Pharmacokinetic Modeling to Characterize Acetaminophen Pharmacokinetics and N-Acetyl-p-Benzoquinone Imine (NAPQI) Formation in Non-Pregnant and Pregnant Women. Clin Pharmacokinet. 2020 Jan;59(1):97-110. doi: 10.1007/s40262-019-00799-5. 
