# Cookiecutter Bioinformatics

Fork of the [Max Planck Institute of Immunobiology and Epigenetics Bioinformatics Core Facility](https://www.ie-freiburg.mpg.de/bioinformatics) repo, with the idea of creating reproducible, FAIR bioinformatic workflows. See [Project homepage](https://github.com/dkoppstein/cookiecutter-bioinformatics-project). I tailored it to my personal preferences and usage. 

### Requirements:
-----------

 - Python 2.7 or 3.5+
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```

### Usage:
------------

    cookiecutter gh:saimanzano/cookiecutter-bioinformatics-project


### The resulting directory structure
------------

The directory structure of your new project looks like this: 

```

├── CITATION.cff       <- Contains metadata on how the project might eventually be published. 
├── LICENSE
├── Makefile           <- Makefile with commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── config             <- Configuration options for the analysis. 
|   ├── config.yaml    <- Snakemake config file. 
│
├── environment.yaml   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `conda env export > environment.yaml`
│
├── plots              <- A place to store images associated with the project/pipeline, e.g. a 
│                         a figure of the pipeline DAG. 
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── outputs            <- Generated outputs. By default excluded from the git repository.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── data               <- Place for data. By default excluded from the git repository. 
│   ├── external       <- Data from third party sources.
│   └── raw_data       <- The original, immutable data dump.
│
├── results            <- Final output of the data processing pipeline, incl. final figures.
│   └── final_figs     <- Generated graphics and figures to be used in the paper
│ 
├── tests              <- A place to test scripts and ideas. By default excluded from the git repository.
│ 
├── scripts            <- A place for short shell or python scripts.
│ 
├── setup.py           <- Makes project pip installable (pip install -e .) so src can be importe
│
├── src                <- Source code for use in this project. Naming convention is a number (for ordering), 
│                         and a short `-` delimited description, e.g. `1.0-jqp-initial-data-exploration`.
│   ├── __init__.py    <- Makes src a Python module
│ 
├── workflow           <- Place to store the main pipeline for rerunning all the analysis. 
│   ├── envs           <- Contains different conda environments in .yaml format for running the pipeline. 
│   ├── rules          <- Contains .smk files that are included by the main Snakefile, including common.smk for functions. 
│   ├── scripts        <- Contains different R or python scripts used by the script: directive in Snakemake.
│   ├── Snakefile      <- Contains the main entrypoint to the pipeline.
│ 
├── workspace          <- Space for intermediate results in the pipeline. By default excluded from the git repository.  
```


### Installing development requirements
------------

    pip install -r requirements.txt

### Running the tests
------------

    py.test tests
