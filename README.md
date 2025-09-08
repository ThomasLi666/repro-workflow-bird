# NestBox Analytics — Reproducible Workflow

This repository contains a reproducible workflow for analyzing **bird movements at a nesting box**.  
The project demonstrates data preprocessing, exploratory analysis, visualization, and interpretation, with a strong focus on **reproducibility** and the **FAIR data principles**.

## Project Overview

- **Goal**: Study daily and seasonal bird activity patterns from nest box movement sensors.  
- **Core Questions**:
  - How do daily and seasonal movement patterns evolve?
  - Is there activity during dark hours?
  - How do first/last daily movements relate to sunrise and sunset?
  - What is the hourly activity distribution for specific days?
- **Data caveats**: corrupted partial counts, missing lines, flutter-induced overcounting (capped).

## Repository Structure

```
├── Final_NestBox_Reproducible_with_FAIR.ipynb   # Jupyter notebook with full workflow
├── environment.yml                              # Reproducible environment specification
├── outputs/                                     # Example outputs (tables, figures, metadata)
│   ├── figs/
│   ├── tables/
│   └── meta/
└── README.md                                    # This file
```

## Installation

Create a conda environment from the `environment.yml` file:

```bash
conda env create -f environment.yml
conda activate nestbox-workflow
```

Or install with pip (inside a virtual environment):

```bash
pip install -r requirements_freeze.txt
```

## Usage

Run the notebook step by step or execute all cells at once:

```bash
jupyter lab
```

Outputs (figures, tables, metadata) will be saved under `outputs/<run_id>/...` with a unique timestamp.

For parameterized runs, you can also use [papermill](https://papermill.readthedocs.io):

```bash
papermill Final_NestBox_Reproducible_with_FAIR.ipynb output.ipynb -p DATA_FILE bird_jan25jan16.txt
```

## FAIR Principles

This project is aligned with the FAIR principles:

- **Findable**: Repository with keywords (`birds`, `nestbox`, `reproducibility`, `FAIR`, `time series`).  
- **Accessible**: Open-source code and metadata, with instructions for data access.  
- **Interoperable**: Uses standard formats (CSV, PNG, JSON).  
- **Reusable**: Version-pinned environment and documentation ensure reusability.  

## Keywords

`birds`, `nestbox`, `activity monitoring`, `time series`, `reproducibility`, `FAIR`, `workflow`

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---
**Maintainer**: Your Name  
**Contact**: your.email@example.com
