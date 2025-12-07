# 🔱 Contributing to CogniLearn: Applied ML Algorithms Repository

Welcome to the **CogniLearn** initiative! As an Apex Technical Authority, we maintain a zero-defect standard for all ML model implementations and documentation. Your contributions are vital to advancing this shared knowledge base for cutting-edge AI methodologies.

By participating, you agree to uphold our [Code of Conduct](https://github.com/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository/blob/main/CODE_OF_CONDUCT.md).

## 1. ⚙️ Getting Started: Development Environment Setup

This repository leverages the robust Python data science ecosystem, primarily focusing on Jupyter Notebooks. We mandate the use of `uv` for resilient dependency management and strict reproducibility.

### Prerequisites
*   Python 3.10+
*   Git
*   `uv` (Installed globally: `pip install uv`)

### Local Setup

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository.git
    cd CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository
    
2.  **Synchronize Dependencies:** Use `uv` to create the virtual environment and install all dependencies (including development tools) from `pyproject.toml`.
    bash
    uv sync
    
3.  **Activate Environment:**
    bash
    source .venv/bin/activate  # Linux/macOS
    .venv\Scripts\activate     # Windows
    

## 2. 🛡️ Development Standards & Code Quality

We strictly enforce quality controls using `Ruff` for consistency and readability across all Python files and utility scripts. Maintaining clear, reproducible notebooks is paramount.

### Code Formatting and Linting

Before submitting any changes, you **must** run the formatter and linter to ensure compliance with Apex standards:

bash
# Auto-format code using Ruff
uv run ruff format .

# Check for linting errors and apply fixes
uv run ruff check . --fix


### Notebook Integrity

1.  **Readability:** Ensure all code cells are clean, utilize type hints where applicable, and are logically ordered.
2.  **Documentation:** Every notebook must include thorough Markdown documentation explaining the algorithm's theory, implementation decisions, and results.
3.  **Reproducibility:** Notebooks should be saved with **cleared output cells** (unless the output is a necessary baseline visualization). They must run successfully top-to-bottom.
4.  **Data Policy:** Avoid committing large datasets. Prefer synthetic data generation or documented external download instructions.

## 3. 🐛 Reporting Issues and Suggestions

We use dedicated templates to streamline triage and ensure rapid response.

### 🐞 Bug Reports

If you find an error or unexpected result in an existing algorithm or script:

1.  Search existing issues to prevent duplication.
2.  Use the [Bug Report Template](https://github.com/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository/issues/new?assignees=chirag127&labels=bug%2C+triage-required&template=bug_report.md&title=%5BBUG%5D%3A+).
3.  Provide full traceback, steps to reproduce, and environment details (`Python version`, `uv list`).

### ✨ Enhancement and Algorithm Suggestions

For proposing new ML algorithms, models, or architectural changes, open a standard issue detailing the proposed addition and its value proposition to the data science community.

## 4. 🚀 Pull Request Protocol (PRs)

All contributions must adhere to the following protocol to ensure high-velocity integration:

1.  **Fork** the repository and create your feature branch (`git checkout -b feat/new-model-implementation`).
2.  Ensure your changes pass all mandated linting and formatting checks.
3.  Push your changes to your fork.
4.  Open a Pull Request targeting the `main` branch.
5.  **Use the [PR Template](https://github.com/chirag127/CogniLearn-Applied-ML-Algorithms-Python-Notebooks-Repository/compare?expand=1) provided.** Fill out all sections detailing the changes, model parameters, and verification steps.

### Conventional Commit Standard

We enforce the Conventional Commits specification for automated changelog generation and clarity. Commits must be atomic.

| Type | Description | Example
| :--- | :--- | :---
| `feat:` | A new algorithm, model, or major functional improvement. | `feat: implement k-means clustering notebook`
| `fix:` | Correction of a bug, calculation error, or dependency issue. | `fix: corrected batch size calculation in CNN script`
| `docs:`| Changes only to documentation (Markdown or Notebook text). | `docs: updated algorithm theory section in decision_tree.ipynb`
| `chore:`| Updates to tooling, CI configuration, or dependency versions. | `chore: upgrade numpy dependency via uv`
| `refactor:`| Restructuring code without changing external behavior. | `refactor: extracted data loading utility into helper script`