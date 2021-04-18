---
date: "2020-12-30T15:44:32+05:30"
title: Cum sa folosesti regex in filtrarea listelor de marketing in R
author: ineszz
tags:
  - regex
  - liste-de-marketing
  
slug: cum-sa-folosesti-regex-in-filtrarea-listelor-de-marketing-in-r
draft: true
showonlyimage: yes
image: img/portfolio/icon-regex-r.jpg
---

Intotdeauna m-am intrebat cum pot sa-mi optimizez filtrele pentru tot felul de selectii pe care trebuie sa le fac in activitatea de base management. 

Zilele trecute, uitandu-ma pe coursera am descoperit un curs interesant de R, pe care am zis sa-l parcurg in ideea de a-mi improspata cunostiintele.


```{r}
df <- read_sav("./fisier.sav")

#Etichete pentru recode
lbls <- c('grupa 18-22', 
          'grupa 23-26', 
          'grupa 27-30', 
          'peste 30')

```
Voila! Asta a fost! ;-)