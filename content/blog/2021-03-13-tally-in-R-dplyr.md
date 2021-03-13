---
date: "2021-03-13T15:44:32+05:30"
title: How to tally in R dplyr
author: ineszz
tags:
  - dplyr
  - tally
  - EN
  
slug: tally-in-R-dplyr
draft: false
showonlyimage: false
---

I decided to explore some common functions from tidyverse ecosystem in an attempt to start participating in the #tidytuesday. <!--more-->

**tally** verb is another used functions I noticed in the participants scripts. 

Let's deep dive on some options:

```
# simple wrapper to summarize number of observations from a dataframe, similar to nrow()
df %>% tally()

# basic ordered , could be replaced with previous blog post - **count()**
df %>% group_by(grup) %>% tally(column, sort = TRUE)

# using all function options
df %>% tally(column1, wt=w, sort = TRUE, name="Total")


```


If you find my notes to be incomplete, help me via github or write me 💌😊. You can send me a message if you liked my post too! 😉