# Architecting for Action: Data Lineage and Analysis via the T-DAR Framework

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22905116.svg)](https://doi.org/10.5281/zenodo.22905116)

This repository contains the LaTeX source code, figures, and related diagrams for the paper introducing the **T-DAR (Targeted Data-Actions-Results)** framework. T-DAR is a methodology designed for analyzing data lineage and ensuring actionable insights within complex data ecosystems.

While modern observability platforms excel at detecting anomalies, and lineage tools like OpenLineage build comprehensive dependency graphs, they often lack a native mechanism to track subsequent interventions. The T-DAR framework bridges this gap by providing an active, programmatic governance loop that links issues directly to the data ecosystem.

## Core Concepts

The framework relies on two primary entities:

- **DAREntry**: An immutable log event categorized into three phases:
  - **Data (D)**: The factual snapshot or metric collected (The Assessment).
  - **Action (A)**: The specific intervention taken in response to the data.
  - **Result (R)**: The outcome or consequence of the action.
- **Targeted Observation**: A stateful container that groups DAREntries into a chronological sequence, strictly bound to a specific polymorphic Data Asset (ranging from a database to a single column).

## PDF Export

Download the compiled PDF of the paper from the following link:
[Architecting for Action: Data Lineage and Analysis via the T-DAR Framework](https://github.com/xFufly/tdar-lineage/releases/latest)

## Repository Structure

- `main.tex`: The main LaTeX source file of the paper.
- `uml/`: Contains the PlantUML source files used to generate the architectural and state machine diagrams.
  - `tdar_architecture.puml`: UML class diagram of the framework.
  - `tdar_state.puml`: State machine diagram for the Targeted Observation lifecycle.
  - `tdar_case_study.puml`: Object diagram illustrating a Medallion Architecture use case.
- `out/`: Contains the generated outputs (e.g., LaTeX exports from PlantUML).
- `inspiration/`: Reference materials and foundational papers (e.g., the DAR nursing standard).

## Compilation Instructions

To compile the paper into a PDF, you will need a standard TeX distribution (such as TeX Live, MacTeX, or MiKTeX) with the `pdflatex` engine.

Run the following command in the root directory:

```bash
pdflatex main.tex
pdflatex main.tex
```

Note: Running the compilation command twice ensures that all internal citations and bibliography references are correctly linked.

## Author

[DIDELOT Tim](https://timdidelot.fr/)

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](LICENSE).

## How to Cite

If you use this framework in your research, please cite:

```bibtex
@article{didelot2026tdar,
  author       = {Didelot, Tim},
  title        = {Architecting for Action: Data Lineage and Analysis via the T-DAR Framework},
  year         = 2026,
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.22905116},
  url          = {https://doi.org/10.5281/zenodo.22905116}
}
```
