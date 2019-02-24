
<!-- README.md is generated from README.Rmd. Please edit that file -->
Data and Source R Markdown files with codes for *Pemahaman kuantitatif dasar dan penerapannya dalam mengkaji keterkaitan antara bentuk dan makna*
=================================================================================================================================================

[**Gede Primahadi Wijaya Rajeg**](https://figshare.com/authors/Gede_Primahadi_Wijaya_Rajeg/1234749) <a itemprop="sameAs" content="https://orcid.org/0000-0002-2047-8621" href="https://orcid.org/0000-0002-2047-8621" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon">orcid.org/0000-0002-2047-8621</a> <br>[**I Made Rajeg**](https://figshare.com/authors/I_Made_Rajeg/4052377) <a itemprop="sameAs" content="https://orcid.org/0000-0001-8989-0203" href="https://orcid.org/0000-0001-8989-0203" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon">orcid.org/0000-0001-8989-0203</a>

[![License: CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

The paper (in Indonesian) has just been accepted (with minor revision) for open-access publication in [*Linguistik Indonesia*](http://www.linguistik-indonesia.org), the flagship journal for the Linguistic Society of Indonesia ([*Masyarakat Linguistik Indonesia*](http://www.mlindonesia.org) \[MLI\]). The post-print version of the paper is available on [INA-Rxiv](https://doi.org/10.31227/osf.io/bt4h7), the Indonesian Preprint Server. The materials in this repository are licensed under the [Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/). See the `LICENSE` file for the details.

The folder `data` contains the raw concordance file in plain text format (i.e. `panas_raw.txt`) used in the paper. The file `panas_sample.txt` is used as illustrative subset of the raw data.

The paper is written using [R Markdown](https://rmarkdown.rstudio.com) [Notebook](https://bookdown.org/yihui/rmarkdown/notebook.html) that mixes prose and R codes together for generating reproducible scientific reports (see Frank & Hartgerink, [2017](#ref-frank_rmarkdown_2017) for overview). This source R Notebook file is named `panas_paper.Rmd` and is rendered into an MS Word output using the `word_document2()` function from the [bookdown](https://bookdown.org) R package (Xie, [2016](#ref-xie_bookdown_2016)).

The repository also includes an [RStudio](https://www.rstudio.com) project (i.e. `2018 Oct - PANAS.Rproj`). Double-click this file to open an RStudio session associated with data and materials in this repository so that the codes in the source R Markdown Notebook can be executed and run (see Wickham & Grolemund, [2017](#ref-wickham_r_2017), Ch. 8 for information on *projects*-based workflow in RStudio).

``` r
devtools::session_info()
#> ─ Session info ──────────────────────────────────────────────────────────
#>  setting  value                       
#>  version  R version 3.5.1 (2018-07-02)
#>  os       macOS  10.14.3              
#>  system   x86_64, darwin15.6.0        
#>  ui       X11                         
#>  language (EN)                        
#>  collate  en_US.UTF-8                 
#>  ctype    en_US.UTF-8                 
#>  tz       Australia/Melbourne         
#>  date     2019-02-24                  
#> 
#> ─ Packages ──────────────────────────────────────────────────────────────
#>  package     * version date       lib source        
#>  assertthat    0.2.0   2017-04-11 [1] CRAN (R 3.4.0)
#>  backports     1.1.2   2017-12-13 [1] CRAN (R 3.5.0)
#>  callr         3.1.1   2018-12-21 [1] CRAN (R 3.5.0)
#>  cli           1.0.1   2018-09-25 [1] CRAN (R 3.5.0)
#>  crayon        1.3.4   2017-09-16 [1] CRAN (R 3.4.1)
#>  desc          1.2.0   2018-05-01 [1] CRAN (R 3.5.0)
#>  devtools      2.0.1   2018-10-26 [1] CRAN (R 3.5.1)
#>  digest        0.6.15  2018-01-28 [1] CRAN (R 3.5.0)
#>  evaluate      0.11    2018-07-17 [1] CRAN (R 3.5.0)
#>  fs            1.2.3   2018-06-08 [1] CRAN (R 3.5.0)
#>  glue          1.3.0   2018-07-17 [1] CRAN (R 3.5.0)
#>  htmltools     0.3.6   2017-04-28 [1] CRAN (R 3.5.0)
#>  knitr         1.20    2018-02-20 [1] CRAN (R 3.5.0)
#>  magrittr      1.5     2014-11-22 [1] CRAN (R 3.4.0)
#>  memoise       1.1.0   2017-04-21 [1] CRAN (R 3.4.0)
#>  pkgbuild      1.0.2   2018-10-16 [1] CRAN (R 3.5.0)
#>  pkgload       1.0.2   2018-10-29 [1] CRAN (R 3.5.0)
#>  prettyunits   1.0.2   2015-07-13 [1] CRAN (R 3.5.0)
#>  processx      3.2.1   2018-12-05 [1] CRAN (R 3.5.0)
#>  ps            1.3.0   2018-12-21 [1] CRAN (R 3.5.0)
#>  R6            2.3.0   2018-10-04 [1] CRAN (R 3.5.0)
#>  Rcpp          1.0.0   2018-11-07 [1] CRAN (R 3.5.0)
#>  remotes       2.0.2   2018-10-30 [1] CRAN (R 3.5.0)
#>  rlang         0.3.1   2019-01-08 [1] CRAN (R 3.5.2)
#>  rmarkdown     1.11    2018-12-08 [1] CRAN (R 3.5.0)
#>  rprojroot     1.3-2   2018-01-03 [1] CRAN (R 3.4.3)
#>  sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 3.5.0)
#>  stringi       1.2.4   2018-07-20 [1] CRAN (R 3.5.0)
#>  stringr       1.3.1   2018-05-10 [1] CRAN (R 3.4.4)
#>  testthat      2.0.1   2018-10-13 [1] CRAN (R 3.5.0)
#>  usethis       1.4.0   2018-08-14 [1] CRAN (R 3.5.0)
#>  withr         2.1.2   2018-03-15 [1] CRAN (R 3.4.4)
#>  yaml          2.2.0   2018-07-25 [1] CRAN (R 3.5.0)
#> 
#> [1] /Users/Primahadi/Rlibs
#> [2] /Library/Frameworks/R.framework/Versions/3.5/Resources/library
```

References
==========

Frank, M., & Hartgerink, C. (2017, July 31). RMarkdown for writing reproducible scientific papers. Retrieved January 29, 2019, from <https://libscie.github.io/rmarkdown-workshop/handout.html>

Wickham, H., & Grolemund, G. (2017). *R for Data Science*. Canada: O’Reilly. Retrieved from <http://r4ds.had.co.nz/>

Xie, Y. (2016). *Bookdown: Authoring Books and Technical Documents with R Markdown*. Chapman and Hall/CRC.
