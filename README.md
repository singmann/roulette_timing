
# Data and Code: A speed-of-play limit reduces gambling expenditure in an online roulette game

<!-- badges: start -->
<!-- badges: end -->

This repository consists of data and code for the manuscript "A speed-of-play limit reduces gambling expenditure in an online roulette game" by Newall, Weiss-Cohen, Singmann, Boyce, Walasek, and Rockloff.

The code to reproduce the analysis is contained in the [RMarkdown file](https://rmarkdown.rstudio.com/) `bayesian_analysis.Rmd`. Running the code requires that the `data` folder containing the data is in the same folder as `bayesian_analysis.Rmd`.

Compiling (or "knitting") this RMarkdown document produces the output file `bayesian_analysis.html` which contains numerical results and figures. Compiling also creates the results figures as files in folder `figures` as well as saves the Bayesian MCMC chains as a binary `R` file in folder `model_fits`. Both of these folders are created during compilation in case they do not yet exist.

To ensure computational reproducibility, the code uses the [`checkpoint`](https://cran.r-project.org/package=checkpoint) package. This makes sure that `R` package versions from a specific checkpoint date (2021-10-20) are used. Sometimes running checkpoint from within `RMarkdown` can fail. In this case, running the following `R` code once **before** compiling the RMarkdown document will install the required packages. Please note that the working directory of the `R` session needs to be set to the directory (see `getwd()` and `setwd()`) in which the `bayesian_analysis.Rmd` file is (and in which ideally no further `R` files should be as `checkpoint` will install all packages found in the folder in which it is run.)



```r
install.packages("checkpoint")
library("checkpoint")
create_checkpoint("2021-10-20")
```


