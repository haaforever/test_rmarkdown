Test 2
================

# Second test

``` r
library("RMySQL")
```

    ## Loading required package: DBI

    ## Warning: package 'DBI' was built under R version 4.1.2

``` r
library(knitr)
```

    ## Warning: package 'knitr' was built under R version 4.1.2

``` r
con.db <- dbConnect(drv = MySQL(), user = "iguana", password = "mlmobiis!", host = "192.168.100.189", dbname = "Haji")
dbListTables(con.db)
```

    ##  [1] "MTV_2010"                "MTV_2011"               
    ##  [3] "MTV_2012"                "MTV_2013"               
    ##  [5] "MTV_2014"                "MTV_2015"               
    ##  [7] "MTV_2016"                "MTV_2017"               
    ##  [9] "MTV_2018"                "MTV_2019"               
    ## [11] "MTV_2020"                "MTV_2021"               
    ## [13] "MTV_TP1v5_TP2v1"         "MTV_TP_viralref"        
    ## [15] "MTV_viralref_duplicated"

``` r
dt.tp1.v5 <- dbGetQuery(conn = con.db, statement = "SELECT * FROM MTV_viralref_duplicated")
kable(dt.tp1.v5[1:30,])
```

| definition                                                                     | num_samples | num_unique_seq |
|:-------------------------------------------------------------------------------|------------:|---------------:|
| ubiquitin E3 ligase ICP0 \[Human alphaherpesvirus 2\]                          |           2 |              2 |
| neurovirulence protein ICP34.5 \[Human alphaherpesvirus 2\]                    |           2 |              1 |
| transcriptional regulator ICP4 \[Human alphaherpesvirus 2\]                    |           2 |              1 |
| hypothetical protein \[High Plains wheat mosaic emaravirus\]                   |           4 |              4 |
| unnamed protein product \[Equus caballus papillomavirus 3\]                    |           6 |              6 |
| transforming protein \[Human papillomavirus 135\]                              |           2 |              2 |
| transforming protein \[Human papillomavirus 136\]                              |           2 |              2 |
| hypothetical protein \[Pig stool associated circular ssDNA virus GER2011\]     |           3 |              3 |
| putative VPg protein \[Artemisia virus A\]                                     |           2 |              1 |
| transforming protein \[Human papillomavirus type 137\]                         |           2 |              2 |
| transforming protein \[Human papillomavirus 140\]                              |           2 |              2 |
| transforming protein \[Human papillomavirus type 144\]                         |           2 |              2 |
| movement protein \[Deinbollia mosaic virus\]                                   |           2 |              2 |
| putative transmembrane protein \[Grapevine leafroll-associated virus 13\]      |           3 |              3 |
| hypothetical protein \[Mocis latipes granulovirus\]                            |          70 |             70 |
| 39K \[Mocis latipes granulovirus\]                                             |           2 |              2 |
| hypothetical protein \[Urbanus proteus nucleopolyhedrovirus\]                  |          38 |             38 |
| hypothetical protein \[Tilapia lake virus\]                                    |          10 |             10 |
| virion protein V67 \[Canid alphaherpesvirus 1\]                                |           2 |              1 |
| virion protein US10 \[Canid alphaherpesvirus 1\]                               |           2 |              1 |
| regulatory protein ICP22 \[Canid alphaherpesvirus 1\]                          |           2 |              1 |
| transcriptional regulator ICP4 \[Canid alphaherpesvirus 1\]                    |           2 |              1 |
| hypothetical protein \[Sclerotinia sclerotiorum fusarivirus 1\]                |           3 |              3 |
| hypothetical protein \[Grapevine Roditis leaf discoloration-associated virus\] |           3 |              3 |
| hypothetical protein \[Lutzomyia reovirus 1\]                                  |           3 |              3 |
| hypothetical protein \[Microviridae Bog5275_51\]                               |           2 |              2 |
| hypothetical protein \[Microviridae Bog1249_12\]                               |           3 |              3 |
| hypothetical protein \[Microviridae Fen7940_21\]                               |           2 |              2 |
| hypothetical protein \[Microviridae Fen7918_21\]                               |           2 |              2 |
| hypothetical protein \[Microviridae Fen7895_21\]                               |           2 |              2 |
