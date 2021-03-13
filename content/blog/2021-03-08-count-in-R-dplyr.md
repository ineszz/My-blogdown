---
date: "2021-03-07T15:44:32+05:30"
title: How to count in R dplyr
author: ineszz
tags:
  - dplyr
  - count
  - EN
  
slug: count-in-R-dplyr
draft: false
showonlyimage: false
---

I decided to explore some common functions from tidyverse ecosystem in an attempt to start participating in the #tidytuesday. 

**count** verb is one of the most used functions I noticed in most of the participants scripts. Coming from an SQL/SAS background to R, I usually either think in plain SQL counts or proc freq's for counting. 

In R, I discovered the dplyr and in my first attempts I've always used the SQL mindset: group_by, then summarize.

However, **count()** verb is quite easy to use. Let's deep dive the options:

```
# basic count
df %>% count(column)

# basic ordered count
df %>% count(column, sort = TRUE)

# multiple groups ordered count
df %>% count(column1, column2, sort = TRUE)

# counts on data cubes structure with wt option
df %>% count(column2, wt = freq)

```


If you find my notes to be incomplete, help me via github or write me 💌😊. You can send me a message if you liked my post too! 😉