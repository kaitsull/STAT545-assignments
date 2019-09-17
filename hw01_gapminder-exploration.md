HW 01: Gapminder Exploration
================
Kaitlin Sullivan

## The Gapminder Dataframe

### *Let’s explore the gapminder dataframe\!*

The gapminder dataframe contains **6 columns** with information about
**life expectancies, population,** and **GDP percapita** in various
countries.

``` r
#number of columns in the gapminder dataframe
ncol(gapminder)
```

    ## [1] 6

``` r
#names of columns in the gapminder dataframe
names(gapminder)
```

    ## [1] "country"   "continent" "year"      "lifeExp"   "pop"       "gdpPercap"

There is information provided **every 5 years**, from **1952-2007**.

``` r
#interval of years between datapoints
interval<-(gapminder$year[2]-gapminder$year[1])
paste(c('data provided every', interval, 'years'), collapse = " ")
```

    ## [1] "data provided every 5 years"

``` r
#minimum and maximum year in gapminder dataset
x<-min(gapminder$year)
y<-max(gapminder$year)
paste(c('from', x,'to', y), collapse = " ")
```

    ## [1] "from 1952 to 2007"

The average life expectancy at birth in **1952** was **49 years**.

``` r
#average life expectancy 1952
minExp<-subset(gapminder, year == 1952, lifeExp)
mean(minExp$lifeExp)
```

    ## [1] 49.05762

The average life expectancy at birth in **2007** was **67 years**.

``` r
#average life expectancy 2007
maxExp<-subset(gapminder, year == 2007, lifeExp)
mean(maxExp$lifeExp)
```

    ## [1] 67.00742
