# Creating Plots in Python

This guide provides a general overview of how to create and display plots in Python for data visualization.

---

## 1. Install a Plotting Library

The most common library for plotting in Python is **Matplotlib**. You can install it using:

```bash
pip install matplotlib
```

Other options include:

* **Seaborn** (for statistical plots)
* **Plotly** (for interactive plots)
* **Pandas plotting** (built on top of Matplotlib)

---

## 2. Import Libraries

You can import the main plotting module like this:

```python
import matplotlib.pyplot as plt
```

If you need to generate numerical data, you can also import NumPy:

```python
import numpy as np
```

---

## 3. Prepare Data

Data can come from many sources — a file, a database, or code-generated arrays.
Example using simple data:

```python
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
```

Or generate evenly spaced numbers:

```python
x = np.linspace(0, 10, 50)
y = x ** 2
```

---

## 4. Create a Plot

A simple line plot can be made using:

```python
plt.plot(x, y)
plt.show()
```

This displays a basic graph of `y` versus `x`.

---

## 5. Add Titles and Labels

You can make your plot clearer by labeling the axes and adding a title:

```python
plt.plot(x, y)
plt.title("Example Plot")
plt.xlabel("X values")
plt.ylabel("Y values")
plt.show()
```

---

## 6. Customize Appearance

You can change line styles, colors, and markers:

```python
plt.plot(x, y, color='green', linestyle='--', marker='o')
```

Common options:

* `color`: `'red'`, `'blue'`, `'green'`, or hex values like `'#123456'`
* `linestyle`: `'-'`, `'--'`, `':'`, or `'-.`
* `marker`: `'o'`, `'s'`, `'^'`, etc.

---

## 7. Multiple Datasets

You can plot multiple lines on the same figure:

```python
y2 = [val * 1.5 for val in y]
plt.plot(x, y, label="Original")
plt.plot(x, y2, label="Scaled")
plt.legend()
plt.show()
```

---

## 8. Other Plot Types

Matplotlib supports many kinds of plots:

```python
plt.scatter(x, y)     # Scatter plot
plt.bar(x, y)         # Bar chart
plt.hist(y)           # Histogram
plt.boxplot(y)        # Box plot
plt.pie(y)            # Pie chart
```

---

## 9. Save a Plot

You can export your plot as an image file:

```python
plt.savefig("my_plot.png", dpi=300)
```

Supported formats include `.png`, `.jpg`, `.pdf`, and `.svg`.

---

## 10. General Workflow

1. Import plotting library
2. Load or create data
3. Choose the plot type
4. Customize labels and styles
5. Display or save the plot

---

## Example

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)
y = np.exp(x)

plt.plot(x, y, color='blue')
plt.title("Exponential Growth")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.grid(True)
plt.show()
```

---

## Summary

Creating plots in Python follows a simple pattern:

* Import a plotting library
* Prepare your data
* Call a plotting function
* Customize as needed
* Display or save the figure

This general approach applies whether you use Matplotlib, Seaborn, Plotly, or another visualization tool.


# Insert Writeup Here
# Google Doc Link: https://docs.google.com/document/d/1WgP2UnqisQ-X36laP5-93Ptow1lTxA5wsAUWuQyJetc/edit?usp=sharing