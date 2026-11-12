# SPARE
Implementation of a preservation-aware sequential model editing framework for disaster-related social media classification, evaluated on HumAID, CrisisNLP, and CrisisLexT26 datasets.

# Preservation-Aware Sequential Model Editing for Disaster-Related Social Media Classification

## Overview

This repository contains the implementation and experimental evaluation of a preservation-aware sequential model editing approach for disaster-related social media classification.

The approach aims to correct misclassified instances while preserving previously acquired knowledge and minimizing unintended changes to correctly classified samples.

The experiments use **Qwen2.5-3B-Instruct** as the base language model and evaluate the approach across three disaster-related datasets.

## Datasets

The experiments are conducted on three datasets:

- **HumAID**
- **CrisisNLP**
- **CrisisLexT26**

Each dataset is evaluated separately using the same overall experimental framework.

## Repository Structure

The repository is organized into three dataset-specific directories:

```text
├── HumAID/
│   ├── 01_baseline.ipynb
│   ├── 02_ripple_protect.ipynb
│   ├── 03_fine_localization.ipynb
│   ├── 04_model_editing.ipynb
│   └── 05_evaluation.ipynb
│
├── CrisisNLP/
│   ├── 01_baseline.ipynb
│   ├── 02_ripple_protect.ipynb
│   ├── 03_fine_localization.ipynb
│   ├── 04_model_editing.ipynb
│   └── 05_evaluation.ipynb
│
├── CrisisLexT26/
│   ├── 01_baseline.ipynb
│   ├── 02_ripple_protect.ipynb
│   ├── 03_fine_localization.ipynb
│   ├── 04_model_editing.ipynb
│   └── 05_evaluation.ipynb
│
└── README.md
```

## Methodology

The experimental workflow consists of five main stages:

### 1. Baseline Evaluation

The base language model is evaluated on each dataset to identify correctly classified and misclassified instances before editing.

### 2. Ripple and Protection Set Construction

Misclassified instances are organized into label-specific ripple groups. Correctly classified instances are retained as a protection set to assess knowledge preservation during editing.

### 3. Fine-Grained Localization

Model components relevant to targeted corrections are identified to guide the editing process.

### 4. Sequential Model Editing

Targeted edits are applied sequentially to improve the model's predictions while limiting interference with previously correct behavior.

### 5. Evaluation

The edited model is evaluated to measure the effectiveness of corrections, generalization to related instances, retention of protected predictions, and unintended changes.


## Usage

The experimental notebooks are organized in the following order:

1. `01_baseline.ipynb`
2. `02_ripple_protect.ipynb`
3. `03_fine_localization.ipynb`
4. `04_model_editing.ipynb`
5. `05_evaluation.ipynb`

The experiments require a Python environment with the dependencies used in the notebooks, access to the base model, and the corresponding datasets.

**Note:** The notebooks represent stages of an interconnected experimental workflow. Some stages depend on intermediate files, variables, or model states produced by earlier stages. Additional environment and checkpoint configuration may be required when running notebooks independently.

## Research Purpose

This repository supports research on reliable model editing for disaster-related social media analysis, with an emphasis on improving targeted predictions while preserving existing model behavior.

## Citation

Citation information will be added when the associated research paper becomes available.
