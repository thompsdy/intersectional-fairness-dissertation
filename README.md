# Intersectional Fairness in Machine Learning: An Analysis Using Oxonfair.
Dylan Thompson — MSc Computer Science, Trinity College Dublin, 2026

## Requirements

Python 3.13.5 was used for development. Run `python3 --version` to check yours.

## Steps

**1. Install dependencies**
```bash
pip3 install -r requirements.txt
```

If pip3 installs to a different Python, use the full path:
```bash
/Library/Frameworks/Python.framework/Versions/3.13/bin/pip3 install -r requirements.txt
```

**2. Open the notebook**
```bash
jupyter notebook reproduce_dissertation.ipynb
```

In VS Code: open `reproduce_dissertation.ipynb`, click the kernel selector (top right), and select the Python 3.13 interpreter where you ran pip3.

**3. Run all cells top to bottom**

ACS datasets download automatically on first run — internet required.

The notebook is fully self-contained. Section 8 covers the three-attribute extension (sex x age x race, 8 groups).

## Reproducing dissertation results vs. retraining from scratch

At the top of the notebook, `RUN_ALL = False` (default). This loads pre-computed results from the `results/` directory and reproduces all tables and figures without retraining — takes ~2 minutes.

To retrain all models from scratch, set `RUN_ALL = True`. This runs the full pipeline (~3–4 hours on a modern laptop).

All experiments use `RANDOM_SEED = 42`, set in the setup cell, which ensures identical splits, training, and threshold selection across runs.
