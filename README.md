# RoomSense 🧠

**Room occupancy prediction with a small neural network built from scratch.**

RoomSense investigates whether temperature, humidity, light and CO₂ readings can help identify whether an office room is occupied. The motivation is energy efficiency: predictions might help facilities staff identify rooms worth checking, but this project **does not** control appliances or measure electricity savings.

## Current status

FIT1061 H2 project — **in development**. Predictions, scores and results have not been obtained yet.

## Planned approach

- Python and NumPy, with a feedforward neural network and one hidden layer.
- A P8-inspired weighted-sum classifier for comparison.
- Learning-rate and unreliable-sensor experiments.
- Accuracy, precision, recall, macro-F1 and confusion-matrix evaluation.

## Dataset

UCI [Occupancy Detection](https://archive.ics.uci.edu/dataset/357/occupancy-detection), Luis Candanedo (2016), CC BY 4.0. Download and extract `datatraining.txt`, `datatest.txt` and `datatest2.txt` into `data/raw/`.

The `data/raw/` files are intentionally not committed. To reproduce this project, download them from the credited source.

## Getting started

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m notebook
```

Open `RoomSense_H2.ipynb` from Jupyter, or open it in VS Code with the Python/Jupyter extensions and select the `.venv` Python kernel.

## Project layout

- `RoomSense_H2.ipynb` — H2 project notebook, experiments, figures, and report
- `data/` — local dataset location (`data/raw/` excluded from Git)
- `figures/` — exported plots, when completed
- `requirements.txt` — initial Python dependencies
- `SETUP.md` — GitHub and development instructions

## Academic integrity and attribution

This repository is intended to stay private during the assessment. The original H2 notebook template is from FIT1061. AI assistance used in planning and learning should be declared accurately in the H2 notebook. All implementation and experimental claims must be checked by the student.
