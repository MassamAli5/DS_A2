# DS-A2 — AI-Use and Independent-Verification Log

**Project:** Inference and Uncertainty in Sedimentary Phosphorite Geochemistry

**Source:** Ali et al. (2026), *Journal of Asian Earth Sciences*. DOI: 10.1016/j.jseaes.2025.106927.

**AI tool:** OpenAI ChatGPT

**Purpose:** To document the limited use of AI for coding assistance and computational troubleshooting during the analysis.

## 1. Scope of AI Assistance

ChatGPT was used only as a coding and troubleshooting aid.

The assistance included:

- Helping identify and resolve Python coding errors.
- Providing coding syntax and implementation suggestions when needed.
- Troubleshooting issues encountered while running the analysis in Jupyter Notebook and VS Code.
- Helping diagnose computational or package-related errors.
- Clarifying how specific Python functions or code operations work.

The research questions, analytical approach, statistical methods, data interpretation, and scientific conclusions were determined by the researcher. AI-generated code or suggestions were reviewed and tested before use.

## 2. Computational Analysis

All analyses were designed, executed, and inspected by the researcher. These included:

| Task | Analysis performed | Verification |
|---|---|---|
| Bulk-rock mean comparison | Welch unequal-variance confidence interval | Manually calculated limits compared with SciPy |
| Sampling-distribution demonstration | Fixed-seed parametric Monte Carlo simulation | Simulated variability compared with theoretical standard error |
| Study A uncertainty | Within-group nonparametric percentile bootstrap | Results independently checked against the selected analytical framework |
| Statistical power | Monte Carlo Welch tests across sample sizes, effects, and noise levels | Exported simulation results reloaded and checked |
| In situ apatite uncertainty | Parent-level summaries and layer-stratified cluster bootstrap | Parent-rock hierarchy examined; incomplete resamples recorded |
| Assumption counterexample | Paired synthetic parent-rock simulation | Empirical rejection rates and coverage estimated over 2,000 experiments |
| Reproducibility | Fixed random seeds and dependency recording | Restart-and-run-all check completed in VS Code |

## 3. Independent Verification

The following checks were performed by the researcher:

1. The original supplementary workbook was inspected, including six selected records covering the three stratigraphic layers across Tables S1 and S2.
2. Source-table stratigraphic group boundaries were examined.
3. Manually calculated Welch 95% confidence intervals were compared with SciPy's unequal-variance t-test confidence intervals.
4. Power-simulation results were exported as CSV files and reloaded for comparison.
5. Synthetic-counterexample results were exported and reloaded for comparison.
6. Random seeds and scientific Python package versions were recorded.
7. The notebook was executed from a restarted Jupyter kernel in VS Code without reported errors.
8. The scientific method note was exported to PDF, and equation rendering was visually checked.

These checks support computational reproducibility and internal consistency but do not establish the validity of all geological sampling assumptions.

## 4. Limitations and Outstanding Verification

- The six source records were selected for layer coverage rather than randomly.
- A separate direct programmatic comparison of those records against processed dataframes has not yet been documented.
- Parent-sample identifier interpretation has not been independently confirmed against original laboratory notebooks.
- Independent reproduction on a second computer has not been demonstrated.
- Historical failed runs have not been comprehensively archived.
- The Study B bootstrap percentile interval is based on 9,977 complete repetitions; 23 incomplete repetitions were excluded and reported.
- The analyses are observational and retrospective. Statistical intervals do not establish geological causation or sampling representativeness.

## 5. AI Responsibility Statement

ChatGPT was used as a technical coding and troubleshooting resource. It did not determine the research questions, select the scientific methodology, interpret the geological significance of the results, or make the final analytical decisions.

The researcher was responsible for the data, analysis design, code execution, verification of outputs, statistical interpretation, geological interpretation, and final conclusions. AI-generated coding suggestions were treated as unverified until tested and checked by the researcher.

## 6. Reproducibility Records

The submission repository contains:

- `DS-A2_data_foundation.ipynb` — Executable analysis notebook.
- `Supplementary file.xlsx` — Original published supplementary dataset.
- `requirements.txt` and `requirements-lock.txt` — Dependency information.
- `results/` — Saved power and counterexample simulation results.
- `figures/` — Statistical visualizations.
- `docs/Method_Note.md` and `docs/Method_Note.pdf` — Scientific method and derivation note.
- `docs/AI_Verification_Log.md` — AI-use and verification record.

Repository version information and submission links will be recorded after GitHub publication.
