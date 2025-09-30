import math

def f(x):
    return math.sin(x) + math.cos(x)

x = math.pi / 6   # x = π/6
h = 0.01

# central difference formula
f_prime = (f(x + h) - f(x - h)) / (2 * h)

print("Approximate derivative at x=π/6:", f_prime)

# exact derivative
exact = math.cos(x) - math.sin(x)
print("Exact derivative:", exact)
print("Error:", abs(f_prime - exact))
