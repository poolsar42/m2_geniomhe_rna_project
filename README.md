# RNA bioinformatics - M2-GENIOMHE project

This repo is a wrapper around skeleton that was provided to us to start.

## Repository

- `data`: a folder with the training (`data/TrainingSet`), testing (`data/TestSet`), sample (`data/sample`) folders and `SPOT-RNA-1D` folder.
  The `sample` folder contains a `.fasta` file that should be used to do inference for the delivery.
  The `SPOT-RNA-1D` folder contains the predictions from `SPOT-RNA-1D` for the Training set (`data/SPOT-RNA-1D/training.json`) and Test set (`data/SPOT-RNA-1D/test.json`). `angles` folder in `data` contains `.csv` files for each sequence with all angles for it's nucleotides.
- `rna_angles_prediction_dssr`: is a folder where a cloned code from this [repository](https://github.com/EvryRNA/rna_angles_prediction_dssr/tree/main). It computes angles for provided `TestSet` and `TrainingSet` in the data.
- `src`: a folder where we implement our solution. Lets take a closer look at its components.
- `models`: folder where we store our pre-trained models
- `results`: folder where we store comparisons (MAE) of our model with prediction of SPOT-RNA-1D

## src

- `__init__.py`: initialization of a package
- `main.py`: modify and run this code to check functionality of all modules within the package
- `data_extraction.py`: extract the needed angles provided by dssr
- `utils.py`: modify the data so that it become feedable to a model
- `visualisation.py`: functionality to view distribution of angles in provided datasets
- `models.py`: implementation of LSTM regressor and classifier for angle predictions
- `train.py`: functions which train the models
- `evaluate.py`: functions to test the accuracy of trained models

## How to get started

1. Navigate to `rna_angles_prediction_dssr` folder and run `python dssr_wrapper.py`

2. Navigate to the `root/src` folder and run `main.py`

3. Add modifications to main to test desirable functionality

## TO-DO

- Include python requirements to run your code with good library versions.
- Compare our results with results from SPOT-RNA-1D
