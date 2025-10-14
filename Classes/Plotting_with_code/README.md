# Plotting with Code

This document outlines how to create and visualize data using plots in both **Python** and **R Studio**. It covers basic plotting workflows, common plot types, and best practices for clear and effective data visualization.

---

## Why Plotting Data is Important

Plotting data helps readers visualize patterns, trends, and outliers that might be difficult to detect from raw data alone. Using different types of plots can also help illustrate relationships, correlations, and comparisons between variables.

---

## Software

### Python

Python is one of the most popular languages for data analysis and visualization. It supports multiple libraries such as **Matplotlib**, **Seaborn**, and **Plotly**.

Install Matplotlib with:

```bash
pip install matplotlib
```

### R Studio

R Studio can be downloaded and installed directly on your computer.
If you already have it, update to the latest version to ensure compatibility with packages like **ggplot2**.

> Close R Studio before updating to ensure a smooth installation process.

---

# Plotting in Python

This section provides a general overview of how to create and customize plots in Python using Matplotlib.

## 1. Import Libraries

```python
import matplotlib.pyplot as plt
import numpy as np
```

## 2. Prepare Data

```python
x = np.linspace(0, 10, 50)
y = x ** 2
```

## 3. Create a Plot

```python
plt.plot(x, y)
plt.show()
```

## 4. Add Titles and Labels

```python
plt.plot(x, y)
plt.title("Example Plot")
plt.xlabel("X values")
plt.ylabel("Y values")
plt.show()
```

## 5. Customize Appearance

```python
plt.plot(x, y, color='green', linestyle='--', marker='o')
```

Common options:

* `color`: `'red'`, `'blue'`, `'green'`, or hex codes like `'#123456'`
* `linestyle`: `'-'`, `'--'`, `':'`, `'-.`'
* `marker`: `'o'`, `'s'`, `'^'`

## 6. Multiple Datasets

```python
y2 = [val * 1.5 for val in y]
plt.plot(x, y, label="Original")
plt.plot(x, y2, label="Scaled")
plt.legend()
plt.show()
```

## 7. Other Plot Types

```python
plt.scatter(x, y)     # Scatter plot
plt.bar(x, y)         # Bar chart
plt.hist(y)           # Histogram
plt.boxplot(y)        # Box plot
plt.pie(y)            # Pie chart
```

## 8. Save a Plot

```python
plt.savefig("my_plot.png", dpi=300)
```

---

# Plotting in R Studio

## Different Types of Plots in R

R offers many visualization types, primarily using the **ggplot2** package.

| **Goal**                                     | **Best Plot**                   | **R Library Examples**                                                           |
| -------------------------------------------- | ------------------------------- | -------------------------------------------------------------------------------- |
| **Compare categories**                       | Bar chart, Grouped bar chart    | `ggplot2::geom_bar()`, `ggplot2::geom_col()`                                     |
| **Show trends over time**                    | Line chart, Area chart          | `ggplot2::geom_line()`, `ggplot2::geom_area()`                                   |
| **Show distribution of values**              | Histogram, Boxplot, Violin plot | `ggplot2::geom_histogram()`, `ggplot2::geom_boxplot()`, `ggplot2::geom_violin()` |
| **Show relationships between two variables** | Scatter plot, Regression line   | `ggplot2::geom_point()`, `ggplot2::geom_smooth(method = "lm")`                   |
| **Show proportions or parts of a whole**     | Stacked bar chart, Pie chart    | `ggplot2::geom_bar(position = "fill")`, `ggplot2::coord_polar()`                 |
| **Show correlations or multivariate data**   | Heatmap, Pair plot              | `ggplot2::geom_tile()`, `GGally::ggpairs()`                                      |
| **Show uncertainty or variation**            | Error bars, Boxplot             | `ggplot2::geom_errorbar()`, `ggplot2::geom_boxplot()`                            |

---

## Best Practices for Visualization

**1. Choose the right visualization for your goals.**

* Use plots that best match the type of data and story you want to tell.

**2. Use colors that are easy to read.**

* Maintain color consistency across plots.
* Use color palettes suitable for color-blind accessibility.

Install a color-blind friendly palette:

```R
install.packages("viridis")
library(viridis)
```

**3. Label your plots clearly.**

* Always include titles, axis labels, and units.
* Add legends if plotting multiple variables.

Example in R:

```R
library(ggplot2)
ggplot(mpg, aes(x = displ, y = hwy)) +
  geom_point(color = "darkorange") +
  labs(title = "Engine Size vs. Highway MPG",
       x = "Engine Displacement (liters)",
       y = "Highway Miles per Gallon")
```

**4. Use appropriate scales.**

* Make sure axis scales fit your data and do not distort trends.

**5. Keep plots simple and accessible.**

* Avoid excessive decorations.
* Use readable fonts and appropriate text sizes.

**6. Provide context.**

* Add annotations or reference lines to highlight key insights.

**7. Ensure reproducibility.**

* Keep code organized and consistent in style.

---

## Resources

* [ggplot2 documentation](https://ggplot2.tidyverse.org/)
* [R visualization recipes](https://posit.cloud/learn/recipes)
* [DataCamp tutorials](https://www.datacamp.com/)

---

# Summary

Data visualization is a key component of analysis in both Python and R.
The general process is:

1. Import a plotting library.
2. Prepare or load your data.
3. Choose an appropriate plot type.
4. Customize appearance and labels.
5. Display or save the plot.

Whether using **Matplotlib** in Python or **ggplot2** in R, clear and effective plots make data insights easier to interpret and communicate.
