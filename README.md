Deep learning for tabular data
==============================

A practical application of machine learning and deep learning on tabular dataset from EDP. Wind turbine
data by was retrieved from their webpage https://www.edp.com/en/innovation/open-data/data. In this project the prediction models had a goal to guess on the bearing temperature of the generator. Different approaches are explored in the repositiory with variations of models, validation sets, training, and feature engineering. The project uses reseach paper by Bindingsbø, Singh, Kaprate, Øvsthus [1]

## Jupyter Notebooks

See [./notebooks/](./notebooks/)

## Project:
![image](https://github.com/Markustho/DAT255-group12/assets/122047522/b8ac9188-b223-4fb7-99d0-ac0d4a1cddcd)

## Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Not in use
    ├── README.md          <- The top-level README for developers using this project.
    ├── Kaggle_notebook    <- Initial file exploring the machine learning models with different methods
    ├── data
    │   ├── external       <- Not in use
    │   ├── interim        <- Not in use
    │   ├── processed      <- # The final, canonical data sets for modeling.
    │   └── raw            <- Not in use
    │
    ├── docs               <- Not in use
    │
    ├── models             <- Contains .pkl files from the deep and tree model
    │
    ├── notebooks          <- Not in use                                     
    │
    ├── references         <- Not in use
    │
    ├── reports            <- Not in use
    │   └── figures        <- Not in use
    │
    ├── requirements.txt   <- Not in use
    │
    ├── setup.py           <- Not in use
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Not in use
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Not in use
    │   │   └── build_features.py
    │   │
    │   ├── models         <- folder for models that have splitters
    │   │   │                 
    │   │   ├── Kaggle_notebook.ipynb 
    │   │   └── Neural Network
    │   │   │                └── 4_neural_network.ipynb
    │   │   └── Random Forest
    │   │                    └── 1_split_datasets.ipynb
    │   │                    └── 2_clean_data_train_model.ipynb
    │   │                    └── 3_use_RF_model.ipynb
    │   │                    └── 5_interpreting_results.ipynb
    │   │                    
    │   │                    
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

# Key files
src/models/Kaggle_notebook.ipynb - File to get a feel for the machine learning methods and data handling. Make this the first file you read

src/models/random forest/  - random forest tester with splitter (this folder has multiple files)

src/models/Neural network/  - neural network with splitter (this folder has multiple files)

# How to run
Use poetry to install the necessary project dependencies https://python-poetry.org/docs/basic-usage/

1. Clone the github repository

2. Open powershell

## Bash:
Locate repository folder
> cd into repository

Use poetry to install the dependencies for the project
```shell
 poetry install
```

Run whatever file you want to view from key files from above section
```shell
> poetry python run "filename.type"
 ```

# An exploration of the world of AgTech

By ASL, 11.02.2024

> This is a template for a report on the world of AgTech used as a demonstration of DAT255 Course Projects. It's meant to help students get started with their own projects. It is not necessary to follow this structure.

# Introduction
 * Set the stage for the report by highlighting the importance of AgTech in addressing global food security, sustainability challenges, and how this report aims to contribute to understanding and advancing AgTech solutions.

# Part 1: Understanding Maintenance

## What is maintenance? 
* Overview of agriculture: scope and significance. (preventative, reactive and predictive maintenance ?)
* Key challenges in contemporary agriculture. (key challenges of maintenance programs of today)

## What is predictive maintenance?

* Definition and scope of AgTech. (predictive maintenance)
* Current state of AgTech: innovations and applications. 
* The future of AgTech: emerging technologies and trends.

# Part 2: Predictive maintenance in action: Case studies and experiments

## Methodology
* Description of the experimental design and methodology. 
* Specify the criteria for selecting case studies and experiments.
* Data collection and analysis techniques.

## Case studies (wind turbine)
* Detailed presentation of selected AgTech projects or experiments. (spanish windturbine farm off the coast of africa, turbine 07, etc... )
* Analysis of the data collected.
* Results and findings.

# Part 3: Implications and future directions

## Discussion
* Interpretation of results. (RMSE differences and which model performed best)
* Implications for the future of agriculture and AgTech. (machine learning for maintenance programs)
* Challenges and opportunities. (accuracy challenges, cost reduction opportunities)

## Conclusion
* Summary of key findings and their significance.
* Recommendations for future research and applications in AgTech

# References
* Citing all sources of information, data, and literature reviewed.

# Appendices (if applicable)
* Additional data, charts, or information that support the report but are too detailed for the main text.


# Bibliography:

[1] O. T. Bindingsbø, M. Singh, K. Øvsthus, og A. Keprate, «Fault detection of a wind turbine generator bearing using interpretable machine learning», Front. Energy Res., bd. 11, s. 1284676, des. 2023, doi: 10.3389/fenrg.2023.1284676.
