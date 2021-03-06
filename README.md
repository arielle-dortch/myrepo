readme
================

<!-- README.md is generated from README.Rmd. Please edit that file -->

# packages-report

## Bonus activity prompt

  - Combine your work analyzing your R packages and what we’ve learned
    re: GitHub and R Markdown
  - This `README.Rmd` gives a scaffold for using the work you did
    earlier to make a little report.
  - Given our previous work, I’m using pre-computed results and
    including a pre-made figure, leaving the R code down in scripts
    below `R/`. But know that, in other contexts, you could inline all
    that code in chunks here. Depends on downstream usage and the
    project context.
  - Locally, do `README.Rmd` –\> `README.md` with the “Knit” button or
    via `rmarkdown::render("README.Rmd")`. Commit both.
  - I presume you are hooked up to GitHub remote repo, covered in
    [Existing project, GitHub
    last](https://happygitwithr.com/existing-github-last.html). Summary:
      - Consider the convenience function `usethis::use_github()`. Or to
        do by hand:
      - Create a similarly-named repo on GitHub.
      - Add it to the local repo as the `origin` remote: `git remote add
        origin https://github.com/YOU/REPO.git`.
      - Push and cement the branch tracking relationship: `git push
        --set-upstream origin master`.
  - Push\! Now your README is an excellent welcome mat and summary of
    your project.
  - On GitHub, in *Settings*, turn on GitHub Pages. Visit the given URL
    for an even more polished report of your project. It may take a few
    minutes to show up / update. Record that as the URL for your repo.

## Overview

The goal of packages-report is to FINISH THIS SENTENCE.

I have `FILL THIS IN!!!` add-on packages installed.

Here’s how they break down in terms of which version of R they were
built under, which is related to how recently they were updated on CRAN.

### Flow of the analysis

*If you have time, document the analysis works, using internal links.*

*If you created some sort of controller script, describe that here.*

<details>

<summary>Session info</summary>

``` r
devtools::session_info()
#> ─ Session info ───────────────────────────────────────────────────────────────
#>  setting  value                       
#>  version  R version 3.6.1 (2019-07-05)
#>  os       macOS Catalina 10.15.1      
#>  system   x86_64, darwin15.6.0        
#>  ui       X11                         
#>  language (EN)                        
#>  collate  en_US.UTF-8                 
#>  ctype    en_US.UTF-8                 
#>  tz       America/Los_Angeles         
#>  date     2020-01-27                  
#> 
#> ─ Packages ───────────────────────────────────────────────────────────────────
#>  package     * version date       lib source        
#>  assertthat    0.2.1   2019-03-21 [1] CRAN (R 3.6.0)
#>  backports     1.1.5   2019-10-02 [1] CRAN (R 3.6.0)
#>  broom         0.5.2   2019-04-07 [1] CRAN (R 3.6.0)
#>  callr         3.4.0   2019-12-09 [1] CRAN (R 3.6.1)
#>  cellranger    1.1.0   2016-07-27 [1] CRAN (R 3.6.0)
#>  cli           2.0.0   2019-12-09 [1] CRAN (R 3.6.1)
#>  colorspace    1.4-1   2019-03-18 [1] CRAN (R 3.6.0)
#>  crayon        1.3.4   2017-09-16 [1] CRAN (R 3.6.0)
#>  DBI           1.0.0   2018-05-02 [1] CRAN (R 3.6.0)
#>  dbplyr        1.4.2   2019-06-17 [1] CRAN (R 3.6.0)
#>  desc          1.2.0   2018-05-01 [1] CRAN (R 3.6.0)
#>  devtools      2.2.1   2019-09-24 [1] CRAN (R 3.6.0)
#>  digest        0.6.23  2019-11-23 [1] CRAN (R 3.6.0)
#>  dplyr       * 0.8.3   2019-07-04 [1] CRAN (R 3.6.0)
#>  ellipsis      0.3.0   2019-09-20 [1] CRAN (R 3.6.0)
#>  evaluate      0.14    2019-05-28 [1] CRAN (R 3.6.0)
#>  fansi         0.4.0   2018-10-05 [1] CRAN (R 3.6.0)
#>  forcats     * 0.4.0   2019-02-17 [1] CRAN (R 3.6.0)
#>  fs            1.3.1   2019-05-06 [1] CRAN (R 3.6.0)
#>  generics      0.0.2   2018-11-29 [1] CRAN (R 3.6.0)
#>  ggplot2     * 3.2.1   2019-08-10 [1] CRAN (R 3.6.0)
#>  glue          1.3.1   2019-03-12 [1] CRAN (R 3.6.0)
#>  gtable        0.3.0   2019-03-25 [1] CRAN (R 3.6.0)
#>  haven         2.2.0   2019-11-08 [1] CRAN (R 3.6.0)
#>  hms           0.5.2   2019-10-30 [1] CRAN (R 3.6.0)
#>  htmltools     0.4.0   2019-10-04 [1] CRAN (R 3.6.0)
#>  httr          1.4.1   2019-08-05 [1] CRAN (R 3.6.0)
#>  jsonlite      1.6     2018-12-07 [1] CRAN (R 3.6.0)
#>  knitr         1.26    2019-11-12 [1] CRAN (R 3.6.0)
#>  lattice       0.20-38 2018-11-04 [1] CRAN (R 3.6.1)
#>  lazyeval      0.2.2   2019-03-15 [1] CRAN (R 3.6.0)
#>  lifecycle     0.1.0   2019-08-01 [1] CRAN (R 3.6.0)
#>  lubridate     1.7.4   2018-04-11 [1] CRAN (R 3.6.0)
#>  magrittr      1.5     2014-11-22 [1] CRAN (R 3.6.0)
#>  memoise       1.1.0   2017-04-21 [1] CRAN (R 3.6.0)
#>  modelr        0.1.5   2019-08-08 [1] CRAN (R 3.6.0)
#>  munsell       0.5.0   2018-06-12 [1] CRAN (R 3.6.0)
#>  nlme          3.1-140 2019-05-12 [1] CRAN (R 3.6.1)
#>  pillar        1.4.2   2019-06-29 [1] CRAN (R 3.6.0)
#>  pkgbuild      1.0.6   2019-10-09 [1] CRAN (R 3.6.0)
#>  pkgconfig     2.0.3   2019-09-22 [1] CRAN (R 3.6.0)
#>  pkgload       1.0.2   2018-10-29 [1] CRAN (R 3.6.0)
#>  prettyunits   1.0.2   2015-07-13 [1] CRAN (R 3.6.0)
#>  processx      3.4.1   2019-07-18 [1] CRAN (R 3.6.0)
#>  ps            1.3.0   2018-12-21 [1] CRAN (R 3.6.0)
#>  purrr       * 0.3.3   2019-10-18 [1] CRAN (R 3.6.0)
#>  R6            2.4.1   2019-11-12 [1] CRAN (R 3.6.0)
#>  Rcpp          1.0.3   2019-11-08 [1] CRAN (R 3.6.0)
#>  readr       * 1.3.1   2018-12-21 [1] CRAN (R 3.6.0)
#>  readxl        1.3.1   2019-03-13 [1] CRAN (R 3.6.0)
#>  remotes       2.1.0   2019-06-24 [1] CRAN (R 3.6.0)
#>  reprex        0.3.0   2019-05-16 [1] CRAN (R 3.6.0)
#>  rlang         0.4.2   2019-11-23 [1] CRAN (R 3.6.0)
#>  rmarkdown     1.18    2019-11-27 [1] CRAN (R 3.6.0)
#>  rprojroot     1.3-2   2018-01-03 [1] CRAN (R 3.6.0)
#>  rstudioapi    0.10    2019-03-19 [1] CRAN (R 3.6.0)
#>  rvest         0.3.5   2019-11-08 [1] CRAN (R 3.6.0)
#>  scales        1.1.0   2019-11-18 [1] CRAN (R 3.6.0)
#>  sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 3.6.0)
#>  stringi       1.4.3   2019-03-12 [1] CRAN (R 3.6.0)
#>  stringr     * 1.4.0   2019-02-10 [1] CRAN (R 3.6.0)
#>  testthat      2.3.1   2019-12-01 [1] CRAN (R 3.6.0)
#>  tibble      * 2.1.3   2019-06-06 [1] CRAN (R 3.6.0)
#>  tidyr       * 1.0.0   2019-09-11 [1] CRAN (R 3.6.0)
#>  tidyselect    0.2.5   2018-10-11 [1] CRAN (R 3.6.0)
#>  tidyverse   * 1.3.0   2019-11-21 [1] CRAN (R 3.6.0)
#>  usethis       1.5.1   2019-07-04 [1] CRAN (R 3.6.0)
#>  vctrs         0.2.0   2019-07-05 [1] CRAN (R 3.6.0)
#>  withr         2.1.2   2018-03-15 [1] CRAN (R 3.6.0)
#>  xfun          0.11    2019-11-12 [1] CRAN (R 3.6.0)
#>  xml2          1.2.2   2019-08-09 [1] CRAN (R 3.6.0)
#>  yaml          2.2.0   2018-07-25 [1] CRAN (R 3.6.0)
#>  zeallot       0.1.0   2018-01-28 [1] CRAN (R 3.6.0)
#> 
#> [1] /Library/Frameworks/R.framework/Versions/3.6/Resources/library
```

</details>

*See <https://github.com/jennybc/wtf-packages-report-EXAMPLE> for a
fully realized example.*
