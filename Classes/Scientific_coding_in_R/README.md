# Scientific Coding in R
This document contains an introduction to scientific coding in R. We will discuss:
1) how to download the necessary software
2) resources to get started
3) best practices for coding in R!

## Why Use R for Scientific Programming?
- **Statistical Power**: R is a language that is commonly used for statistical analysis and data visualization. It was designed by statisticians and excels in heavy-duty data analysis!
 - **Community**: There is a vast open-source community of R users that consists of developers and domain experts in a wide variety of scientific fields. This community develops and supports R packages for almost any scientific application you can think of!

## Software
- The latest version of R can be downloaded here: https://cran.r-project.org/
- RStudio is the text-editing software where coding projects are built. This can be downloaded here: https://posit.co/downloads/
- Within RStudio, users can create projects, markdown files, and interface directly with local files on the computer. 

## Getting Started
[Datacamp](https://www.datacamp.com/users/sign_in) provides free tutorials to get started with coding in R. 

### Basic Concepts and Workflow
1) R Scripts (`.R`): R Scripts are one of the major files you will develop in R. Scripts are text files that include lines of R code. 
2) R Markdown (`.Rmd`): R markdown files are documents that include text, code, and results (visualizations, output, etc.) in one file. You might use an R Markdown file to publish or share the results of your analyses!
3) The R Console: When you open up R or R Studio, you will be met with a **console** where you can type commands and view the output of your R scripts. A basic Workflow in R may proceed as follows:
- Writing code in a `.R` file
- Running code line-by-line or in code blocks
- Viewing the results of your code in the R console. 

When beginning in R, it is important to become familiar with basic commands. Start by:
1) Loading and storing a practice dataset: `data <- read.csv()`
2) Performing basic calculations with data or practice vectors.
3) Installing a basic package, such as tidyverse using `install.packages(“tidyr”)`.
4) Using the `help()` function to obtain information about syntax and function of commands in R, as well as helpful examples.

**Example basic code**
```r
library(tidyr)
vector <- c(1,3,5,7,9)
mean(vector)
help(mean)
help(boxplot)
```

## Building Proficiency
Online forums such as [R for Ecology](https://www.rforecology.com/) and [geeksforgeeks.org](https://www.geeksforgeeks.org/) are public resources to learn how to use advanced functions and understand complicated syntax.

AI LLMs such as [Cursor](https://cursor.com/) can be powerful tools to help write complicated programs. However, these tools should only be leveraged once users have developed proficiency in R and can understand the syntax and functionality of code that has been written with AI. 

Online courses are offered at [DataCamp](https://www.datacamp.com/), [Coursera](https://www.coursera.org/), and [LinkedIn Learning](https://www.linkedin.com/learning/) on various subjects for all skill levels.

## Best Practices
- Keep track of who wrote the code and its intended purpose by writing a 1-2 sentence description at the beginning of the file.
- Load all packages necessary for your code before you begin coding.
- Set a consistent working directory before beginning. 
- Define variables early in your code and use consistent naming conventions.
- Add clear comments about each part of your code.
- Keep your code in bit-sized chunks and avoid repetition by using functions or loops.
