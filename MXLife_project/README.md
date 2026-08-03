# MXLife

Literature-mined dataset + survival-analysis models for predicting Ti3C2Tx MXene oxidation shelf-life.

## What this is
MXene stability data is scattered across dozens of papers with no consistent format. This project pulls it into one structured, time-dependent dataset and uses survival analysis to predict shelf-life (probability of staying stable at 7/30/90/180 days) instead of treating stability as a single yes/no property. Full rules, ontology, and rationale are in the project handoff report (kept alongside this repo, not tracked here).

## Structure
- `data/raw/` - the working Excel file (`papers_screening` + `raw_extractions` sheets). Source of truth.
- `data/processed/` - cleaned/normalized CSVs. Starts ~week 9.
- `data_dictionary/` - column definitions and allowed values. Currently just the `Allowed_Values` sheet inside the raw workbook; gets exported standalone once frozen.
- `notebooks/` - cleaning, baseline models, survival models, figures.
- `scripts/` - `clean_data.py`, `make_labels.py`, `train_models.py`.
- `literature/` - paper-level notes that don't fit into a raw_extractions row.
- `extraction_notes/` - running list of confusing/ambiguous variables hit during extraction.
- `figures/` - manuscript figures.
- `validation_experiment/` - validation experiment data, photos, logs.
- `manuscript/` - drafts.

## Status
Screening: 47 papers reviewed, 39 include / 8 exclude. Extraction: just starting (0 rows in raw_extractions so far).

## Scope
Ti3C2Tx MXene only for the main dataset (other MXenes marked secondary if included). No active learning / RL claims - that's explicitly out of scope.
