# International Football Match Outcome Prediction
 
Project for the INFO-H410 course at the École Polytechnique de Bruxelles, ULB.
 
We compare three AI techniques to predict the outcome of international football matches (`H` = home win, `D` = draw, `A` = away win) using the same engineered rolling team-form features:
 
1. Naive Bayes
2. Random Forest (introduced through Decision Tree and Bagging)
3. Multi-Layer Perceptron (MLP)

The full pipeline lives in `notebooks/football_prediction.ipynb`.
 
 
## Setup
 
Create and activate a virtual environment:
 
```bash
python3 -m venv .venv
source .venv/bin/activate
```
 
Install the dependencies:
 
```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```
 
Register the kernel for Jupyter:
 
```bash
python -m ipykernel install --user --name infoh410-football --display-name "Python (INFOH410 Football)"
```
 
 
## Run the notebook
 
```bash
jupyter lab notebooks/football_prediction.ipynb
```
 
In Jupyter, select the kernel **Python (INFOH410 Football)** and run the cells from top to bottom.
 
 
## Data
 
The raw dataset is expected at `data/results.csv`. The processed train, validation and test splits used by the notebook are already provided in `data/processed/`.
 
 
## Troubleshooting
 
If you get a `ModuleNotFoundError`, make sure the virtual environment is activated and that Jupyter is using the **Python (INFOH410 Football)** kernel.
 
If Jupyter is not available after installation, reactivate the environment and reinstall:
 
```bash
source .venv/bin/activate
python -m pip install -r requirements.txt
```
 
