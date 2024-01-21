# SOLES `learnr` R Markdown template

This is an R Markdown template for creating a `learnr` tutorial with minimal University of Sydney branding, with optional setup for hosting on [Binder](https://mybinder.org/) which allows users to run the tutorial in their browser without installing R or RStudio.

View the tutorial [here](https://mybinder.org/v2/gh/usyd-soles-edu/soles-learnr/main?urlpath=shiny/tutorial/learnr.Rmd).

Note that the tutorial might take a few minutes to load the first time you open it as Binder needs to create a virtual environment to run the tutorial in, which involves installing R and all the packages used in the tutorial.

## Installation

To use this template, you will need to install the `learnr` package:

```r
install.packages("learnr")
```

Either download the files in this repository, or clone/use this template repository, then open `learnr.Rmd` in RStudio.
RStudio might prompt you to install additional packages, which you should do. Then, click the "Run Document" button to preview the tutorial.

## Optional - Binder

To host the tutorial on Binder, the simplest way is to copy this repository as a template by clicking the green "Use this template" button above. This will create a new repository in your GitHub account with the same files as this one.

Then, rename the `learnr.Rmd` file, move it across folders, etc. Then, edit the README.md file (like this one) to update the link to the tutorial on Binder. The link should look like this:

```
https://mybinder.org/v2/gh/<your-github-username>/<your-repository-name>/main?urlpath=shiny/tutorial/<path-to-your-Rmd-filename>.Rmd
```

## Adding R packages

If you use any R packages in your tutorial, you will need to add them to the `environment.yml` file so that Binder knows to install them. To do this, add the package name to the `dependencies` section of the `environment.yml` file, like this:

```yml
channels:
  - conda-forge
dependencies:
  - r-base>4.3.0
  - r-learnr
  - r-ggplot2
```


## Multiple tutorials in one repository

**You can host multiple tutorials in the same repository**, just create a new folder for each tutorial and create a new link for each file accordingly.

## License and Attribution

This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).


