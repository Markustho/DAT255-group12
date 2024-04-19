Deep learning for tabular data
==============================

A practical application of machine learning and deep learning on tabular dataset from EDP. Wind turbine
data by was retrieved from their webpage https://www.edp.com/en/innovation/open-data/data. In this project the prediction models had a goal to guess on the bearing temperature of the generator. Different approaches are explored in the repositiory with variations of models, validation sets, training, and feature engineering. The project uses reseach paper by Bindingsbø, Singh, Kaprate, Øvsthus [1]


The slides accompanying the project can be found [here](https://docs.google.com/presentation/d/e/2PACX-1vSFtTsAzrGwXETVMaQlbelOe8VNptf3GTVGABAKh6koSu2Wcu74QdYOkh7-W6blsB5xUwNljDwA4I0C/pub?start=false&loop=false&delayms=3000).


## Report

See [./reports/report.md](./reports/report.md)

## Jupyter Notebooks

See [./notebooks/](./notebooks/)

## Oppgave:
![image](https://github.com/Markustho/DAT255-group12/assets/122047522/b8ac9188-b223-4fb7-99d0-ac0d4a1cddcd)

## Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

# Key files
src/models/Kaggle_notebook.ipynb - File to get a feel for the machine learning methods and data handling. Make this the first file you read

src/models/random forest/  - random forest tester with splitter

src/models/Neural network/  - neural network with splitter

# How to run
Use poetry to install the neccesary components https://python-poetry.org/docs/basic-usage/

Bash:

> cd repository folder

> poetry init

> poetry install

> poetry python run "filename.type"


Bibliography:
[1] O. T. Bindingsbø, M. Singh, K. Øvsthus, og A. Keprate, «Fault detection of a wind turbine generator bearing using interpretable machine learning», Front. Energy Res., bd. 11, s. 1284676, des. 2023, doi: 10.3389/fenrg.2023.1284676.
