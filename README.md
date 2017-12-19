<!-- README.md is generated from README.Rmd. Please edit that file -->
tie
===

The goal of tie is to tie return values from function to

Example
-------

This is a basic example which shows you how to solve a common problem:

``` r
library(tie)

x <- rnorm(100)
tie[low,up] <- range(x)
low
#> [1] -3.243978
up
#> [1] 2.140045

tie[,q25,q50,q75,] <- quantile(x)
q25
#> [1] -0.5266646
q75
#> [1] 0.6280359

library(stringr)
fruits <- c(
  "apples and oranges and pears and bananas",
  "pineapples and mangos and guavas"
)
tie[left, right] <- str_split(fruits, " and ")
left
#> [1] "apples"  "oranges" "pears"   "bananas"
right
#> [1] "pineapples" "mangos"     "guavas"

tie[coef, res] = lm( Sepal.Length ~ Species, data = iris)
coef
#>       (Intercept) Speciesversicolor  Speciesvirginica 
#>             5.006             0.930             1.582
res
#>      1      2      3      4      5      6      7      8      9     10 
#>  0.094 -0.106 -0.306 -0.406 -0.006  0.394 -0.406 -0.006 -0.606 -0.106 
#>     11     12     13     14     15     16     17     18     19     20 
#>  0.394 -0.206 -0.206 -0.706  0.794  0.694  0.394  0.094  0.694  0.094 
#>     21     22     23     24     25     26     27     28     29     30 
#>  0.394  0.094 -0.406  0.094 -0.206 -0.006 -0.006  0.194  0.194 -0.306 
#>     31     32     33     34     35     36     37     38     39     40 
#> -0.206  0.394  0.194  0.494 -0.106 -0.006  0.494 -0.106 -0.606  0.094 
#>     41     42     43     44     45     46     47     48     49     50 
#> -0.006 -0.506 -0.606 -0.006  0.094 -0.206  0.094 -0.406  0.294 -0.006 
#>     51     52     53     54     55     56     57     58     59     60 
#>  1.064  0.464  0.964 -0.436  0.564 -0.236  0.364 -1.036  0.664 -0.736 
#>     61     62     63     64     65     66     67     68     69     70 
#> -0.936 -0.036  0.064  0.164 -0.336  0.764 -0.336 -0.136  0.264 -0.336 
#>     71     72     73     74     75     76     77     78     79     80 
#> -0.036  0.164  0.364  0.164  0.464  0.664  0.864  0.764  0.064 -0.236 
#>     81     82     83     84     85     86     87     88     89     90 
#> -0.436 -0.436 -0.136  0.064 -0.536  0.064  0.764  0.364 -0.336 -0.436 
#>     91     92     93     94     95     96     97     98     99    100 
#> -0.436  0.164 -0.136 -0.936 -0.336 -0.236 -0.236  0.264 -0.836 -0.236 
#>    101    102    103    104    105    106    107    108    109    110 
#> -0.288 -0.788  0.512 -0.288 -0.088  1.012 -1.688  0.712  0.112  0.612 
#>    111    112    113    114    115    116    117    118    119    120 
#> -0.088 -0.188  0.212 -0.888 -0.788 -0.188 -0.088  1.112  1.112 -0.588 
#>    121    122    123    124    125    126    127    128    129    130 
#>  0.312 -0.988  1.112 -0.288  0.112  0.612 -0.388 -0.488 -0.188  0.612 
#>    131    132    133    134    135    136    137    138    139    140 
#>  0.812  1.312 -0.188 -0.288 -0.488  1.112 -0.288 -0.188 -0.588  0.312 
#>    141    142    143    144    145    146    147    148    149    150 
#>  0.112  0.312 -0.788  0.212  0.112  0.112 -0.288 -0.088 -0.388 -0.688
```
