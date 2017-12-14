---
title       : Physics Application
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:2 key:5ef0ed3dfd
## Gravitational Force


*** =instructions
Jack is now standing at an altitude anywhere on Earth, where gravitational force is not 9.81 m/s^2. Please create a function called Force that takes an integer, height, in its parameter. Then, use the equation (G * m * M) / height^2 to return the value of g.

G = 6.674 * 10^-11

m = 8

M = 5.972 * 10^24

g = (G * m * M) / height^2

*** =hint
Power can be calculated with x1**x2 or math.pow(x1, x2).

For example, 2**3 and math.pow(2, 3) both equal to 8.

*** =pre_exercise_code
```{python}
import math
```

*** =sample_code
```{python}
import math
def gForce(___):
    G = ___
    m = 8
    M = ___
    g = ___
    return g
```

*** =solution
```{python}
import math
def gForce(height):
    G = 6.674 * math.pow(10, -11)
    m = 8
    M = 5.972 * math.pow(10, 24)
    g = (G * m * M) / math.pow(height, 2)
    return g
```

*** =sct
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
#test_object("G", eq_condition="equal", do_eval=True, undefined_msg="Your string1 has not been defined", incorrect_msg="Your string1 is not initialized properly")
```


--- type:NormalExercise lang:python xp:100 skills:2 key:c6434d6e6b
## Pendulum Time Period


*** =instructions
While at the same location, Jack happens to have a pendulum in his pocket, so he wants to measure the time needed for the pendulum to complete 1 period. Please create a function called time that takes in 2 parameters: an integer length and an integer height.
Then, use the equation T = 2π * √(length / g)  to return the value of T in time.

T = 2 * (length / g)

 = square root

Must use python MATH FUNCTIONS!

*** =hint
Call the Force function to find the value of g.

Use math.pi for π.

Use math.sqrt(x) for(length / g)

*** =pre_exercise_code
```{python}
import math
```

*** =sample_code
```{python}
import math
def gForce(height):
    G = 6.674 * math.pow(10, -11)
    m = 8
    M = 5.972 * math.pow(10, 24)
    g = (G * m * M) / math.pow(height, 2)
    return g
    
# Create the function timePeriod here

```

*** =solution
```{python}
import math
def gForce(height):
    G = 6.674 * math.pow(10, -11)
    m = 8
    M = 5.972 * math.pow(10, 24)
    g = (G * m * M) / math.pow(height, 2)
    return g

def timePeriod(length, height):
    T = 2 * math.pi * math.sqrt(length/gForce(height))
    return T
```

*** =sct
```{python}
#test_function("timePeriod")
#test_student_typed("math.pi", pattern = False, not_typed_msg = "An important math function is missing.")
#test_student_typed("math.sqrt", pattern = False, not_typed_msg = "An important math function is missing.")
success_msg("Great Work!")
```
