## PHYS1002 - Computational Lab 1: Exercise 10 Solutions


import math
import numpy as np


# Step 1:  Define the value of any constants used in solving this problem.  In this case g=9.8 m/s
g = 9.8

# Step 2: User inputs initial height h, and time of flight t
h = float(input("Enter the height of the ball above the ground (m): "))
b = 0.3
m = 1 #kg

x = 0; t = 0; v = 0 # initialise displacement, time and velocity at 0
dt = 0.001
while x < h:
    a = g - b/m*v
    v += a*dt
    x += v*dt
    
    t += dt
    
print(f'Time taken: {t:.2f} seconds')
print(f'Velocity of ball at ground: {v:.2f} m/s')
