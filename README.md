[![pages-build-deployment](https://github.com/WarwickCIM/IM939_handbook_quarto/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/WarwickCIM/IM939_handbook/actions/workflows/pages/pages-build-deployment) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/WarwickCIM/IM939_handbook_quarto/main)

# Data Science Across Disciplines' handbook

This repository contains the labs' handbook for [IM939: Data Science Across Disciplines](https://cagatayturkay.github.io/data-science-across-disciplines), created by Carlos Cámara-Menoyo, Cagatay Turkay and James Tripp.

![IM939 Logo](media/IM939_logo.png)

## Handbook

The handbook uses [quarto](https://quarto.org).

Render book locally:

From the book's root:

```bash
quarto render
```

If you want the cache to be regenerated:

```bash
quarto render --cache-refresh
```

Publishing book to github pages:

```bash
quarto publish gh-pages   
```
### Other resources that can be useful:

- Notebook embedding: https://quarto.org/docs/authoring/notebook-embed.html

## Virtual environments

Virtual environments are a way to install all the dependencies (and their right version) required for a certain project by isolating python and libraries' specific versions. Every person who recreatesthe virtual environment will be using the same packages and versions, reducing errors and increasing reproducibility.

In this project, virtual environments are managed by `conda`, which means that you should have [Anaconda distribution](https://www.anaconda.com) installed (Read [installing instructions on their website](https://www.anaconda.com/distribution/))

**Activate virtual environment**

```bash
conda activate env/
```

or, if  it is stored in `env/` folder:

```bash
conda activate env/
```

**Deactivate virtual environment:**

```bash
conda deactivate
```

**Update virtual environment from  `environment.yml`:**

```bash
conda env update -f environment.yml
```

**Recreate virtual environment from `environment.yml`:**

```bash
conda env create -f environment.yml
```

or, if we want to install the environment within the project:

```bash
conda env create --prefix env -f environment.yml
```

**Freeze used dependencies into a file**

We can create a file (in this case `environment.yml`) containing the exact libraries and versions used in the current environment. This can be useful to update the versions used in the environment in the future.

```bash
conda env export > environment.yml
```