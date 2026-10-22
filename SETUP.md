# RoomSense: first milestones

## 1. Create the personal GitHub repository

Visit https://github.com/new, select owner `mxhamedxx`, name `RoomSense`, make it **Private**, and leave README, .gitignore and license unchecked. If it already exists, do not create a second one.

## 2. Open the folder

Extract this starter project's `RoomSense/` folder into `D:\Projects\`, then open `D:\Projects\RoomSense` in VS Code.

## 3. Install Python dependencies (PowerShell in RoomSense folder)

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m notebook
```

## 4. Inspect the H2 notebook

Open `RoomSense_H2.ipynb`. The H1 recap is filled from your previously completed H1; review it. Run the SETUP cell and confirm `Setup OK.`. The `Data`, `Implementation`, `Experiment 1`, `Experiment 2`, `Visualisation 1`, `Visualisation 2`, and `H2.2 Report` sections remain for you to complete and explain.

## 5. Add the UCI data locally

From https://archive.ics.uci.edu/dataset/357/occupancy-detection download the dataset and put these files into `data/raw/`:
- datatraining.txt
- datatest.txt
- datatest2.txt

Do not train against either official test file. Split the training file into training and validation in time order; use training statistics for scaling.

## 6. First Git commit

```powershell
git init -b main
git config --local user.name "mxhamedxx"
git config --local user.email "YOUR-VERIFIED-GITHUB-EMAIL"
git add .
git commit -m "chore: set up RoomSense H2 project"
git remote add origin https://github.com/mxhamedxx/RoomSense.git
git push -u origin main
```

Your Git author name/email is separate from authentication. If you already configured Git or added an origin, inspect with `git status`, `git remote -v`, and `git log -1` before repeating these commands. Sign in to **mxhamedxx** when prompted.

## 7. Suggested milestones

1. `chore: set up RoomSense H2 project`
2. `feat: inspect occupancy dataset and class labels`
3. `feat: split and standardise sensor features`
4. `feat: implement and verify neural network forward pass`
5. `feat: implement and check backpropagation`
6. `feat: train model and evaluate baseline`
7. `test: compare learning rates and missing sensor readings`
8. `docs: analyse results and complete H2 report`

Only commit a milestone after that change exists and has been tested.

## H2 rubric reminders

- Two or more meaningful experiments, not just different random seeds.
- At least two visualisations **explained in the report**.
- A reproducible, understandable model and honest comparison with the baseline.
- At least four specific limitations and an ethical connection to C2 or C4.
- Around 1500 words covering all six report sections.
- Accurately declare AI assistance. The HD task discourages AI-generated core implementation and reflection; complete these yourself, using assistance for explanation and debugging.
