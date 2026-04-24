# Intersectional Fairness in Machine Learning: An Analysis Using Oxonfair.
Dylan Thompson — MSc Computer Science, Trinity College Dublin, 2026

## Steps

**1. Install dependencies**
```
pip install -r requirements.txt
```

**2. Open the notebook**
```
jupyter notebook reproduce_dissertation.ipynb
```

**3. Run all cells top to bottom**

ACS datasets download automatically on first run — internet required.

The notebook is fully self-contained. Section 8 covers the three-attribute extension (sex x age x race, 8 groups).

## Reproducing dissertation results vs. retraining from scratch

At the top of the notebook, `RUN_ALL = False` (default). This loads pre-computed results from the `results/` directory and reproduces all tables and figures without retraining — takes ~2 minutes.

To retrain all models from scratch, set `RUN_ALL = True`. This runs the full pipeline (~3–4 hours on a modern laptop).

All experiments use `RANDOM_SEED = 42`, set in the setup cell, which ensures identical splits, training, and threshold selection across runs.
