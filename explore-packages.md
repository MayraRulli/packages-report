explore-packages.R
================
Mayra.Rulli
2019-06-11

``` r
library(tidyverse)
```

    ## Warning: package 'tidyverse' was built under R version 3.5.3

    ## -- Attaching packages ------------------------------------------------------------- tidyverse 1.2.1 --

    ## v ggplot2 3.1.0     v purrr   0.2.5
    ## v tibble  2.1.3     v dplyr   0.8.1
    ## v tidyr   0.8.3     v stringr 1.3.1
    ## v readr   1.1.1     v forcats 0.3.0

    ## Warning: package 'tibble' was built under R version 3.5.3

    ## Warning: package 'tidyr' was built under R version 3.5.3

    ## Warning: package 'dplyr' was built under R version 3.5.3

    ## -- Conflicts ---------------------------------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
.libPaths()
```

    ## [1] "C:/Users/Mayra.Rulli/Documents/R/win-library/3.5"
    ## [2] "C:/Program Files/R/R-3.5.1/library"

``` r
ipt <- installed.packages() %>%
  as.tibble %>%
  select(Package, LibPath, Version, Priority, Built)
```

    ## Warning: `as.tibble()` is deprecated, use `as_tibble()` (but mind the new semantics).
    ## This warning is displayed once per session.

``` r
ipt
```

    ## # A tibble: 154 x 5
    ##    Package    LibPath                                Version Priority Built
    ##    <chr>      <chr>                                  <chr>   <chr>    <chr>
    ##  1 agricolae  C:/Users/Mayra.Rulli/Documents/R/win-~ 1.2-8   <NA>     3.5.1
    ##  2 AlgDesign  C:/Users/Mayra.Rulli/Documents/R/win-~ 1.1-7.3 <NA>     3.5.0
    ##  3 askpass    C:/Users/Mayra.Rulli/Documents/R/win-~ 1.1     <NA>     3.5.3
    ##  4 assertthat C:/Users/Mayra.Rulli/Documents/R/win-~ 0.2.1   <NA>     3.5.3
    ##  5 backports  C:/Users/Mayra.Rulli/Documents/R/win-~ 1.1.3   <NA>     3.5.2
    ##  6 base64enc  C:/Users/Mayra.Rulli/Documents/R/win-~ 0.1-3   <NA>     3.5.2
    ##  7 BH         C:/Users/Mayra.Rulli/Documents/R/win-~ 1.69.0~ <NA>     3.5.2
    ##  8 bindr      C:/Users/Mayra.Rulli/Documents/R/win-~ 0.1.1   <NA>     3.5.1
    ##  9 bindrcpp   C:/Users/Mayra.Rulli/Documents/R/win-~ 0.2.2   <NA>     3.5.1
    ## 10 bitops     C:/Users/Mayra.Rulli/Documents/R/win-~ 1.0-6   <NA>     3.5.2
    ## # ... with 144 more rows
