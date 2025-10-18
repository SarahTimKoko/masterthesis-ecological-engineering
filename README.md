# Masterthesis Ecological Engineering

## Description

The results of this project is automatically deployed to <https://sarahtimkoko.github.io/masterthesis-ecological-engineering>

## Project Structure

-   `R/` - R scripts
-   `data/raw` - raw data
-   `data/tidy` - clean data
-   `output/` - figures, tables, results
-   `\_site/` - generated html site
-   `\_site.yml` - R Markdown site configuration
-   `renv.lock` - environment lock file

## Set up

``` r
install.packages("renv")
```

## Usage

``` r
# Load environment
renv::restore()

# Run scripts

source("R/utils.R")

# Render page

Rscript -e 'rmarkdown::render\_site()'
```

## Install new package with renv

```r
renv::install("<package>")
```

After installing the package and checking that your code works, you should call 
```r
renv::snapshot()
``` 
to record the latest package versions in your lockfile. 

