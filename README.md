# quality-trend
---
title: "quality"
author: "wei he"
date: "2025-08-12"
output: html_document
---
# Load libraries

```{r cars}
library(tidyverse)

# Read CSV
df <- read_csv("defect_rate_analysis_july2025.csv")
# Quick view
glimpse(df)
summary(df)
# Replace missing defect type with "None"
df <- df %>%
  mutate(`Top Defect Type` = ifelse(is.na(`Top Defect Type`), "None", `Top Defect Type`))
```
## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:


## Including Plots

You can also embed plots, for example:

```{r pressure, echo=FALSE}
plot(pressure)
```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
