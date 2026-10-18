# Run the Shiny Application

Runs a Shiny application. This function normally does not return;
interrupt R to stop the application (usually by pressing Ctrl+C or Esc).

## Usage

``` r
go_insane(
  demo = FALSE,
  port = getOption("shiny.port"),
  launch.browser = getOption("shiny.launch.browser", interactive()),
  host = getOption("shiny.host", "127.0.0.1"),
  workerId = "",
  quiet = FALSE,
  display.mode = c("auto", "normal", "showcase"),
  test.mode = getOption("shiny.testmode", FALSE)
)
```

## Arguments

- demo:

  \[[logical](https://rdrr.io/r/base/logical.html)\] A logical
  indicating if examples spreadsheets should be copied in the app.

- port:

  The TCP port that the application should listen on. If the `port` is
  not specified, and the `shiny.port` option is set (with
  `options(shiny.port = XX)`), then that port will be used. Otherwise,
  use a random port between 3000:8000, excluding ports that are blocked
  by Google Chrome for being considered unsafe: 3659, 4045, 5060, 5061,
  6000, 6566, 6665:6669 and 6697. Up to twenty random ports will be
  tried.

- launch.browser:

  If true, the system's default web browser will be launched
  automatically after the app is started. Defaults to true in
  interactive sessions only. The value of this parameter can also be a
  function to call with the application's URL.

- host:

  The IPv4 address that the application should listen on. Defaults to
  the `shiny.host` option, if set, or `"127.0.0.1"` if not. See Details.

- workerId:

  Can generally be ignored. Exists to help some editions of Shiny Server
  Pro route requests to the correct process.

- quiet:

  Should Shiny status messages be shown? Defaults to FALSE.

- display.mode:

  The mode in which to display the application. If set to the value
  `"showcase"`, shows application code and metadata from a `DESCRIPTION`
  file in the application directory alongside the application. If set to
  `"normal"`, displays the application normally. Defaults to `"auto"`,
  which displays the application in the mode given in its `DESCRIPTION`
  file, if any.

- test.mode:

  Should the application be launched in test mode? This is only used for
  recording or running automated tests. Defaults to the `shiny.testmode`
  option, or FALSE if the option is not set.

## Examples

``` r

if (interactive()) {
  library(insane)
  # Must be run in an interactive R session!
  go_insane()
}
```
