
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
12. [Markers](#markers)
13. [Marker Colors](#marker-colors)
14. [Grey Scale Image](#grey-scale-image)

_

1. Introduction to Matplotlib

Matplotlib is a widely used Python library for creating static, animated, and interactive visualizations in various formats, including charts, plots, graphs, and more. It provides an intuitive and flexible API for crafting data-driven visualizations and is often used in scientific computing, data analysis, and data science.

 2. Installation
```bash

pip install matplotlib
import matplotlib.pyplot as plt
import numpy as np
# Sample data
x = np.linspace(0, 10, 100)
y = np.sin(x)


#3. Create a basic line plot

plt.plot(x, y)
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.linspace(0, 10, 100)
y = np.sin(x)


4. Customize the plot
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


5. Create multiple plots
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


6. Create a bar chart
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


7. Create a scatter plot
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


8. Create a histogram
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


9. Create a pie chart
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


10. Create a 3D surface plot
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


11. Create a line plot
plt.plot(x, y)
plt.title('Save Plot as Image')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')

# Save the plot as an image (e.g., PNG)
plt.savefig('my_plot.png')

# Show the plot
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Sample data
x = np.linspace(0, 2 * np.pi, 50)
y = np.sin(x)


12. XY plot with different marker styles
plt.figure(figsize=(10, 5))

# Circle markers
plt.plot(x, y, marker='o', label='Circle Marker', linestyle='-', markersize=6)

# Square markers
plt.plot(x, y + 0.2, marker='s', label='Square Marker', linestyle='-', markersize=6)

# Diamond markers
plt.plot(x, y + 0.4, marker='D', label='Diamond Marker', linestyle='-', markersize=6)

# Triangle markers
plt.plot(x, y + 0.6, marker='^', label='Triangle Marker', linestyle='-', markersize=6)

# Cross markers
plt.plot(x, y + 0.8, marker='x', label='Cross Marker', linestyle='-', markersize=6)

# Plus markers
plt.plot(x, y + 1.0, marker='+', label='Plus Marker', linestyle='-', markersize=6)

# Customize the plot
plt.title('XY Plot with Different Markers')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.grid(True)
plt.legend()

# Display the plot
plt.show()
# Matplotlib Marker Color Letters Guide


13. Single-Letter Color Codes
Matplotlib provides a set of single-letter color codes that you can use to specify marker colors quickly. Here are some commonly used color codes:

- `'b'`: Blue
- `'g'`: Green
- `'r'`: Red
- `'c'`: Cyan
- `'m'`: Magenta
- `'y'`: Yellow
- `'k'`: Black
- `'w'`: White

## Using Marker Color Letters

You can use these single-letter color codes when creating scatter plots or line plots with markers in Matplotlib. To set the marker color, combine the color code with the `color` parameter.

### Example - Scatter Plot with Marker Color

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [10, 5, 20, 15, 30]

# Create a scatter plot with red markers
plt.scatter(x, y, marker='o', color='r', label='Red Markers')

# Customize the plot
plt.title('Scatter Plot with Red Markers')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.legend()
plt.grid(True)

# Show the plot
plt.show()
# Generating and Displaying a Random Grayscale Image in Matplotlib


14. Generating a Random Grayscale Image
To create a random grayscale image, we'll follow these steps:

1. Import the required libraries.
2. Generate random pixel values between 0 and 255.
3. Arrange these values into a 2D NumPy array to represent the image.

```python
import matplotlib.pyplot as plt
import numpy as np

# Define the dimensions of the image
width, height = 256, 256

# Generate random grayscale values (0 to 255)
random_image = np.random.randint(0, 256, (height, width), dtype=np.uint8)

# Display the random grayscale image
plt.imshow(random_image, cmap='gray')
plt.title('Random Grayscale Image')
plt.axis('off')  # Turn off axis labels
plt.show()

