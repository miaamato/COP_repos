---
title: Intro_to_ggplot
author: Mia
date: '2022-02-07'
slug: intro-to-ggplot
categories: []
tags: []
---

#Intro
Typing words on ggplot2
## Starwars plot
starwars glimpse


```{r}
ggplot(data = starwars, mapping = aes(x = height, y = mass)) +
  geom_point() +
  labs(title = "Mass vs. height of Starwars characters",
       x = "Height (cm)", y = "Weight (kg)")
```

## Ascombe's quartet
```{r}
library(tidyverse)
library(palmerpenguins)
```

