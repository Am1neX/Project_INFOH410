# International Football Match Outcome Prediction

This project predicts international football match outcomes (`H`, `D`, `A`) using engineered rolling team-form features and three model families:

1. Naive Bayes
2. Random Forest, introduced through Decision Tree and Bagging
3. Neural Network (MLP)

The main playbook is the notebook at `notebooks/football_prediction.ipynb`.

## Setup

Create and activate the local virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the Python dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Register the virtual environment as a Jupyter kernel:

```bash
python -m ipykernel install --user --name infoh410-football --display-name "Python (INFOH410 Football)"
```

## Run The Notebook

Start JupyterLab:

```bash
jupyter lab notebooks/football_prediction.ipynb
```

In Jupyter, select the kernel named **Python (INFOH410 Football)**, then run the notebook cells from top to bottom.

## Data

The raw dataset is expected at:

```text
data/results.csv
```

The notebook creates processed train/test files in:

```text
data/processed/
```

These processed files are already present in the repository. the model section, reloads them directly so it can be rerun after the import/setup cells.

## Model Outputs

Running the notebook saves model artifacts under:

```text
models/
```

The Random Forest section saves its artifacts under:

```text
models/RandomForest/
```

## Troubleshooting

If you see `ModuleNotFoundError`, make sure the `.venv` is activated and that Jupyter is using the **Python (INFOH410 Football)** kernel.

If Jupyter is not available after installation, run:

```bash
source .venv/bin/activate
python -m pip install -r requirements.txt
```
