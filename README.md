# JASA Reproducibility Study
### Evaluating Reproducibility Practices in Statistical Research Software
 
A Master's capstone project at the University of California, Santa Cruz, systematically evaluating the reproducibility of computational research papers published in the Journal of the American Statistical Association (JASA) from 2020 to 2025.
 
---
 
## The Core Finding
 
**Only 30% of assessed papers met a moderate reproducibility threshold, despite data and code being publicly available for most of them.**
 
Artifact availability is not the same as reproducibility. A paper can share its code and data and still be impossible to reproduce if the environment is undocumented, dependencies are missing, or execution fails silently. This study quantifies exactly where that gap exists across 20 randomly selected JASA papers.
 
---
 
## What This Project Demonstrates
 
### Research Design
20 papers were selected using a true random number generator from JASA volumes 115-120 (2020-2025). Each paper was evaluated by actually attempting to execute the provided code, not just checking whether artifacts existed.
 
### Reproducibility Assessment Rubric
A five-indicator rubric was designed from scratch, with each indicator weighted to reflect its importance in the reproduction pipeline. See `REPRODUCIBILITY_RUBRIC.md` for the complete scoring criteria.
 
| Indicator | Weight |
|---|---|
| Data Availability | 15% |
| Code Accessibility | 15% |
| Code Executability | 30% |
| Documentation Completeness | 20% |
| Result Reproducibility | 20% |
 
Code Executability carries the highest weight because availability without executability is meaningless in practice.
 
### Technical Execution
All code was executed on an Apple MacBook Air (M3, macOS Sequoia) using R 4.5.0 and Python 3.13.5. Execution attempts included manual dependency resolution, environment setup, and result verification against published outputs.
 
### Critical Thinking
The rubric was validated by first running it against four JASA reproducibility award winners before applying it to the random sample. This dry run confirmed the rubric could distinguish between genuine reproducibility and artifact presence alone.
 
---
 
## Key Findings
 
### 1. Availability ≠ Reproducibility
Of the 16 evaluable papers, 9 had complete data availability and 10 had complete code accessibility. But only 3 achieved full code executability and only 2 reproduced results in full. Sharing artifacts is becoming common. Making them actually work is not.
 
### 2. The Most Common Failure Points
- Missing or undocumented dependencies
- No environment specification (no requirements.txt, no Dockerfile, no sessionInfo)
- Long runtimes with no checkpointing, causing crashes before completion
- Code that references objects or files not included in the supplemental materials
 
### 3. 2024 Papers Show Improvement
Three of the four highest-scoring papers in the study were published in 2024, suggesting a modest but meaningful shift toward better artifact packaging in recent JASA publications.
 
### 4. The Fix Is Not More Rules: It Is Better Incentives
The study concludes that compliance-based policies ("sticks") are insufficient. What drives reproducibility is recognition: badges, citation credit, and explicit rewards tied to executable, independently verified artifacts ("carrots").
 
---
 
## Scoring Results Summary
 
| Final Score Range | Number of Papers |
|---|---|
| 0.00 (no artifacts) | 6 papers |
| 0.40 - 0.59 | 4 papers |
| 0.60 - 0.79 | 2 papers |
| 0.80 - 1.00 | 4 papers |
 
Mean score: 0.41 | Median score: 0.48
 
---
 
## Files in This Repository
 
| File | Description |
|---|---|
| `Mrudula_Capstone_JASA_Reproducibility.pdf` | Full capstone paper including methodology, results, discussion and references |
| `REPRODUCIBILITY_RUBRIC.md` | The five-indicator scoring rubric with detailed 0/1/2 criteria for each indicator |
 
---
 
## About This Project
 
**Institution:** University of California, Santa Cruz

**Degree:** Master of Science in Computer Science and Engineering

**Advisor:** Professor Marcela Alfaro-Córdoba

**Completed:** October 2025

**GPA:** 3.96/4.0
 
---
 
## Author
 
**Mrudula Reddy Atla**
 
Dataset: JASA Volumes 115–120 (2020–2025)
Tools: R 4.5.0, Python 3.13.5, RStudio, VS Code
