# Template for Machine learning projects

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._

## Requirements

- [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html)
- [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html): This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
pip install cookiecutter
```

or

``` bash
conda install -c conda-forge cookiecutter
```

## Create a new project

In a folder where you want your project generated:

```bash
cookiecutter https://github.com/kesant/projects_template
```

## Resulting directory structure


    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── install.md         <- Detailed instructions to set up this project.
    ├── data
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries.
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, eg.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── environment.yml    <- The requirements file for reproducing the analysis environment.
    ├── requirements.txt   <- The pip requirements file for reproducing the environment.
    │
    ├── test               <- Unit and integration tests for the project.
    │   ├── __init__.py
    │   └── test_model.py  <- Example of a test script.
    │
    ├── .here              <- File that will stop the search if none of the other criteria
    │                         apply when searching head of project.
    │
    ├── setup.py           <- Makes project pip installable (pip install -e .)
    │                         so {{ cookiecutter.project_module_name }} can be imported.
    │
    └── {{ cookiecutter.project_module_name }}   <- Source code for use in this project.
        │
        ├── __init__.py             <- Makes {{ cookiecutter.project_module_name }} a Python module.
        │
        ├── config.py               <- Store useful variables and configuration.
        │
        ├── dataset.py              <- Scripts to download or generate data.
        │
        ├── features.py             <- Code to create features for modeling.
        │
        ├── modeling                
        │   ├── __init__.py 
        │   ├── predict.py          <- Code to run model inference with trained models.
        │   └── train.py            <- Code to train models.
        │
        ├── utils                   <- Scripts to help with common tasks.
        │   └── paths.py            <- Helper functions for relative file referencing across the project.        
        │
        └── plots.py                <- Code to create visualizations.

## Credits

This project is heavily influenced by [drivendata's Cookiecutter Data Science](https://github.com/drivendata/cookiecutter-data-science), [andfanilo's Cookiecutter for Kaggle Conda projects](https://github.com/andfanilo/cookiecutter-kaggle)

Other links that helped shape this cookiecutter :

- [Write less terrible code with Jupyter Notebook](https://blog.godatadriven.com/write-less-terrible-notebook-code)
- [Cookiecutter DataScience Opinions](http://drivendata.github.io/cookiecutter-data-science/#opinions)
