Welcome to the Matplotlib Learning Guide! This README file serves as a starting point for your journey to learn Matplotlib, a powerful Python library for creating data visualizations. Whether you are new to Matplotlib or looking to expand your knowledge, this guide will help you get started and master the essentials.

## Table of Contents

1. [Introduction to Matplotlib](#introduction-to-matplotlib)
2. [Installation](#installation)
3. [Basic Line Plot](#basic-line-plot)
4. [Customizing Plots](#customizing-plots)
5. [Multiple Plots](#multiple-plots)
6. [Bar Charts](#bar-charts)
7. [Scatter Plots](#scatter-plots)
8. [Histograms](#histograms)
9. [Pie Charts](#pie-charts)
10. [3D Plots](#3d-plots)
11. [Saving and Exporting](#saving-and-exporting)

## 1. Introduction to Matplotlib

Matplotlib is a widely used Python library for creating static, animated, and interactive visualizations in various formats, including charts, plots, graphs, and more. It provides an intuitive and flexible API for crafting data-driven visualizations and is often used in scientific computing, data analysis, and data science.

## 2. Installation

Before you begin, make sure you have Matplotlib installed. You can install it using pip:

```bash
pip install matplotlib
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Create a basic line plot
plt.plot(x, y)
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Customize the plot
plt.plot(x, y, label='Sine Wave', color='b', linestyle='--')
plt.title('Customized Sine Wave')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.legend()
plt.grid(True)
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

# Create multiple plots
plt.subplot(2, 1, 1)  # Two rows, one column, first plot
plt.plot(x, y1, label='Sine Wave', color='b')
plt.legend()

plt.subplot(2, 1, 2)  # Two rows, one column, second plot
plt.plot(x, y2, label='Cosine Wave', color='r')
plt.legend()

plt.show()
import matplotlib.pyplot as plt

# Sample data
categories = ['Category A', 'Category B', 'Category C']
values = [10, 15, 7]

# Create a bar chart
plt.bar(categories, values, color='c')
plt.title('Bar Chart Example')
plt.xlabel('Categories')
plt.ylabel('Values')
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.random.rand(50)
y = np.random.rand(50)

# Create a scatter plot
plt.scatter(x, y, color='g', marker='o', label='Random Data')
plt.title('Scatter Plot Example')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.legend()
plt.grid(True)
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
data = np.random.randn(1000)  # Generate random data

# Create a histogram
plt.hist(data, bins=20, color='m', alpha=0.7)
plt.title('Histogram Example')
plt.xlabel('Values')
plt.ylabel('Frequency')
plt.grid(True)
plt.show()
import matplotlib.pyplot as plt

# Sample data
labels = ['Category A', 'Category B', 'Category C']
sizes = [40, 30, 20]

# Create a pie chart
plt.pie(sizes, labels=labels, autopct='%1.1f%%', colors=['gold', 'lightcoral', 'lightskyblue'])
plt.title('Pie Chart Example')
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.linspace(-5, 5, 50)
y = np.linspace(-5, 5, 50)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

# Create a 3D surface plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_surface(X, Y, Z, cmap='viridis')

plt.title('3D Surface Plot')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Create a line plot
plt.plot(x, y)
plt.title('Save Plot as Image')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')

# Save the plot as an image (e.g., PNG)
plt.savefig('my_plot.png')

# Show the plot
plt.show()
