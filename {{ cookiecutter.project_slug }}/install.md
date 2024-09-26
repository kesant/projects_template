# {{ cookiecutter.project_name }} guide installation

## Prerequisites

- [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html)
- Optional [Mamba](https://mamba.readthedocs.io/en/latest/)

## Create environment

```bash
conda env create -f environment.yml
conda activate {{ cookiecutter.project_slug }}
```

or 

```bash
mamba env create -f environment.yml
mamba activate {{ cookiecutter.project_slug }}
```
or 

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
pip install -r requirements.txt
```

The packages necessary to run the project are now installed inside the conda environment.

**Note: The following sections assume you are located in your environment.**

## Set up project's module

To move beyond notebook prototyping, all reusable code should go into the `{{ cookiecutter.project_module_name }}/` folder package. To use that package inside your project, install the project's module in editable mode, so you can edit files in the `{{ cookiecutter.project_module_name }}` folder and use the modules inside your notebooks :

```bash
pip install --editable .
```

To use the module inside your notebooks, add `%autoreload` at the top of your notebook :

```python
%load_ext autoreload
%autoreload 2
```

Example of module usage :

```python
from {{ cookiecutter.project_module_name }}.utils.paths import data_dir
data_dir()
```
## Update Environment Files After Installing New Dependencies

```bash
conda install <package_name>
conda env export --no-builds | grep -v "^prefix: " > environment.yml
```

or 

```bash
mamba install <package_name>
mamba env export --no-builds | grep -v "^prefix: " > environment.yml
```
or 

```bash
pip install <package_name>
pip freeze > requirements.txt
```

