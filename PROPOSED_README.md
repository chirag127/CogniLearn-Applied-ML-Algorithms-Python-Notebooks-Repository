# 🧠 CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository

[![GitHub Stars](https://img.shields.io/github/stars/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository?style=flat-square&color=yellow)](https://github.com/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository)
[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository/ci.yml?style=flat-square)](https://github.com/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository?style=flat-square)](https://codecov.io/gh/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg?style=flat-square)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Python Version](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)](https://www.python.org/)

--- 

This repository serves as a definitive, curated archive of advanced Machine Learning and Artificial Intelligence algorithm implementations, meticulously documented within executable Jupyter Notebooks. **Accelerate your AI/ML journey** by leveraging robust, production-adjacent Python codebases for foundational and cutting-edge methodologies.

## 🏛️ Architecture Overview: Modular Documentation

This project utilizes a **Modular Documentation** structure, where each notebook functions as a self-contained module focusing on one core algorithm or architectural concept (e.g., Transformer Layer, GAN variant). The overall structure prioritizes clarity and executability over complex software coupling.

text
CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository/
├── algorithms/
│   ├── deep_learning/
│   │   ├── transformers_attention.ipynb
│   │   └── cnn_advanced_vision.ipynb
│   ├── classical_ml/
│   │   ├── svm_kernel_tricks.ipynb
│   │   └── boosting_xgboost_impl.ipynb
│   └── reinforcement_learning/
│       └── dqn_basics.ipynb
├── environment/
│   ├── environment.yml  # Conda setup for reproducibility
│   └── README.md        # Environment setup instructions
├── LICENSE
├── README.md
└── utils/
    └── plotting_helpers.py  # Standardized visualization utilities


## 📋 Table of Contents

1. [System Directives for AI Agents](#-system-directives-for-ai-agents-critical)
2. [Features & Methodologies](#features--methodologies)
3. [Apex Toolchain & Environment](#apex-toolchain--environment)
4. [Development & Verification](#development--verification)
5. [Contribution & Licensing](#contribution--licensing)

---

## 🤖 System Directives for AI Agents (CRITICAL)

<details>
<summary>⚙️ **APEX Agent Configuration: Python/Jupyter Environment**</summary>

### 1. Identity & Prime Directive (December 2025 Context)

**Role:** Senior Principal Architect. Your primary directive is to ensure the integrity, reproducibility, and intellectual quality of these educational ML assets. All modifications must adhere to the **Zero-Defect, High-Velocity, Future-Proof** philosophy.

**Context Anchor:** This repository is Python-based, utilizing Jupyter Notebooks (`.ipynb`). The environment must be managed via `Conda`/`Mamba` for dependency stability, as Runtimes are highly sensitive.

### 2. Apex Toolchain Definition (Scenario C: Data / AI / Scripts)

*   **Language Core:** Python 3.10+ enforced.
*   **Dependency Manager:** `Mamba`/`Conda` (or `uv` if migrating to pure Pip environment, though Conda is safer for notebook dependencies).
*   **Linting/Formatting:** **Ruff** is the mandated linter for any supporting Python scripts (`.py`). Notebook code cells should be manually reviewed against PEP 8, assuming the notebook renderer handles immediate cell syntax checks.
*   **Testing Framework:** **Pytest**. Unit tests (`test_*.py`) must validate *utility functions* and *model initialization logic* separately from the heavy matrix computations within the notebooks.
*   **AI Integration:** Assume interaction with external models requires robust API key management (via environment variables, **NEVER** hardcoded).

### 3. Architectural Patterns Enforced

*   **DRY (Don't Repeat Yourself):** Abstract common boilerplate (data loading, standard Keras/PyTorch layers, visualization setups) into the `./utils` directory.
*   **SOLID:** Ensure model classes (if implemented in Python modules) follow the Single Responsibility Principle (SRP). The notebook's role is integration and demonstration, not complex software design.
*   **Verification Command (Environment Setup):**
    bash
    # Use mamba for reliable package resolution
    mamba env create -f environment/environment.yml
    mamba activate cognilearn_env
    # Run static analysis on utilities
    ruff check ./utils
    # Run tests on utility layer
    pytest ./tests
    

### 4. Documentation Imperative

Every notebook must begin with a Level 1 (`#`) heading stating the algorithm's name and a Level 3 (`###`) heading detailing the core mathematical concept being demonstrated.

</details>

## ✨ Features & Methodologies

*   **Foundational Models:** Complete implementations of classical algorithms (SVM, Random Forests, Gradient Boosting).
*   **Deep Learning Constructs:** Detailed walk-throughs of CNN architectures, RNN variants, and modern Transformer blocks (e.g., Self-Attention mechanism).
*   **Reproducibility Focus:** All environments are strictly defined using the provided Conda specification file.
*   **Visualization Aids:** Utilities included for standardized plotting of loss curves, confusion matrices, and feature importance scores.

## 🛠️ Apex Toolchain & Environment

This repository mandates a sterile, reproducible environment suitable for complex ML dependencies.

### Environment Setup

1.  **Clone Repository:**
    bash
    git clone https://github.com/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository.git
    cd CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository
    

2.  **Create & Activate Environment (Mamba Recommended):**
    bash
    mamba env create -f environment/environment.yml
    mamba activate cognilearn_env
    

### Verification Scripts

| Task | Command | Description |
| :--- | :--- | :--- |
| **Environment Check** | `mamba list` | Verify installed packages match specification. |
| **Utility Linting** | `ruff check ./utils` | Enforce PEP 8 and modern Python standards on helper scripts. |
| **Run Tests** | `pytest` | Execute Pytest suite against utility layer. |
| **Notebook Health** | `jupyter nbconvert --to-script *.ipynb` | Quickly convert notebooks to scripts to check for syntax errors. |

## 🚀 Development & Verification

Contributions are welcome provided they adhere to the rigorous standards defined by the **Apex Agent Directives** above. Ensure any new notebook clearly explains the mathematical derivation before showing the code implementation.

### Development Principles

*   **YAGNI:** Only implement the complexity necessary to demonstrate the core concept. Avoid over-engineering the demonstration code.
*   **Modularity:** Keep notebook cell logic clean. Use helper functions from `./utils` extensively.

## ⚖️ Contribution & Licensing

This material is shared under the **Creative Commons Attribution-NonCommercial 4.0 International License**. Review the `LICENSE` file for full details. For collaboration guidelines, please see **`.github/CONTRIBUTING.md`**.
