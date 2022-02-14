---
title: Visualizing Categorical Data
author: ''
date: '2022-02-09'
slug: visualizing-categorical-data
categories:
  - R
tags:
  - GGPLOT2
---
## cALL Libraries
```{r}
library(openintro)
glimpse(loans_full_schema)
loans <- loans_full_schema %>%
  select(loan_amount, interest_rate, term, grade, 
         state, annual_income, homeownership, debt_to_income)
glimpse(loans)
```
## PLOT
```{r}
ggplot(loans, aes(x = homeownership, fill = grade)) +
  geom_bar(positioin = "fill")
```
```{r}
ggplot(loans, aes(y = homeownership,
                  fill = grade)) +
  geom_bar(position = "fill") +
  labs(
    x = "Proportion",
    y = "Homeownership",
    fill = "Grade",
    title = "Grades of Lending Club loans",
    subtitle = "and homeownership of lendee"
  )
```
```{r}
ggplot(loans, aes(x = homeownership, y = loan_amount)) +
  geom_violin()

```


