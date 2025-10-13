# Exploratory Data Analysis

Exploratory data analysis (EDA) is a way to acquaint yourself with the data you're using. What you produce in EDA are not results, but they are good to include your tables or plots in every paper or project you do. It's a good way to "start the story" of your data.
Some tips:
- Always do exploratory data analysis
- Show your advisor your exploratory work
- Read the metadata
- If you're using geospatial data: make maps
- If you're studying timeseries: make timeseries
- If you're using counts: make histograms
  
The primary languages for exploratory data analysis are Python and R.


## In R
### Looking at the Data

`str()` : this command shows the overall structure of the data, including variable names, data types and the first few values

### Finding gaps or unusual numbers within data
`is.na(df)` : this function returns a logical matrix indicating which elements are missing (TRUE) and elements that aren’t missing (FALSE)
`sum(is.na(df))` : this function counts the number of missing values in a data frame (df)
### Counting missing values in each column (2 options)
`sapply()`
`colSums(is.na(df))` 

## In Python


## Summarizing and Visualizing Data

The `summary()` function will provide counts of categorical data and summary statistics (mean, median, minimum, maximum, and quartile values) for numerical data. 

```r
summary(penguins)
```
<img width="1099" height="325" alt="image" src="https://github.com/user-attachments/assets/b05ab199-ad92-445a-a737-11e54e31047b" />

### Exploratory plots can be helpful to understand general trends in the data and provide a starting point for data analysis.

Using `plot()` will produce a scatterplot of two variables in the dataset. Scatterplots allow for visualization of the trends in the data and the relationship between the parameters (linear, hyperbolic, etc). This function can also help identify outliers in the dataset.

```r
plot(bill_length_mm ~ body_mass_g, data=penguins)
```
<img width="780" height="675" alt="image" src="https://github.com/user-attachments/assets/6ae70df3-5b2b-4b12-8799-6ec03a366ad9" />

From this exploratory plot, one can see a generally linear trend between penguin body mass and bill length. 

The command `hist()` will produce a histogram of the data, which allows one to observe the distribution of the data. Observing the distribution is useful to determine the symmetry and modality of the data. Data that is multimodal and heavily skewed may not fit the assumptions necessary for some statistical analyses. 

```r
hist(penguins$bill_length_mm)
```
<img width="780" height="675" alt="image" src="https://github.com/user-attachments/assets/d86e7105-62b1-43a5-82ab-355bc538a46a" />


This histogram shows a generally normal distribution of bill length sampled from the penguins. 

Creating a `boxplot()` allows for the visualization of the distributions of groups of variables. Similar to creating a histogram, this can be useful to understand effect sizes between groups and assess the symmetry of the data. Boxplots will also provide a visual summary of the median, maximum, minimum, and quartile values. 

```r
boxplot(bill_length_mm ~ sex, data-penguins)
```
<img width="780" height="675" alt="image" src="https://github.com/user-attachments/assets/e1d88c65-ff57-4502-a30b-c424d0525548" />

This exploratory boxplot shows that sex may have an effect on penguin mean bill length. 


Visualizing data allows one to see patterns that may be difficult to understand from raw data alone. 

