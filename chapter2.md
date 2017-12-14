---
title       : Physics Application
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:3 key:5ef0ed3dfd
## Gravitational Force


*** =instructions
Jack is now standing at an altitude anywhere on Earth, where gravitational force is not 9.81 m/s^2. Please use the function called gForce that takes an integer called "height" in its parameter. Then, use the equation (G * m * M) / height^2 to return the value of g.

G = 6.674 * 10^-11

m = 8

M = 5.972 * 10^24

g = (G * m * M) / height^2

Additionally, if we want to print out the value of g,
we have to call the function "gForce" in a print statement.
However, the variable type of g doesn't seem to fit into the print statement.

Please change the variable type of the result of gForce in the print statement.

*** =hint
- Power can be calculated with x1**x2 or math.pow(x1, x2).

For example, 2**3 and math.pow(2, 3) both equal to 8.

- To change a variable type into a string type, put the variable inside str().

For example, to change x = 6 into a string, type str(x).

*** =pre_exercise_code
```{python}
import math
```

*** =sample_code
```{python}
# No import is required

# gForce has been defined for you, now fill in the following.
def gForce(___):
    G = ___
    m = 8
    M = ___
    g = ___
    return g
    
# Fill in the underlined area so the variable type of gForce() fits into the print statement.
print (___(gForce(10000000)))
```

*** =solution
```{python}
# No import is required

# gForce has been defined for you, now fill in the following.
def gForce(height):
    G = 6.674 * math.pow(10, -11)
    m = 8
    M = 5.972 * math.pow(10, 24)
    g = (G * m * M) / math.pow(height, 2)
    return g
    
print(str(gForce(10000000)))
```

*** =sct
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

test_output_contains(str('31.8857024'),
                    pattern = True,
                    no_output_msg = "The answer is not right! Check your calculations again!")
                    
success_msg("Great Work!")
```


--- type:NormalExercise lang:python xp:100 skills:2 key:c6434d6e6b
## Pendulum Time Period


*** =instructions
While at the same location, Jack happens to have a pendulum in his pocket, so he wants to measure the time needed for the pendulum to complete 1 period. Please create a function called "timePeriod" that takes in 2 parameters: an integer length and an integer height.
Then, use the equation T = 2π * √(length / g)  to return the value of T in timePeriod.

T = 2π * √(length / g)

√ = square root

Must use python MATH FUNCTIONS!

*** =hint
Call the gForce function to find the value of g.

Use math.pi for π.

Use math.sqrt(x) for square root.

*** =pre_exercise_code
```{python}
import math
```

*** =sample_code
```{python}
# gForce is given for you to solve this problem
def gForce(height):
    G = 6.674 * math.pow(10, -11)
    m = 8
    M = 5.972 * math.pow(10, 24)
    g = (G * m * M) / math.pow(height, 2)
    return g
    
# Create the function timePeriod here


# Function call - no need to change this
print(str(timePeriod(0.5, 10000000)))
```

*** =solution
```{python}
def gForce(height):
    G = 6.674 * math.pow(10, -11)
    m = 8
    M = 5.972 * math.pow(10, 24)
    g = (G * m * M) / math.pow(height, 2)
    return g

def timePeriod(length, height):
    T = 2 * math.pi * math.sqrt(length/gForce(height))
    return T
    
print(str(timePeriod(0.5, 10000000)))
```

*** =sct
```{python}
Ex().check_function_def('timePeriod').multi(
        check_args('length').missing_msg = "Invalid parameter(s) in timePeriod.",
        check_args('height').missing_msg = "Invalid parameter(s) in timePeriod."))
        
test_student_typed("math.pi", pattern = False, not_typed_msg = "An important math function is missing.")
test_student_typed("math.sqrt", pattern = False, not_typed_msg = "An important math function is missing.")
success_msg("Great Work!")
```
