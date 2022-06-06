
<!-- README.md is generated from README.Rmd. Please edit that file -->

# strava

<!-- badges: start -->

[![R-CMD-check](https://github.com/tyluRp/strava/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/tyluRp/strava/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->

The goal of strava is to access the strava API from R.

## Authenticate

First, create an API application from your personal strava account, read
more here: <https://developers.strava.com/docs/getting-started/>

Then store the following credentials in your `.Renviron` file that you
can find with `usethis::edit_r_environ`:

-   `STRAVA_ID`
-   `STRAVA_SECRET`

Refresh your R session and make a request:

``` r
library(strava)

if (interactive()) get_athlete_activities()
```

The first time you make a request, you will be asked to authorize. After
authorization, the token will be cached in memory for future requests in
the current session.