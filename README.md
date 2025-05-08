import math

def f(x):
    return x + math.log(x) - 0.5

a = 0.1   
b = 1.0
n = 100   
h = (b - a) / n

for i in range(n):
    x0 = a + i * h
    x1 = x0 + h
    if f(x0) * f(x1) < 0:
        print(f"Kök [{x0:.4f}, {x1:.4f}] intervalındadır")
