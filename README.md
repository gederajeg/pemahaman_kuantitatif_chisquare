
<!-- README.md is generated from README.Rmd. Please edit that file -->
Data and Source R Markdown files with codes for *Pemahaman kuantitatif dasar dan penerapannya dalam mengkaji keterkaitan antara bentuk dan makna*
=================================================================================================================================================

[**Gede Primahadi Wijaya Rajeg**](https://figshare.com/authors/Gede_Primahadi_Wijaya_Rajeg/1234749) <a itemprop="sameAs" content="https://orcid.org/0000-0002-2047-8621" href="https://orcid.org/0000-0002-2047-8621" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon">orcid.org/0000-0002-2047-8621</a> <br>[**I Made Rajeg**](https://figshare.com/authors/I_Made_Rajeg/4052377) <a itemprop="sameAs" content="https://orcid.org/0000-0001-8989-0203" href="https://orcid.org/0000-0001-8989-0203" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon">orcid.org/0000-0001-8989-0203</a>

[![License: CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

The paper (in Indonesian) has just been accepted (with minor revision) for open-access publication in [*Linguistik Indonesia*](http://www.linguistik-indonesia.org), the flagship journal for the Linguistic Society of Indonesia ([*Masyarakat Linguistik Indonesia*](http://www.mlindonesia.org) \[MLI\]). The materials in this repository are licensed under the [Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/). See the `LICENSE` file for the details.

The folder `data` contains the raw concordance file in plain text format (i.e. `panas_raw.txt`) used in the paper. The file `panas_sample.txt` is used as illustrative subset of the raw data.

The paper is written using [R Markdown](https://rmarkdown.rstudio.com) [Notebook](https://bookdown.org/yihui/rmarkdown/notebook.html) that mixes prose and R codes together for generating reproducible scientific reports (see Frank & Hartgerink, [2017](#ref-frank_rmarkdown_2017) for overview). This source R Notebook file is named `panas_paper.Rmd` and is rendered into an MS Word output using the `word_document2()` function from the [bookdown](https://bookdown.org) R package (Xie, [2016](#ref-xie_bookdown_2016)).

The repository also includes an [RStudio](https://www.rstudio.com) project (i.e. `2018 Oct - PANAS.Rproj`). Double-click this file to open an RStudio session associated with data and materials in this repository so that the codes in the source R Markdown Notebook can be executed and run (see Wickham & Grolemund, [2017](#ref-wickham_r_2017), Ch. 8 for information on *projects*-based workflow in RStudio).

``` r
devtools::session_info()
#> Session info -------------------------------------------------------------
#>  setting  value                       
#>  version  R version 3.5.1 (2018-07-02)
#>  system   x86_64, darwin15.6.0        
#>  ui       X11                         
#>  language (EN)                        
#>  collate  en_US.UTF-8                 
#>  tz       Australia/Melbourne         
#>  date     2019-01-29
#> Packages -----------------------------------------------------------------
#>  package   * version date       source        
#>  backports   1.1.2   2017-12-13 CRAN (R 3.5.0)
#>  base      * 3.5.1   2018-07-05 local         
#>  compiler    3.5.1   2018-07-05 local         
#>  datasets  * 3.5.1   2018-07-05 local         
#>  devtools    1.13.6  2018-06-27 CRAN (R 3.5.0)
#>  digest      0.6.15  2018-01-28 CRAN (R 3.5.0)
#>  evaluate    0.11    2018-07-17 CRAN (R 3.5.0)
#>  graphics  * 3.5.1   2018-07-05 local         
#>  grDevices * 3.5.1   2018-07-05 local         
#>  htmltools   0.3.6   2017-04-28 CRAN (R 3.5.0)
#>  knitr       1.20    2018-02-20 CRAN (R 3.5.0)
#>  magrittr    1.5     2014-11-22 CRAN (R 3.4.0)
#>  memoise     1.1.0   2017-04-21 CRAN (R 3.4.0)
#>  methods   * 3.5.1   2018-07-05 local         
#>  Rcpp        0.12.18 2018-07-23 CRAN (R 3.5.1)
#>  rmarkdown   1.10    2018-06-11 CRAN (R 3.5.0)
#>  rprojroot   1.3-2   2018-01-03 CRAN (R 3.4.3)
#>  stats     * 3.5.1   2018-07-05 local         
#>  stringi     1.2.4   2018-07-20 CRAN (R 3.5.0)
#>  stringr     1.3.1   2018-05-10 cran (@1.3.1) 
#>  tools       3.5.1   2018-07-05 local         
#>  utils     * 3.5.1   2018-07-05 local         
#>  withr       2.1.2   2018-03-15 cran (@2.1.2) 
#>  yaml        2.2.0   2018-07-25 cran (@2.2.0)
```

References
==========

Frank, M., & Hartgerink, C. (2017, July 31). RMarkdown for writing reproducible scientific papers. Retrieved January 29, 2019, from <https://libscie.github.io/rmarkdown-workshop/handout.html>

Wickham, H., & Grolemund, G. (2017). *R for Data Science*. Canada: O’Reilly. Retrieved from <http://r4ds.had.co.nz/>

Xie, Y. (2016). *Bookdown: Authoring Books and Technical Documents with R Markdown*. Chapman and Hall/CRC.
