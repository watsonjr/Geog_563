# Scientific Coding in R
This document introduces the basics of **scientific coding in R**. It includes key information on:
1. Installing the necessary software.
2. Learning foundational concepts and workflow. 
3. Developing good coding practices. 


## Why Use R for Scientific Programming?
**Statistical Power:** R is a language that is commonly used for statistical analysis and data visualization. It was designed by statisticians and excels in heavy-duty data analysis!
 **Community:** There is a vast open-source community of R users that consists of developers and domain experts in a wide variety of scientific fields. This community develops and supports R packages for almost any scientific application you can think of!


## Software
- **R**: Download the latest version from [CRAN](https://cran.r-project.org/).  
- **RStudio (Posit)**: Download the integrated development environment (IDE) from [Posit](https://posit.co/downloads/).

RStudio is a user-friendly interface where you can:
- Create and manage projects  
- Write R scripts `.R` and R Markdown reports `.Rmd`  
- View plots, manage your environment, manage libraries, and explore files 


## Learning Resources
[Datacamp](https://www.datacamp.com/users/sign_in) provides free interactive courses to get started with coding in R. 

Online forums such as [R for Ecology](https://www.rforecology.com/) and [geeksforgeeks.org](https://www.geeksforgeeks.org/) are public resources to learn how to use advanced functions and understand complicated syntax.

LLMs such as [https://cursor.com/](Cursor) can be powerful tools to help write complicated programs. However, these tools should only be leveraged once users have developed proficiency in R and can understand the syntax and functionality of code that has been written with AI. 

Online courses are offered at DataCamp, Coursera, and LinkedIn Learning on various subjects for all skill levels.
**DataCamp** - https://www.datacamp.com/
**Coursera** - https://www.coursera.org/
**LinkedIn Learning** - https://www.linkedin.com/learning/

## Core File Types
R Scripts (`.R`): R Scripts are one of the major files you will develop in R. Scripts are text files that include lines of R code. 
R Markdown (`.Rmd`): R markdown files are documents that include text, code, and results (visualizations, output, etc.) in one file. You might use an R Markdown file to publish or share the results of your analyses!
The R Console: When you open up R or R Studio, you will be met with a **console** where you can type commands and view the output of your R scripts. A basic Workflow in R may proceed as follow:
Writing code in a `.R` file
Running code line-by-line or in code blocks
Viewing the results of your code in the R console.

### Table 1. File Types 
| File Type | Description | Typical Use |
|------------|--------------|--------------|
| `.R` | Plain R script containing lines of code | Writing and running analysis pipelines |
| `.Rmd` | R Markdown file combining code, text, and results | Creating reproducible reports |
| Console | Interactive prompt for running commands | Testing functions or small snippets |

## Getting Started
Now that we know a bit more about what R is, let’s learn how to actually use it and get started writing some code. 

### Understanding The Working Directory and Environments
When we open up a `.R` file in RStudio to work on a project, we need to tell our computer where our data files and scripts live. By setting our *working directory* we tell R which folder to look in when we interact with a file. If we don’t set our working directory, R won’t know where to find our files, and we might receive an error message. Thus, setting a working directory is an important part of keeping our project organized. 

**Important Note**: To run a specific block of code in R, highlight the lines you’d like to run and then press Ctrl + Enter (Windows/Linux) or Cmd + Enter (Mac)
```r
# Set working directory to a given folder
setwd("~/Documents/R_Projects")

# Check current working directory
getwd()  
```

When you run your R code, your computer will temporarily store all of your datasets, variables, and other objects in memory. Below are a few helpful functions for managing your R environment.

```r
# List active objects in environment
ls()

# Clear everything from environment
rm(list = ls())
```
### Installing and Loading Packages
One of R’s strengths is the plethora of *packages* available for download. Packages are collections of objects (e.g. functions) that expand the core functionality of R. For example, the `ggplot2` package enables the creation of complex, layered graphics.

You only need to install a package once, however you need to load it every time you start a new R session. 
```r
# Install ggplot2
install.packages(“ggplot2”)

# Load the package when you start R
library(ggplot2)
```
**Note**: You can access *documentation* about an R package or R functions using the `help()` function

```r
# Access the documentation for a package
help(package = “ggplot2”)
```

### Reading in Data
Data can be imported into R in a variety of formats. For tabular data, scientists will often load their data in R from a CSV file. The following example workflow (a) reads a .csv into R as a dataframe (this is how tabular data is handled in R), and (b) starts to explore the data.

**Tip**: Make sure your data is stored in your current working directory. 
```r
# Read in a CSV file located in your 'data' folder
my_data <- read.csv("data/sample_data.csv")

# View the first few rows
head(my_data)

# Get the dimensions of the dataframe
dim(my_data)

# Get a quick summary of the dataset
summary(my_data)
```

## Best Practices
**Document Everything**: Keep track of who wrote the code and its intended purpose by writing a 1-2 sentence 
description at the beginning of the file.
**Keep Code Clean**: Load all packages at the top of your script, define key variables early, keep consistent naming conventions, add clear comments
**Make Code Modular**: Avoid repetition by using interaction and defining functions when possible. 




# Scientific Coding in R
This document introduces the basics of **scientific coding in R**. It includes key information on:
1. Installing the necessary software.
2. Learning foundational concepts and workflow. 
3. Developing good coding practices. 


## Why Use R for Scientific Programming?
**Statistical Power:** R is a language that is commonly used for statistical analysis and data visualization. It was designed by statisticians and excels in heavy-duty data analysis!
 **Community:** There is a vast open-source community of R users that consists of developers and domain experts in a wide variety of scientific fields. This community develops and supports R packages for almost any scientific application you can think of!


## Software
- **R**: Download the latest version from [CRAN](https://cran.r-project.org/).  
- **RStudio (Posit)**: Download the integrated development environment (IDE) from [Posit](https://posit.co/downloads/).

RStudio is a user-friendly interface where you can:
- Create and manage projects  
- Write R scripts `.R` and R Markdown reports `.Rmd`  
- View plots, manage your environment, manage libraries, and explore files 


## Learning Resources
[Datacamp](https://www.datacamp.com/users/sign_in) provides free interactive courses to get started with coding in R. 

Online forums such as [R for Ecology](https://www.rforecology.com/) and [geeksforgeeks.org](https://www.geeksforgeeks.org/) are public resources to learn how to use advanced functions and understand complicated syntax.

LLMs such as [https://cursor.com/](Cursor) can be powerful tools to help write complicated programs. However, these tools should only be leveraged once users have developed proficiency in R and can understand the syntax and functionality of code that has been written with AI. 

Online courses are offered at DataCamp, Coursera, and LinkedIn Learning on various subjects for all skill levels.
**DataCamp** - https://www.datacamp.com/
**Coursera** - https://www.coursera.org/
**LinkedIn Learning** - https://www.linkedin.com/learning/

## Core File Types
R Scripts (`.R`): R Scripts are one of the major files you will develop in R. Scripts are text files that include lines of R code. 
R Markdown (`.Rmd`): R markdown files are documents that include text, code, and results (visualizations, output, etc.) in one file. You might use an R Markdown file to publish or share the results of your analyses!
The R Console: When you open up R or R Studio, you will be met with a **console** where you can type commands and view the output of your R scripts. A basic Workflow in R may proceed as follow:
Writing code in a `.R` file
Running code line-by-line or in code blocks
Viewing the results of your code in the R console.

### Table 1. File Types 
| File Type | Description | Typical Use |
|------------|--------------|--------------|
| `.R` | Plain R script containing lines of code | Writing and running analysis pipelines |
| `.Rmd` | R Markdown file combining code, text, and results | Creating reproducible reports |
| Console | Interactive prompt for running commands | Testing functions or small snippets |

## Getting Started
Now that we know a bit more about what R is, let’s learn how to actually use it and get started writing some code. 

### Understanding The Working Directory and Environments
When we open up a `.R` file in RStudio to work on a project, we need to tell our computer where our data files and scripts live. By setting our *working directory* we tell R which folder to look in when we interact with a file. If we don’t set our working directory, R won’t know where to find our files, and we might receive an error message. Thus, setting a working directory is an important part of keeping our project organized. 

**Important Note**: To run a specific block of code in R, highlight the lines you’d like to run and then press Ctrl + Enter (Windows/Linux) or Cmd + Enter (Mac)
```r
# Set working directory to a given folder
setwd("~/Documents/R_Projects")

# Check current working directory
getwd()  
```

When you run your R code, your computer will temporarily store all of your datasets, variables, and other objects in memory. Below are a few helpful functions for managing your R environment.

```r
# List active objects in environment
ls()

# Clear everything from environment
rm(list = ls())
```
### Installing and Loading Packages
One of R’s strengths is the plethora of *packages* available for download. Packages are collections of objects (e.g. functions) that expand the core functionality of R. For example, the `ggplot2` package enables the creation of complex, layered graphics.

You only need to install a package once, however you need to load it every time you start a new R session. 
```r
# Install ggplot2
install.packages(“ggplot2”)

# Load the package when you start R
library(ggplot2)
```
**Note**: You can access *documentation* about an R package or R functions using the `help()` function

```r
# Access the documentation for a package
help(package = “ggplot2”)
```

### Reading in Data
Data can be imported into R in a variety of formats. For tabular data, scientists will often load their data in R from a CSV file. The following example workflow (a) reads a .csv into R as a dataframe (this is how tabular data is handled in R), and (b) starts to explore the data.

**Tip**: Make sure your data is stored in your current working directory. 
```r
# Read in a CSV file located in your 'data' folder
my_data <- read.csv("data/sample_data.csv")

# View the first few rows
head(my_data)

# Get the dimensions of the dataframe
dim(my_data)

# Get a quick summary of the dataset
summary(my_data)
```

## Best Practices
**Document Everything**: Keep track of who wrote the code and its intended purpose by writing a 1-2 sentence 
description at the beginning of the file.
**Keep Code Clean**: Load all packages at the top of your script, define key variables early, keep consistent naming conventions, add clear comments
**Make Code Modular**: Avoid repetition by using interaction and defining functions when possible. 
