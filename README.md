# Boilerplate Template

This repository contains a minimal, lightweight boilerplate template for data
science projects. The overall purpose is to have an organized and (mostly)
unified project structure so that each project is easily approachable to
different individuals who many need to review or refer to your project in the
future.

This is by no means meant to be prescriptive, but it should hopefully provide a
good starting point. As our team needs change and expand, the structure of this
template will likely change. Feel free to adjust and edit the template as
necessary for your projects.

## Project Structure

This template contains the following folder structure:

```
project-name
│   README.md
└───data/
│       └───raw/
│       └───processed/
└───documents/
└───notebooks/
└───results/
└───scripts/
│       └───python/
|       └───sql/     
```

### Data

Contains subfolders for both raw and processed data sets. Generally speaking,
we don't want to put super large datasets here (maybe max 10MB), so you can add
`*.csv` files to the `.gitignore` file.

The raw data itself should never be touched manually. Instead, you should have
scripts or notebooks that load the raw data into an R or Python environment
for in-environment data manipulation (this will not modify the raw data files
themselves).

Any data that is produced by code should be saved in the `data/processed_data/`
subdirectory.

### Documents

This is a good place to keep any meeting notes, data dictionaries, and
miscellaneous documents.

### Notebooks

This folder should contain Jupyter notebook files (`*.ipnyb`). These files are
typically used for *data analysis*.

### Results

Data or images that are produced from code can be stored here.

### Scripts

Production-ready code & scripts.

## Usage

To use this template, clone the repository to your local machine and rename it:

```
$ git clone https://github.com/phister/ds-boilerplate.git project-name
```

This has set up a new `git` project in the folder `project-name`. After changing
to that directory, we can see `git` has also set up a remote origin for us:

```
$ cd project-name
$ git remote -v
origin https://github.com/phister/ds-boilerplate.git (fetch)
origin https://github.com/phister/ds-boilerplate.git (push)
```

We want origin to be for our new project and not the boilerplate template. We
can do that by removing the original remote:

```
$ git remote remove origin
```

Now, log back into the Github and
[create a new repository](https://github.com/new) with the project
name specified above. Follow the instructions on the page to "push an existing
repository from the command line", or enter this (replace the "..."):

```
$ git remote add origin .../project-name.git
$ git push -u origin master
```

Now you have a copy of the boilerplate template under `project-name`!