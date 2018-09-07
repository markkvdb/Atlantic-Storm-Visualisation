Atlantic Storm Visualisation
================

Introduction
------------

This document contains my solutions to the exercises as presented in \[<https://www.r-bloggers.com/specialize-in-geo-spatial-visualizations-with-leaflet-part-2-exercises/>\].

First we need to load the **leaflet** package and the dataset **atlStorms2005**.

``` r
library(tidyverse)
```

    ## ── Attaching packages ──────────────────────────────────────────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 2.2.1     ✔ purrr   0.2.4
    ## ✔ tibble  1.3.4     ✔ dplyr   0.7.4
    ## ✔ tidyr   0.7.2     ✔ stringr 1.2.0
    ## ✔ readr   1.1.1     ✔ forcats 0.2.0

    ## ── Conflicts ─────────────────────────────────────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
library(leaflet)

data = leaflet::atlStorms2005
```

Exercise 1
----------

Set the default view to longitude -47.4, latitude 39.75 and zoom level 3. In addition, add a button that will scale back to the default view upon clicking it. Hint: use the icon() function from the shiny package to easily render an icon of your choice for the button.

### Solution

``` r
map = data %>%
  leaflet() %>%
  setView(lng = -47.4,
          lat = 39.75,
          zoom = 3) %>%
  addTiles()
```

    ## Loading required package: sp

``` r
print(map)
```

Exercise 2
----------

Add the lines that represent the storms traces to the map.

### Solution

Exercise 3
----------

Color each line according to the storm max wind.

### Solution

Exercise 4
----------

Add a legend to the colors you just added.

### Solution

Exercise 5
----------

Upon hovering over a line, change its weight to 10.

### Solution
