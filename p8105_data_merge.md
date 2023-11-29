p8105_final_wl2926
================
2023-10-18

``` r
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.3     ✔ readr     2.1.4
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.0
    ## ✔ ggplot2   3.4.3     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.2     ✔ tidyr     1.3.0
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

## Clean and merge the data

``` r
red_df <- read.csv("data/Red.csv")
rose_df <- read.csv("data/Rose.csv")
white_df <- read.csv("data/White.csv")
sparkling_df <- read.csv("data/Sparkling.csv")
varieties_df<- read.csv("data/varieties.csv")

# Merge Red with Rose
merged_df_1<-merge(red_df, rose_df, by = intersect(names(red_df), names(rose_df)), all.x = TRUE )
# Merge the result with White
merged_df_2 <- merge(merged_df_1, white_df, by = intersect(names(merged_df_1), names(white_df)), all.x = TRUE)

# Finally, merge the result with Sparkling
final_merged_df <- merge(merged_df_2, sparkling_df, by = intersect(names(merged_df_2), names(sparkling_df)), all.x = TRUE)

head(final_merged_df)
```

    ##                                       Name       Country                Region
    ## 1             'Rosso & Bianco' Shiraz 2016 United States            California
    ## 2         (B) Old Vine Zinfandel Lodi 2017 United States                  Lodi
    ## 3         1 Uno Primitivo di Manduria 2018         Italy Primitivo di Manduria
    ## 4 1 Uno Primitivo di Manduria Riserva 2016         Italy Primitivo di Manduria
    ## 5                         10 Barricas 2015         Spain                 Cádiz
    ## 6             1000X Cabernet - Merlot 2012       Austria            Burgenland
    ##                 Winery Rating NumberOfRatings Price Year
    ## 1 Francis Ford Coppola    3.8             133 13.25 2016
    ## 2               Brazin    4.1             504 15.90 2017
    ## 3    Masseria La Volpe    4.3            1732 12.06 2018
    ## 4    Masseria La Volpe    4.3             148 14.18 2016
    ## 5        Finca Moncloa    4.3              25 37.60 2015
    ## 6      Feiler-Artinger    4.2              46 30.47 2012

``` r
write.csv(final_merged_df, "final_merged_data.csv", row.names = FALSE)
# Assuming final_merged_df is your final merged dataset
final_merged_df$Variety <- NA
write.csv(final_merged_df, "updated_final_merged_data.csv", row.names = FALSE)
```
