Cookiecutter-DVC
==============================

An example of the Cookiecutter DVC project template.

Instructions
------------
1. Clone the repo.
1. Run `make dirs` to create the missing parts of the directory structure described below. 
1. *Optional:* Run `make virtualenv` to create a python virtual environment. Skip if using conda or some other env manager.
    1. Run `source env/bin/activate` to activate the virtualenv. 
1. Run `make requirements` to install required python packages.
1. Put the raw data in `data/raw`.
1. To save the raw data to the DVC cache, run `dvc commit raw_data.dvc`
1. Edit the code files to your heart's desire.
1. Process your data, train and evaluate your model using `dvc repro eval.dvc` or `make reproduce`
1. When you're happy with the result, commit files (including .dvc files) to git.
 
Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make dirs` or `make clean`
    ├── README.md          <- The top-level README for developers using this project.
    ├── raw_data.dvc       <- Keeps the raw data versioned.
    ├── data
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── dvc.lock
    ├── dvc.yaml
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures                 <- Generated graphics and figures to be used in reporting
    │   └── metrics.txt             <- Relevant metrics after evaluating the model.
    │   └── training_metrics.txt    <- Relevant metrics from training the model.
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   ├── __init__.py
    │   │   └── make_dataset.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── __init__.py
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       ├── __init__.py
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.testrun.org

--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>


---

To create a project like this, just go to https://dagshub.com/repo/create and select the **Cookiecutter DVC** project template.

Made with 🐶 by [DAGsHub](https://dagshub.com/).