---
title       : Pizza Party
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:1 key:ccbaff9352
## Sum of Prices


*** =instructions
Angela wants to order a set of pizzas for a party. Each pizza has an original cost + cost of its toppings.
However, the receipt doesn't display the total price of all the pizzas + toppings, so you will have to help Angela
determine the total price she has to pay.

- For maximum efficiency, Angela wants you to only use "for loops".

*** =hint
To cover all the elements in pizzaList,
you need a nested loop, which can be created by using
a for loop inside a for loop.

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
# The following is the original cost + topping costs for each pizza
pizzaList = [[5.35, 2.43, 1.65],
             [6.56, 1.23, 3.21, 0.23, 0.75],
             [7.92, 1.74, 3.25],
             [6.59, 2.17, 3.82, 2.53]]

# Add the total amount to sum
sum = 0
             
# Insert solution here

        
# Display the sum
print(sum)
```

*** =solution
```{python}
# The following is the original cost + topping cost for each pizza
pizzaList = [[5.35, 2.43, 1.65],
             [6.56, 1.23, 3.21, 0.23, 0.75],
             [7.92, 1.74, 3.25],
             [6.59, 2.17, 3.82, 2.53]]

# Add the total amount to sum 
sum = 0

# Insert solution here 
for x in pizzaList:
    for y in x:
        sum += y
        
# Display the sum
print(sum)
```

*** =sct
```{python}
test_student_typed("in pizzaList", pattern = False, not_typed_msg = "Make sure you are using loops correctly.")
test_output_contains(str('49.43'),
                    pattern = True,
                    no_output_msg = "Incorrect! Make sure your loops have covered each element.")
success_msg("Great Work!")
```


--- type:NormalExercise lang:python xp:100 skills:2 key:f2ac4e01c6
## <<<New Exercise>>>


*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}

```

*** =solution
```{python}

```

*** =sct
```{python}

```
