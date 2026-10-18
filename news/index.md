# Changelog

## insane 1.0.3

CRAN release: 2023-11-14

### Chores

- In `DESCRIPTION`, `inst/app/app.R`, and `R/go_insane.R`,
  - chore: remove `ggthemes` to avoid archiving.

## insane 1.0.2

CRAN release: 2023-04-01

### Chores

- In `DESCRIPTION`,
  - chore: update domain name.

**Full Changelog**:
<https://github.com/mcanouil/insane/compare/v1.0.1...v1.0.2>

## insane 1.0.1

CRAN release: 2022-12-05

### Chores

- In `DESCRIPTION`,
  - chore: update email address.
- chore: remove `ggbeeswarm`.

**Full Changelog**:
<https://github.com/mcanouil/insane/compare/v1.0.0...v1.0.1>

## insane 1.0.0

CRAN release: 2022-11-24

### Chores

- In `DESCRIPTION`,
  - chore: update email address.
- In `README.md`,
  - chore: update URLs with issues.

**Full Changelog**:
<https://github.com/mcanouil/insane/compare/v0.1.0...v1.0.0>

## insane 0.1.0

CRAN release: 2020-11-04

### New features

- New Shiny app in `inst/app/`.
- New [`deploy()`](../reference/deploy.md) (`R/deploy.R`) function to
  easily deploy (copy) the shiny app to a specified directory.
- New [`go_insane()`](../reference/go_insane.md) (`R/go_insane.R`)
  function to easily run
  ([`shiny::runApp()`](https://rdrr.io/pkg/shiny/man/runApp.html)) the
  shiny app.
- New vignette `insane` describing the Shiny app.
- New vignette `protocol`, describing the experimental protocol on which
  the Shiny app is built on.
