--- 
theme: dashboard
title: World Heritage Sites
toc: false
---

# World Heritage Sites

```R
library(tidyverse)
data <- read_csv('heritage.csv') %>%
    pivot_longer(2:3)
ggplot(data) +
    geom_point(aes(x=Country,y=name,color=Year))
```