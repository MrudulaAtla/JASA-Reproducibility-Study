# Reproducibility Assessment Rubric

This rubric was developed for the JASA Reproducibility Study to systematically evaluate computational research papers. Each indicator is scored 0, 1, or 2. The final normalized score is computed using the weighted formula below.

---

## Scoring Formula

```
Final Score = (0.15 × DA) + (0.15 × CA) + (0.30 × CE) + (0.20 × DC) + (0.20 × RR)
              ────────────────────────────────────────────────────────────────────────
                                            2
```

Where:
- **DA** = Data Availability
- **CA** = Code Accessibility
- **CE** = Code Executability
- **DC** = Documentation Completeness
- **RR** = Result Reproducibility

The formula ensures the final score ranges from 0 to 1.

---

## Indicator Weights

| Indicator | Weight | Rationale |
|---|---|---|
| Data Availability | 15% | Foundational : without data, reproducibility is impossible |
| Code Accessibility | 15% | Foundational : without code, reproducibility is impossible |
| Code Executability | 30% | Highest weight : availability without executability is meaningless |
| Documentation Completeness | 20% | Often determines whether available code can actually be run |
| Result Reproducibility | 20% | Highest level of assurance : validates outputs against published results |

---

## Scoring Criteria

### Data Availability (DA)

| Score | Criteria |
|---|---|
| 0 | No data provided, or data is entirely inaccessible (e.g. proprietary without access, missing from supplementary materials) |
| 1 | Partial data availability : data provided but requiring special permissions or only examples included |
| 2 | Complete datasets provided, openly accessible, and clearly linked from the paper or supplementary materials |

---

### Code Accessibility (CA)

| Score | Criteria |
|---|---|
| 0 | No code provided or access restricted |
| 1 | Code is provided but incomplete (e.g. missing functions or scripts, references to unavailable repositories) or hosted in unstable locations |
| 2 | Full codebase provided, well-organized, openly accessible, and clearly linked from the paper |

---

### Code Executability (CE)

| Score | Criteria |
|---|---|
| 0 | Code fails to run due to missing dependencies, compilation errors, incompatible environments, or other fatal errors with no guidance to resolve issues |
| 1 | Code partially executes but requires manual fixes, undocumented dependencies, or non-trivial effort to resolve errors : some outputs may not match original results |
| 2 | Code executes successfully in the stated environment with minimal setup, producing outputs consistent with the expected workflow |

---

### Documentation Completeness (DC)

| Score | Criteria |
|---|---|
| 0 | No documentation or instructions provided |
| 1 | Limited documentation : a brief README without details on environment setup, execution order, or dependency versions |
| 2 | Comprehensive documentation provided, including environment specifications (e.g. requirements.txt, Dockerfile, sessionInfo), execution steps, and explanations of inputs and outputs |

---

### Result Reproducibility (RR)

| Score | Criteria |
|---|---|
| 0 | Results cannot be reproduced at all : outputs differ substantially or are missing (generally linked to code being unexecutable) |
| 1 | Partial reproducibility achieved : some figures, tables, or analyses can be reproduced but discrepancies remain compared to published results |
| 2 | Results are fully reproducible, with reproduced outputs matching those reported in the paper within expected tolerances |

---

## How to Apply This Rubric

1. Download all supplementary materials associated with the paper (datasets, code, documentation)
2. Score Data Availability and Code Accessibility before attempting execution
3. Attempt to execute the code in the environment specified by the authors
4. Score Code Executability based on whether execution succeeds, partially succeeds, or fails
5. Score Documentation Completeness based on whether the provided instructions were sufficient to attempt execution
6. Score Result Reproducibility based on whether reproduced outputs match published figures and tables
7. Apply the weighted formula to compute the final normalized score

---

## Validation

Before applying this rubric to the random sample, it was validated against four papers recognized as JASA reproducibility award winners. This dry run confirmed the rubric could reliably distinguish between genuine reproducibility and artifact presence alone, and that the 0/1/2 scoring criteria were specific enough to apply consistently across papers.
