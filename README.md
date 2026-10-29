# Intro_to_ML_26-27
Introduction to Machine Learning - Course for the Artificial Intelligence and Data Analytics Bachelor Degree - University of Trieste

 - Fabio Anselmi 

 - Alex Rodriguez 

 - Lorenzo Tonet (LORENZO.TONET@studenti.units.it)

 - ?

Notebooks: 

First semester (Mod. A):

* [Lab 0](Labs/Lab-0_IntroColab.ipynb): Introduction to Google Colab 

* [Lab 0.1](Labs/Lab0_Intro_to_pandas.ipynb): Introduction to Pandas

* [Lab 1](Labs/Lab-01_Data_generation.ipynb): Data generation

* [Lab 2](Labs/Lab-02_Linear_and_Logistic_Reg.ipynb): Linear and logistic reg. ([solved](Solutions/Lab-02_Linear_and_Logistic_Reg_Solved.ipynb))

## Local setup with uv

Install [uv](https://docs.astral.sh/uv/getting-started/installation/), then run from the repository root:

```bash
uv run jupyter lab
```

uv automatically downloads Python 3.13 if needed, creates `.venv`, and installs
the dependencies from `uv.lock`. No manual environment creation or activation
is needed. Open a notebook in `Labs/` and use the Python 3 kernel.

### VS Code

Run `uv sync` once, open a notebook with the Python and Jupyter extensions
installed, and select **Select Kernel → Python Environments → .venv**.

### Managing dependencies

```bash
uv add package-name   # Add a dependency and update uv.lock
uv sync              # Install the locked dependencies after pulling changes
uv run python        # Run Python in the project environment
```

Commit `pyproject.toml`, `.python-version`, and `uv.lock`; `.venv` is already
ignored. Restart the notebook kernel after adding dependencies.

The pandas and data-generation labs are supported locally, including the
interactive `drawdata` widget. Draw some points before running the cells that
read and plot the widget's data. The pandas lab downloads its CSV from GitHub
and needs internet access; a copy is also available at `data/ign.csv`.

`Lab-0_IntroColab.ipynb` is a Google Colab tutorial: run it on Colab. Its Drive
mount and example `pip install` cells (including the old NumPy version) are
specific to that tutorial and should not be run in the local uv environment.

See the [uv Jupyter guide](https://docs.astral.sh/uv/guides/integration/jupyter/)
for details about notebook integration.
