Deep learning for tabular data
==============================

A practical application of machine learning and deep learning on tabular dataset from EDP. Wind turbine
data by was retrieved from their webpage https://www.edp.com/en/innovation/open-data/data. In this project the prediction models had a goal to guess on the bearing temperature of the generator. Different approaches are explored in the repositiory with variations of models, validation sets, training, and feature engineering. The project builds upon the work done by Bindingsbø, Singh, Kaprate, Øvsthus [1]

## Jupyter Notebooks

See [./notebooks/](./notebooks/)

## Project:
![image](https://github.com/Markustho/DAT255-group12/assets/122047522/b8ac9188-b223-4fb7-99d0-ac0d4a1cddcd)

## Project Organization
------------

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── Kaggle_notebook    <- Initial file exploring the machine learning models with different methods
    ├── data
    │   ├── processed      <- # The final, canonical data sets for modeling.
    │   └── raw            <- # Raw datasets from EDP
    │
    ├── docs               <- Not in use
    │
    ├── models             <- Contains .pkl files from the deep and tree model
    │                                 
    ├── references         <- Article references 
    │
    ├── reports            <- Report template
    │
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── models         <- folder for models that have splitters
    │   │   │                 
    │   │   ├── Notebook_blogpost_tabular_data.ipynb 
    │   │   └── Neural Network
    │   │   │                └── 4_neural_network.ipynb
    │   │   └── Random Forest
    │   │                    └── 1_split_datasets.ipynb
    │   │                    └── 2_clean_data_train_model.ipynb
    │   │                    └── 3_use_RF_model.ipynb
    │   │                    └── 4_interpreting_results.ipynb
                   
Notebook_blogpost_tabular_data.ipynb include the linear regression and XGBoost models. It also includes a short blogpost. 

Random forest and neural network implementations go hand in hand. We suggest to open the files in order, 1->2->3->4

--------

<p><small>Project template based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

# Key files
src/models/Notebook_blogpost_tabular_data.ipynb - File to get a feel for the machine learning methods and data handling. Make this the first file you read

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
 poetry run python3 "filename.type"
 ```

# Report
[Click here to find report](reports/report.md)



