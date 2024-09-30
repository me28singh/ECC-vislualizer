# Elliptic Curve Cryptography Visualization 

This project provides a Python-based implementation of basic operations in Elliptic Curve Cryptography (ECC), along with a graphing tool to visualize elliptic curves over finite fields. The project is designed to demonstrate core cryptographic operations like point addition, doubling, and modular arithmetic, and includes a grapher to plot these elliptic curves.

# Features
ECC Operations: Point addition, point doubling, and modular arithmetic.
Point Multiplication: Efficient point multiplication using binary sequences.
Elliptic Curve Plotting: Visualizes elliptic curves over finite fields using matplotlib.
Modular Arithmetic: Includes utilities for modular inverse and square root calculations.

# Installation
To get started with this project, ensure you have Python installed, then clone the repository:
git clone https://github.com/me28singh/ECC-vislualizer.git
cd ecc-visualization

Next, install the required dependencies:
pip install matplotlib

Usage
Running the ECC Operations
To use the ECC operations for cryptographic computations:
from ecc_visualization import ECC, Point

# Define the curve parameters a, b, p (where p is a prime number)
ecc = ECC(a=2, b=3, p=17)

# Find all points on the curve
points = ecc.findAllPoints()
print("Points on the curve:", points)

# Perform point addition
point1 = points[0]
point2 = points[1]
result = ecc.Add(point1, point2)
print("Point addition result:", result)
Visualizing Elliptic Curves
To plot an elliptic curve over a finite field:
from ecc_visualization import Grapher

# Initialize the Grapher
g = Grapher()

# Define the curve parameters a, b, p
a, b, p = 2, 3, 17

# Plot the elliptic curve y² = x³ + ax + b (mod p)
g.plotCurve(a, b, p)
Example Input:
To run a test case, pass the curve parameters a, b, and p as input:
2 3 17
This will plot the elliptic curve defined by the equation:
y² ≡ x³ + 2x + 3 (mod 17)

# How It Works
Elliptic Curve Equation
An elliptic curve is represented by the equation:
y² = x³ + ax + b (mod p)
Where a, b define the curve parameters, and p is a prime number for the finite field.

# ECC Operations
The core operations implemented are:

Point Addition: Adds two points on the elliptic curve.
Point Doubling: Doubles a point on the curve.
Point Multiplication: Uses binary sequences for fast point multiplication.
Modular Arithmetic: Handles modular inverse and modular square root calculations.
Fermat’s Little Theorem
This project uses Fermat’s Little Theorem to compute modular inverses, a key part of the cryptographic operations.

# Contributions
Contributions are welcome! If you'd like to contribute to this project, please submit a pull request or open an issue to discuss your changes.
