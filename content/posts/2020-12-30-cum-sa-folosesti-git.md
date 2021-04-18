---
date: "2020-12-30T15:44:32+05:30"
title: Cum sa folosesti git
author: ineszz
tags:
  - git
  
slug: cum-sa-folosesti-git
draft: false
showonlyimage: false
---

Git este un sistem de mentinere a versionarii codului lucrat. Util in colaborarea pe proiecte de coding folosind Github sau Gitlab. Acesta ajuta la eliminarea riscurilor pierderii codului salvat in anumite etape. <!--more-->

Primul pas in folosirea **git** : [download](https://git-scm.com/downloads).
<br>Ulterior, trebuie configurat pentru a putea fi utilizat. 
Pentru asta este nevoie de o interfata GitBash care se instaleaza o data cu downloadul anterior, in care sa putem introduce un utilizator, al vostru, si o adresa de email:

```
git config --global user.name "Jane Doe"
git config --global user.email "jane.doe@somewhere.com"
```
Imediat ce am facut pasii anterior, restartam R Studio pentru ca IDE-ul nostru sa identifice git. Daca totusi, nu apare, el poate fi activat folosind calea: **Tools -> Options -> GIT/SVN**.

Cele mai intalnite situatii in folosirea curenta:
- initializarea **git**;
- setarea unui director specific
- activitatea curenta pe un director existent.

Initializarea unui director
```
cd ~/director-examplu
git init
```
Acest lucru se poate face si folosind un IDE, de exemplu R Studio.
Imediat ce director a fost initializat, vom putea continua cu commit-uri, push-uri si pull-uri pentru sincronizarea proiectului la anumite momente in care se salveaza codul.


Alte comenzi utile:
```
pwd: verific in ce director este activ git
cd: change directory
git status : verific status
rm -rf .git : sterg directorul cu git
git remote add origin https://github.com/ineszz/blog.git: adaug directorului local un director github

git commit -m "your comment" : initializez salvarea versiunii
git push -u origin master : trimit catre baza versiunea salvata
```
Un flow uzual:
```
git add folder/
git commit -m "notes"
git push
```

Un flow pentru un folder existent:
```
git remote add origin https://github.com/ineszz/blog.git
git branch -M main
git push -u origin main
```

Daca notitele mele sunt incomplete, ajuta-ma, fie direct pe github, fie scrie-mi💌😊. Imi poti scrie si daca ti-a placut ! 😉