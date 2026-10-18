# Deploy the Shiny App

Deploy (copy) the shiny application to the specified directory

## Usage

``` r
deploy(
  directory = "/srv/shiny-server",
  app_name = "insane",
  demo = FALSE,
  overwrite = FALSE
)
```

## Arguments

- directory:

  \[[character](https://rdrr.io/r/base/character.html)\] A character
  vector of one path to the new location.

- app_name:

  \[[character](https://rdrr.io/r/base/character.html)\] A character
  vector defining the shiny application name in the new location.

- demo:

  \[[logical](https://rdrr.io/r/base/logical.html)\] A logical
  indicating if examples spreadsheets should be copied in the app.

- overwrite:

  \[[logical](https://rdrr.io/r/base/logical.html)\] A logical
  indicating if existing destination files should be overwritten.

## Value

\[[logical](https://rdrr.io/r/base/logical.html)\] A logical indicating
whether the deployment is successfull (`TRUE`) or not (`FALSE`).

## Examples

``` r

deploy(directory = ".")
#> [1] TRUE

if (interactive()) {
  shiny::runApp("insane")
}
```
