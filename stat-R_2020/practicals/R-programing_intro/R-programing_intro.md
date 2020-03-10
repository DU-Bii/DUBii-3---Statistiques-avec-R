---
title: "Programming with R"
author: "Claire Vandiedonck & Jacques van Helden"
date: "2020-03-09"
output:
  html_document:
    self_contained: no
    code_folding: hide
    fig_caption: yes
    fig_height: 6
    fig_width: 7
    highlight: tango
    incremental: no
    keep_md: yes
    smaller: yes
    theme: cerulean
    toc: yes
    toc_depth: 3
    toc_float: yes
    widescreen: yes
  beamer_presentation:
    colortheme: dolphin
    fig_caption: yes
    fig_height: 6
    fig_width: 7
    fonttheme: structurebold
    highlight: tango
    incremental: no
    keep_tex: no
    slide_level: 2
    theme: Montpellier
    toc: yes
  pdf_document:
    fig_caption: yes
    highlight: zenburn
    toc: yes
    toc_depth: 3
  revealjs::revealjs_presentation:
    theme: night
    transition: none
    self_contained: no
    code_folding: hide
    css: ../../slides.css
  slidy_presentation:
    font_adjustment: 0   ## set to negative/positive values for smaller/bigger fonts
    duration: 45
    self_contained: no
    code_folding: hide
    fig_caption: yes
    fig_height: 6
    fig_width: 7
    highlight: tango
    incremental: no
    keep_md: yes
    smaller: yes
    theme: cerulean
    toc: yes
    widescreen: yes
  ioslides_presentation:
    self_contained: no
    code_folding: hide
    css: ../../slides.css
    fig_caption: yes
    fig_height: 6
    fig_width: 7
    highlight: tango
    smaller: yes
    toc: yes
    widescreen: yes
font-import: http://fonts.googleapis.com/css?family=Risque
subtitle: DUBii -- Statistics with R
font-family: Garamond
transition: linear
---




## Exercice 1 : test

- Créez un vecteur de 100 valeurs tirées aléatoirement selon une loi normale de moyenne 4 et d'écart type 5.

- Identifiez les indices des valeurs strictement supérieures à 3 et récupérez les valeurs correspondantes.

- Testez si la somme de ces valeurs est supérieure à 40, à 30 ou à 20 et affichez un message adéquat selon chaque éventualité.


**Fonctions à utiliser :** rnorm(), which(),sum(), if(),else if(),else(), cat() ou print()

## Exercice 2 : création d'une boucle simple

- Créez une boucle de 10 itérations `i` qui affiche à chaque itération l'indice `i`.
- Calculez au fur et à mesure la somme cumulée des indices dans un vecteur.
- Affichez la somme cumulée finale.

**Fonctions à utiliser :** for(), cat() ou print()


## Exercice 3 : création d'une fonction

- Créez une fonction `calculSomme` qui calcule la somme de deux variables x et y passées en argument.
- Testez la fonction.

**Fonctions à utiliser :** function(), return()

## Exercice 4: création d'une fonction avec des tests, utilisation de cette fonction de manière itérative

- Ecrivez une fonction `calculTarif` qui prend pour argument  un âge et affiche "demi-tarif" si l'âge est inférieur à 12 ans, "tarif sénior" si l'âge est supérieur ou égal à 60 ans et "plein tarif" sinon.
- Testez votre fonction pour des personnes de 5, 65, 85, 41, 23 et 47 ans.

**Fonctions à utiliser :** 

- `function()`, 
- `return()`, 
- `print()`, 
- `c()`

**Instructions conditionnelles: **
- `if`
- `else`
- `else if`
- `for`

## Exercice 5: création d'une fonction avec compteur de boucle

- Ecrivez une fonction `sumCumul` qui calcule la somme cumulée des nombres entiers compris entre deux bornes $a$ et $b$ que vous mettrez en arguments `start` et `end`.

- De plus, toutes les 10 boucles, vous affichez la valeur de l'entier ajouté, sinon vous affichez un point `.`.

- Testez la fonction avec les entiers entre 3 et 55 par exemple.

- Améliorez la fonction en ajoutant un paramètre `interval` correspondant à l'incrément de boucles entre les affichages des entiers (dans la fonction précédente, cet incrément était de 10)
Testez la fonction avec les entiers entre 3 et 55 et un intervalle de 15 par exemple.

**Fonctions à utiliser :** 

- `function()`, 
- `return()`, 
- `cat()`, 
- `seq()`



