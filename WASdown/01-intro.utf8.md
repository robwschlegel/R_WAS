# Introduction {#intro}

Before you will be in any shape to get **R**rring you will need to download the basics. There are lots of resources that can guide you through this process and it is not our intention to create duplicates. You can spend your time looking for answers online and there will surley be several versions of the same thing however, you would be wise to follow the likes of [\@hadleywickham](https://twitter.com/hadleywickham) in this process. Below there is an excerpt from his book co-authored with [\@statgarrett](https://twitter.com/statgarrett);

## Excerpt from [R for Data Science](http://r4ds.had.co.nz/index.html)

Taken from [R for Data Science](http://r4ds.had.co.nz/index.html) and unchanged licenced under the [Creative Commons Attribution-NonCommercial-NoDerivs 3.0](http://creativecommons.org/licenses/by-nc-nd/3.0/us/) United States License. 

### R 

To download R, go to CRAN, the **c**omprehensive **R** **a**rchive **n**etwork. CRAN is composed of a set of mirror servers distributed around the world and is used to distribute R and R packages. Don't try and pick a mirror that's close to you: instead use the cloud mirror, <https://cloud.r-project.org>, which automatically figures it out for you.

A new major version of R comes out once a year, and there are 2-3 minor releases each year. It's a good idea to update regularly. Upgrading can be a bit of a hassle, especially for major versions, which require you to reinstall all your packages, but putting it off only makes it worse.

### RStudio

RStudio is an integrated development environment, or IDE, for R programming. Download and install it from <http://www.rstudio.com/download>. RStudio is updated a couple of times a year. When a new version is available, RStudio will let you know. It's a good idea to upgrade regularly so you can take advantage of the latest and greatest features. For this book, make sure you have RStudio 1.0.0.

When you start RStudio, you'll see two key regions in the interface:

<img src="images/rstudio-console.png" width="75%" />

For now, all you need to know is that you type R code in the console pane, and press enter to run it. You'll learn more as we go along!

### The tidyverse

You'll also need to install some R packages. An R __package__ is a collection of functions, data, and documentation that extends the capabilities of base R. Using packages is key to the successful use of R. The majority of the packages that you will learn in this book are part of the so-called tidyverse. The packages in the tidyverse share a common philosophy of data and R programming, and are designed to work together naturally. 

You can install the complete tidyverse with a single line of code:


```r
install.packages("tidyverse")
```

On your own computer, type that line of code in the console, and then press enter to run it. R will download the packages from CRAN and install them on to your computer. If you have problems installing, make sure that you are connected to the internet, and that <https://cloud.r-project.org/> isn't blocked by your firewall or proxy. 

You will not be able to use the functions, objects, and help files in a package until you load it with `library()`. Once you have installed a package, you can load it with the `library()` function:


```r
library(tidyverse)
```

```
## Warning: package 'tidyverse' was built under R version 3.3.2
```

```
## Loading tidyverse: ggplot2
## Loading tidyverse: tibble
## Loading tidyverse: tidyr
## Loading tidyverse: readr
## Loading tidyverse: purrr
## Loading tidyverse: dplyr
```

```
## Warning: package 'tibble' was built under R version 3.3.2
```

```
## Warning: package 'tidyr' was built under R version 3.3.2
```

```
## Warning: package 'readr' was built under R version 3.3.2
```

```
## Warning: package 'purrr' was built under R version 3.3.2
```

```
## Warning: package 'dplyr' was built under R version 3.3.2
```

```
## Conflicts with tidy packages ----------------------------------------------
```

```
## filter(): dplyr, stats
## lag():    dplyr, stats
```

This tells you that tidyverse is loading the ggplot2, tibble, tidyr, readr, purrr, and dplyr packages. These are considered to be the __core__ of the tidyverse because you'll use them in almost every analysis.

### R Markdown

R Markdown provides an unified authoring framework for data science, combining your code, its results, and your prose commentary. R Markdown documents are fully reproducible and support dozens of output formats, like PDFs, Word files, slideshows, and more. 

R Markdown files are designed to be used in three ways:

1.  For communicating to decision makers, who want to focus on the conclusions,
    not the code behind the analysis.

1.  For collaborating with other data scientists (including future you!), who
    are interested in both your conclusions, and how you reached them (i.e.
    the code).
    
1.  As an environment in which to _do_ data science, as a modern day lab 
    notebook where you can capture not only what you did, but also what you
    were thinking.

R Markdown integrates a number of R packages and external tools. This means that help is, by-and-large, not available through `?`. Instead, as you work through this chapter, and use R Markdown in the future, keep these resources close to hand:

*   R Markdown Cheat Sheet: _Help > Cheatsheets > R Markdown Cheat Sheet_,

*   R Markdown Reference Guide: _Help > Cheatsheets > R Markdown Reference 
    Guide_.

Both cheatsheets are also available at <http://rstudio.com/cheatsheets>.

## Thesisdown


## Blogdown



## Git and Github

The initial process of getting gited is sometimes challenging but we encourage you to pursist and get it set up. Again, there are several online resources which provide detailed step by steps and it is not our intention to guide you through this but rather point you towards some of the 'good' ones.

For this section we have taken content from [Happy Git and GitHub for the useR](http://happygitwithr.com/) which was written by [\@JennyBryan](https://twitter.com/JennyBryan) and licenced under [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/).

### Why Git?

[Git](http://git-scm.com) is a __version control system__. Its original purpose was to help groups of developers work collaboratively on big software projects. Git manages the evolution of a set of files -- called a __repository__ -- in a sane, highly structured way. If you have no idea what I'm talking about, think of it as the "Track Changes" features from Microsoft Word on steroids.

Git has been re-purposed by the data science community. In addition to using it for source code, we use it to manage the motley collection of files that make up typical data analytical projects, which often consist of data, figures, reports, and, yes, source code.

A solo data analyst, working on a single computer, will benefit from adopting version control. But not nearly enough to justify the pain of installation and workflow upheaval. There are much easier ways to get versioned back ups of your files, if that's all you're worried about.

In my opinion, **for new users**, the pros of Git only outweigh the cons when you factor in the overhead of communicating and collaborating with other people. Who among us does not need to do that? Your life is much easier if this is baked into your workflow, as opposed to being a separate process that you dread or neglect.

### Why GitHub?

This is where hosting services like [GitHub](https://github.com), [Bitbucket](https://bitbucket.org), and [GitLab](https://about.gitlab.com) come in. They provide a home for your Git-based projects on the internet.  If you have no idea what I'm talking about, think of it as DropBox but much, much better. The remote host acts as a distribution channel or clearinghouse for your Git-managed project. It allows other people to see your stuff, sync up with you, and perhaps even make changes. These hosting providers improve upon traditional Unix Git servers with well-designed web-based interfaces.

Even for private solo projects, it's a good idea to push your work to a remote location for peace of mind. Why? Because it's fairly easy to screw up your local Git repository, especially when you're new at this. The good news is that often only the Git infrastructure is borked up. Your files are just fine! Which makes your Git pickle all the more frustrating. There are official Git solutions to these problems, but they might require expertise and patience you can't access at 3a.m. If you've recently pushed your work to GitHub, it's easy to grab a fresh copy, patch things up with the changes that only exist locally, and get on with your life.

Don't get too caught up on public versus private at this point. There are many ways to get private repositories from the major providers for low or no cost. Just get started and figure out if and how Git/GitHub is going to work for you! If you outgrow this arrangement, you can throw some combination of technical savvy and money at the problem. You can either pay for a higher level of service or self-host one of these platforms.

Outside of [\@JennyBryan](https://twitter.com/JennyBryan) book you can find a detailed guide to getting **Git**ed with RStudio by [/@juliesquid](https://twitter.com/juliesquid) [here](http://jules32.github.io/2016-07-12-Oxford/git/).

## Twitterverse 

You might also want to follow these guys on Twitter: 

* Hadley Wickham [\@hadleywickham](https://twitter.com/hadleywickham) 
* Garrett Grolemund [\@statgarrett](https://twitter.com/statgarrett)
* Chester Ismay [\@Old_Man_Chester](https://twitter.com/old_man_chester)
* Yihui Xie [\@xieyihui](https://twitter.com/xieyihui)
* Jenny Bryan [\@JennyBryan](https://twitter.com/JennyBryan)
* RStudio Tips [\@rstudiotips](https://twitter.com/rstudiotips)

If you're an active Twitter user, follow the `#rstats` hashtag.



