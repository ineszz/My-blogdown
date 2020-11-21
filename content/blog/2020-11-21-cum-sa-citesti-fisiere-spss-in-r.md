---
title: Cum sa citesti fisiere SPSS in R
author: ineszz
date: '2020-11-21'
tags:
  - SPSS
  - haven
  - recode
slug: cum-sa-citesti-fisiere-spss-in-r
draft: yes
showonlyimage: yes
image: img/portfolio/icon-spss-r.jpg
---

Zilele trecute, o cunostiinta m-a intrebat ce face daca s-a blocat SPSS-ul si nu mai poate face recode la informatiile nou introduse.

> hmmm...

Primul gand a fost "Hai sa facem in R!" stiu un pachet care citeste fisiere din SPSS, chiar SAS, si l-as putea testa cu ocazia asta :-).

Pana sa se hotarasca cum va proceda, am deschis helpul pachetului [*haven*](https://haven.tidyverse.org/) si am gasit cum sa citesc un fisier SPSS.


> read_sav("./fisier.sav") 

! Nu uitati sa incarcati libraria tidyverse inainte (*haven* este inclusa in ecosistemul **tidyverse**).

Am citit fisierul, am facut o scurta simulare de data wrangling construind o variabila categoricala. Pornind de la o variabila numerica, sa zicem varsta (Age) am impartit in clase predefinite folosind functia cut.

```{r}
df <- read_sav("./fisier.sav")

#Etichete pentru recode
lbls <- c('grupa 18-22', 
          'grupa 23-26', 
          'grupa 27-30', 
          'peste 30')
#aplic grupele          
df<-df %>% 
  mutate(AgeGroup = cut(Age, 
        breaks = c(seq(18, 30, by = 4), Inf),include.lowest=TRUE, 
        labels = lbls)
        )

#export inapoi in SPSS formatul sav
write_sav(df, "./fisier_out.sav")

```
Voila! Asta a fost! ;-)