---
title: Cum construiesti un model in R
author: ineszz
date: '2020-09-06'
tags:
  - model
  - caret
  - saveRDS
slug: cum-construiesti-un-model-in-r
draft: yes
showonlyimage: yes
image: img/portfolio/ModelR-icon1.jpg
---

Un model in R se construieste similar oricarei alte tehnologii, desigur, cu mici specificitati datorate limbajului.

In primul rand, avem nevoie sa incarcam in memorie librariile care includ tehnicile si algoritmii utili realizarii unui model. 
Pentru acest articol, voi folosi un exemplu simplu in care voi apela datele din datesetul iris si librariile caret, ggplot.
> Daca doriti sa folositi alt, dataset apelati in consola 
> `data()`


```{r}
# Incarcam librariile
library(ggplot2)
library(caret)
```

```{r}
data("iris")
str(iris)
```

Hai sa construim un model

Incercam sa estimam latimea petalelor folosind lungimea lor 
```{r}
model <- lm(Petal.Length ~ Petal.Width, data = iris)
```
Sa vizualizam modelul
```{r}
ggplot(data = iris, aes(x = Petal.Width, y = Petal.Length)) + geom_point(aes(color = Species)) + stat_smooth(method = "lm")
```

Salvam modelul folosind saveRDS
```{r} 
saveRDS(model, "model_iris.RDS")
```

Acum putem citi modelul direct din fisier, salvand timpul pentru pregatirea modelului
```{r}
model_salvat <- readRDS("model_iris.RDS")
```

Putem verifica, prin comparatie, daca modelul salvat este similar celui construit.
```{r}
print(model$coefficients)
print(model_salvat$coefficients)
```
The end.

