
## NumPy Functions

### np.zeros

The `np.zeros` function is used to create an array filled with zeros. It takes the shape of the desired array as an argument and returns a NumPy array with all elements initialized to 0.

Example:

import numpy as np

#Create a 2x3 array filled with zeros
zeros_array = np.zeros((2, 3))
print(zeros_array)
import numpy as np

# Create a 3x2 array filled with ones
ones_array = np.ones((3, 2))
print(ones_array)
import numpy as np

# Create a 4x4 identity matrix
identity_matrix = np.eye(4)
print(identity_matrix)
import matplotlib.pyplot as plt
import numpy as np

# Create a simple 2D array as an example image
image_data = np.random.rand(5, 5)

# Display the image using plt.imshow
plt.imshow(image_data, cmap='viridis')
plt.colorbar()
plt.show()
import matplotlib.pyplot as plt
import numpy as np

# Generate some sample data
x = np.linspace(0, 2 * np.pi, 100)
y = np.sin(x)

# Create a line plot
plt.plot(x, y, label='sin(x)')
plt.xlabel('x')
plt.ylabel('y')
plt.title('Sine Wave')
plt.legend()
plt.grid(True)
plt.show()
import numpy as np

# Create an array of 10 evenly spaced values between 0 and 1
linspace_array = np.linspace(0, 1, 10)
print(linspace_array)
import numpy as np

# Create a one-dimensional array
arr = np.array([0, 1, 2, 3, 4])

# Accessing elements
element_at_index_2 = arr[2]  # Indexing starts at 0, so this is the third element.
import numpy as np

# Create a two-dimensional array (3x3 matrix)
matrix = np.array([[1, 2, 3],
                   [4, 5, 6],
                   [7, 8, 9]])

# Accessing elements
element_at_row_1_col_2 = matrix[0, 1]  # Accesses the element in the first row, second column (index 0, 1).
import numpy as np

# Create a one-dimensional array
arr = np.array([0, 1, 2, 3, 4, 5])

# Slicing
subarray = arr[1:4]  # Gets elements at indices 1, 2, and 3 (up to, but not including 4).
import numpy as np

# Create an array
arr = np.array([10, 20, 30, 40, 50])

# Fancy Using an array of indices to access elements
indices = np.array([1, 3])
selected_elements = arr[indices]  # Retrieves elements at indices 1 and 3.
import numpy as np

# Create an array
arr = np.array([10, 20, 30, 40, 50])

# Boolean indexing to select elements greater than 30
condition = arr > 30
selected_elements = arr[condition]  # Retrieves elements where the condition is True.

# Plotting a Linear Equation: y = mx + b

import matplotlib.pyplot as plt
import numpy as np

# Define the parameters of the linear equation
m = 2  # Slope
b = 1  # Intercept

# Generate x values
x = np.linspace(-5, 5, 100)

# Calculate y values using the equation
y = m * x + b

# Create the line plot
plt.plot(x, y, label=f'y = {m}x + {b}', color='b')

# Add labels and title
plt.xlabel('x')
plt.ylabel('y')
plt.title('Linear Equation: y = mx + b')
plt.grid(True)

# Add a legend
plt.legend()

# Display the plot
plt.show()

'''
