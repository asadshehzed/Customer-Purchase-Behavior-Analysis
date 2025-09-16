# Customer Purchase Behavior Analysis

A small, practical project for exploring customer purchasing behavior from electronic sales data. The repository centers on a single Jupyter Notebook and a simple, reproducible workflow.

---

## Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## About the Project

This repository analyzes customer purchase behavior from a CSV of electronic sales (e.g., `Electronic_sales_Sep2023-Sep2024.csv`). The goal is a straightforward path: load data, clean and shape it, examine trends and segments, and establish simple baselines. It’s meant to be a sensible starting point for similar retail datasets.

---

## Features

- Reproducible exploratory analysis in a single Jupyter Notebook
- Basic feature engineering for customer and product-level insights
- Time-based trends and seasonality checks
- Segmentation-ready outputs (e.g., RFM-friendly fields)
- Lightweight plotting for quick iteration

---

## Getting Started

Prerequisites:

- Python 3.9+
- pip and a virtual environment tool (venv or conda)
- Jupyter (Notebook or Lab)

Clone and set up:

```bash
git clone https://github.com/USER/REPO.git
cd REPO

# Option A: venv
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
# source .venv/bin/activate

pip install -U pip
pip install -r requirements.txt
```

If `requirements.txt` is not present yet, install common packages and export later:

```bash
pip install pandas numpy matplotlib seaborn jupyter
pip freeze > requirements.txt
```

Run the notebook:

```bash
jupyter notebook "Customer Purchase Behavior Analysis.ipynb"
```

Optional: convert the notebook to a script and run it:

```bash
jupyter nbconvert --to script "Customer Purchase Behavior Analysis.ipynb"
python "Customer Purchase Behavior Analysis.py"
```

---

## Configuration

You can override paths with environment variables. Defaults are chosen to work out of the box.

| Variable     | Description                         | Default                                  |
|--------------|-------------------------------------|------------------------------------------|
| `DATA_PATH`  | Path to the input CSV               | `./Electronic_sales_Sep2023-Sep2024.csv` |
| `OUTPUT_DIR` | Directory for figures and artifacts | `./outputs`                              |

Example usage in Python:

```python
import os
DATA_PATH = os.getenv("DATA_PATH", "./Electronic_sales_Sep2023-Sep2024.csv")
OUTPUT_DIR = os.getenv("OUTPUT_DIR", "./outputs")
```

---

## Roadmap

- Add interactive dashboard (Streamlit or Plotly Dash)
- Implement RFM scoring and basic CLV estimation
- Add simple demand forecasting baseline
- Introduce data validation checks in CI

---

## Contributing

Contributions are welcome. A simple approach:

1. Fork the repository and create a feature branch.
2. Make focused changes with clear commit messages.
3. Ensure the notebook runs end-to-end without errors.
4. Open a pull request describing the change and rationale.

For larger changes, consider opening an issue first to discuss direction.

---

## License

This project is licensed under the MIT License. See `LICENSE` for details.

---

## Acknowledgements

- pandas, NumPy, Matplotlib, Seaborn
- Jupyter ecosystem
- Prior work in retail analytics and customer segmentation

