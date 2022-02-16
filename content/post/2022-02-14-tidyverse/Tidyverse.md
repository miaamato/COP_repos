---
title: Tidyverse
author: ''
date: '2022-02-14'
slug: tidyverse
categories: []
tags: []
---
#C01 assignment

```{r}
library(dplyr)
library(tidyverse)
hotels <- read_csv("https://github.com/miaamato/tidyverse/blob/main/hotels.csv?raw=true")
names(hotels)
glimpse(hotels)
select(hotels, lead_time)
```
#multiple columns
```{r}
select(hotels, hotel, lead_time)
hotels %>%
  select(hotel, lead_time) %>%
  arrange(desc(lead_time))
```
#ggplot incorporation
```{r}
ggplot(hotels, aes(hotel, fill = deposit_type)) +
  geom_bar()
```

