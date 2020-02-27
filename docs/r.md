---
layout: default
title: R
nav_order: 18
description: "R commands and packages."
---

# R Programming Language
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Data Frame/Tibble
## Split a DF/Tbl to a List of DF/Tbl

The code below will split a DF/Tbl according to the values (e.g patterns) in a column and generate a named list (dictionary) of DF/Tbls. The names/keys of the list will be the same as the values used in the criteria to split the DF/Tbl.

```
split (DF, criteria)
example: x <- ttest_hg %>% split(f = .$Pattern)
```

# Colours in R

Package  
`gfDevices` from R core packages (https://www.rdocumentation.org/packages/grDevices/versions/3.4.1)

A list of very distinctive colours.   
`my_colours = grDevices::colors()[grep('gr(a|e)y', grDevices::colors(), invert = T)]`

Generate a list of rainbow colours.  
`my_colours = rainbow(n, s = 1, v = 1, start = 0, end = 5/6, alpha = 1)`  
Where n is the number of colours you want to sample from the spectrum. Start is Red and End is magenta