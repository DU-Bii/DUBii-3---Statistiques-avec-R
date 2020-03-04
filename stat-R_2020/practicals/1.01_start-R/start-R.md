---
title: "Start R -- First steps with R and RStudio"
author: "Claire Vandiedonck & Jacques van Helden"
date: "2020-03-03"
output:
  slidy_presentation:
    font_adjustment: 0   ## set to negative/positive values for smaller/bigger fonts
    duration: 45
    self_contained: no
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
    self_contained: true
    css: ../../slides.css
  html_document:
    self_contained: no
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
  ioslides_presentation:
    self_contained: no
    css: slides.css
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





## Connection to IFB RStudio server

In a Web browser, open a connection to the IFB RStudio server

<https://rstudio.cluster.france-bioinformatique.fr/>

This requires your login and password. 

Check the version of R and of loaded packages.

```r
## Print info about the session
sessionInfo()
```

```
R version 3.5.1 (2018-07-02)
Platform: x86_64-redhat-linux-gnu (64-bit)
Running under: CentOS Linux 7 (Core)

Matrix products: default
BLAS/LAPACK: /usr/lib64/R/lib/libRblas.so

locale:
 [1] LC_CTYPE=en_US.UTF-8       LC_NUMERIC=C               LC_TIME=en_US.UTF-8        LC_COLLATE=en_US.UTF-8     LC_MONETARY=en_US.UTF-8    LC_MESSAGES=en_US.UTF-8    LC_PAPER=en_US.UTF-8       LC_NAME=C                  LC_ADDRESS=C               LC_TELEPHONE=C            
[11] LC_MEASUREMENT=en_US.UTF-8 LC_IDENTIFICATION=C       

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
[1] knitr_1.25

loaded via a namespace (and not attached):
 [1] compiler_3.5.1  magrittr_1.5    tools_3.5.1     htmltools_0.4.0 yaml_2.2.0      Rcpp_1.0.3      stringi_1.4.6   rmarkdown_1.16  stringr_1.4.0   xfun_0.10       digest_0.6.25   rlang_0.4.5     evaluate_0.14  
```



# Navigating in your folders


## Where am I?


```r
## Where am I now?
getwd()

## Where is my home?
Sys.getenv("HOME")

## Who am I?
Sys.getenv("LOGNAME")

## Go home
setwd(Sys.getenv("HOME"))
setwd("~")  ## An easier way
```

### Explanations

- `Sys.getenv()` returns all the environment variables
- `$HOME` is a Unix variable environment indicating the home directory
- `$LOGNAME` is my login name (did you guess?)
- in Unix, `~` denotes your home directory (equivalent to `$HOME`)


## Creating a work space for this course

We will create specific directory to store the data and results of the practicals for this course.


```r
## Define the directory for this course
courseDir <- file.path("~", "dubii20", "stat-R", "session1")
print(courseDir) ## Check the result

## Create the directory
dir.create(courseDir) ## THIS WILL LIKELY NOT WORK
dir.create(path = courseDir, 
           recursive = TRUE, ## Create the parent directories
           showWarnings = FALSE) ## Don't shout it already exists

## Go to this directory
setwd(courseDir)
getwd() ## Check that you are in the right place
```

# Exercises: handling R objects: the main R objects

## 1. Creating matrices

1.1. Create an identity matrix named `identityMat` of dimensions $10 \times 10$. 
1.2. Create a matrix named `randomMat` and fill it up with random values following a normal distribution with mean $\mu=0$ and variance $\sigma^2=5$.

**Tips**

- Identity matrices contain 1 on the diagonal, and 0 everywhere else
- Functions: `matrix()`, `diag()`, `rnorm()`

## 2. Combining vectors and matrices

2.1 Create two random vectors named `x1` and `x2`, containing 100 random values following respectively: 

    - a standard normal law
    - a uniform law spreading from 0 to 10

2.2. Create a matrix named `m1` whose first column contains the 10 first values of `x1`and the second one the 10 last values of `x2`. 

## 2. Combining vectors and matrices (continued)

2.3. Create a matrix named `m2` whose first column contains contains the  16th, 51th, 79the, 31the et 27th values of `x2` valeurs de x1, and whose second column contains the 30th, 70th, 12th, 49th et 45th values of `x2`.

2.4. 


## Load the data for this course

Data and files are stored on the cluster in the directory `/shared/projects/dubii2020/data/module3/seance1/`

We will download the data `Prerequis.RData`  that you saved during the prerequisites session.


```r
## Define the path of the files
data_path <- "/shared/projects/dubii2020/data/module3/seance1/"
print(data_path) ## Check the result

## Load the data from this path
load(paste(data_path, "Prerequis.RData", sep=""))

## List the data you have dowloaded, check their struture and keep in your session only the three vectors called size, weight and bmi as well as the matrix called myData2
ls()

## to complete...
```

Finally, open the script `DUBii_R_Session1.R` stored in the same directory as the data.
