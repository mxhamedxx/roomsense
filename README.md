# RoomSense

RoomSense is a small neural network that predicts office-room occupancy using temperature, humidity, light and CO2 readings.

This project was developed for FIT1061 Introduction to Artificial Intelligence at Monash University.

Author: Mohamed Elsayed Ahmed
Version: v1.0

## Project Features

- Neural network implemented from scratch using Python and NumPy
- Four sensor inputs, six hidden neurons and one output
- Weighted-sum baseline for comparison
- Learning-rate experiment
- Light sensor reliability experiment
- Evaluation using accuracy, precision, occupied recall, macro-F1 and false negatives

## Dataset

RoomSense uses the [UCI Occupancy Detection dataset](https://archive.ics.uci.edu/dataset/357/occupancy-detection).

Download the dataset and place these files inside `data/raw/`:

- `datatraining.txt`
- `datatest.txt`
- `datatest2.txt`

The dataset is not included in the GitHub repository.

## How to Run

Open Anaconda Prompt and navigate to the RoomSense project folder.

Activate the Python environment:

```bash
conda activate roomsense
```

Install the project dependencies if needed:

```bash
python -m pip install -r requirements.txt
```

Open the Jupyter Notebook:

```bash
python -m notebook RoomSense_H2.ipynb
```

Run the notebook cells from top to bottom.

## Results

The selected neural network used a learning rate of 0.5 and was trained for 300 epochs.

On the official test datasets, the neural network achieved:

| Metric | Test Set 1 | Test Set 2 |
|---|---|---|
| Accuracy | 0.9568 | 0.8799 |
| Macro-F1 | 0.9544 | 0.8475 |
| Occupied Recall | 0.9949 | 0.9971 |

The neural network met the macro-F1 and occupied recall targets, but did not achieve the planned improvement over the weighted-sum baseline.

## Limitations

Performance decreases when light sensor readings become unreliable. The project was also evaluated using a limited dataset and does not include real-world building deployment or automatic energy control.

## Project Files

- `RoomSense_H2.ipynb` — Implementation, experiments, graphs and report
- `figures/` — Generated visualisations
- `requirements.txt` — Python dependencies
- `SETUP.md` — Additional setup instructions

## Dataset Reference

Candanedo, L. M. (2016). *Occupancy Detection*. UCI Machine Learning Repository. https://doi.org/10.24432/C5X01N