https://people.math.harvard.edu/~knill/mathmovies/

https://people.math.harvard.edu/~knill/mathmovies/

https://4dtoys.com/

https://www.math.uwaterloo.ca/~rblander/cops/

https://www.math.uwaterloo.ca/~hwolkowi/

musical time machine


https://radiooooo.app/


https://www.matrixcalculus.org/


How to differentiate a matrix of functions
Python Help
Jul 2022
Jul 2022

gary bollenbach
whiffee
Jul 2022
I want a simple elementwise derivative of a matrix. Could not find anything precoded, which was surprising. I tried a few versions, the following is probably the simplest.

import numpy as np
from sympy import *
import sympy as sp

t = symbols(‘t’)

a = np.array([[t**2 + 1, sp.exp(2*t)], [sin(t), 45]])

for row in a:
for element in row:
a[row][element] = diff(a[row][element],t)

print(a)

and the error section that shows in Jupyter:
IndexError Traceback (most recent call last)
Input In [25], in <cell line: 9>()
9 for row in a:
10 for element in row:
—> 11 a[row][element] = diff(a[row][element],t)
13 print(a)

IndexError: arrays used as indices must be of integer (or boolean) type
