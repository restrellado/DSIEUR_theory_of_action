R Notebook
================

# Theory of Action

When new R users in education are provided with scaffolding as they read
the book and provided with relatable education datasets to practice
with, they increase the likelihood of introducing data science into the
education work environment.

# Measuring engagement with scaffolding techniques

Survey questions like:

How true were the following statements after you read the book

  - I learned from the vocabulary sections at the start of each chapter
  - I learned from asking questions in the DSIEUR Slack channel
  - I learned from reviewing the coding walkthroughs before practicing
  - I learned from reviewing the preview questions at the start of each
    chapter

# Measuring engagement with relatable education datasets

Survey questions like:

How true were the following statements after you read the book

  - The datasets used in the walkthroughs are ones that might appear in
    my education workplace

# Measuring introduction of data science into the education work place

Survey questions like:

How true were the following statements after you read the book

  - During the time I was reading the book, data science techniques were
    being used regulalry in my education workplace
  - After reading the book, I could identify at least one action I could
    take to begin introducing data science techniques in my education
    workplace
  - After reading the book, I acted on at least one action item to
    introduce data science techniques in my education workplace

<!-- end list -->

``` r
# Example dataset
library(tidyverse) 
```

    ## ── Attaching packages ────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 3.2.0     ✔ purrr   0.3.2
    ## ✔ tibble  2.1.3     ✔ dplyr   0.8.3
    ## ✔ tidyr   0.8.3     ✔ stringr 1.4.0
    ## ✔ readr   1.3.1     ✔ forcats 0.4.0

    ## ── Conflicts ───────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
surveys <- tibble(
  respondent_id = rep(c(1:2), 3), 
  scaffolding = sample(1:5, 6, replace = TRUE), 
  datasets = sample(1:5, 6, replace = TRUE), 
  used_techniques = sample(1:5, 6, replace = TRUE), 
)
surveys
```

    ## # A tibble: 6 x 4
    ##   respondent_id scaffolding datasets used_techniques
    ##           <int>       <int>    <int>           <int>
    ## 1             1           2        4               5
    ## 2             2           3        3               1
    ## 3             1           5        5               5
    ## 4             2           5        3               4
    ## 5             1           1        1               4
    ## 6             2           4        5               4

# Other data

Conduct interviews to learn more about the experience of reading the
book and trying the ideas in the workplace.
