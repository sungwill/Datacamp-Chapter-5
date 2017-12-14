---
title       : Pizza Party
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:1 key:ccbaff9352
## Sum of Prices


*** =instructions
Angela wants to order a set of pizzas for a party. Each pizza has an original cost + cost of its toppings.
However, the receipt doesn't display the total price of all the pizzas + toppings, so you will have to help Angela
determine the total price she has to pay.

- Add all the prices in pizzaList into sum using loop(s).
- For maximum efficiency, Angela wants you to only use "for loop".

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


--- type:NormalExercise lang:python xp:100 skills:4 key:f2ac4e01c6
## More Fun with Pizza List


*** =instructions
Angela's brother agreed to pay the most expensive items for each pizza, so she can
reduce her cost.

Additionally, Angela wants you to add the pizza names to their prices

- Remove the most expensive price from each list in pizzaList.
- Add each element in pizzaNames to the 1st index of each list in pizzaList.

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
# Both pizzaList and pizzaNames are given for you to solve this problem
pizzaList = [[5.35, 2.43, 1.65],
             [6.56, 1.23, 3.21, 0.23, 0.75],
             [7.92, 1.74, 3.25],
             [6.59, 2.17, 3.82, 2.53]]
             
pizzaNames = ['Hawaii', 'Tomato', 'Margarita', 'Hybrid']

# Enter your solution here


# Prints out the final list of pizzaList
print(pizzaList)
```

*** =solution
```{python}
pizzaList = [[5.35, 2.43, 1.65],
             [6.56, 1.23, 3.21, 0.23, 0.75],
             [7.92, 1.74, 3.25],
             [6.59, 2.17, 3.82, 2.53]]
             
pizzaNames = ['Hawaii', 'Tomato', 'Margarita', 'Hybrid']

for x in pizzaList:
    x.remove(max(x))
    x.insert(0, pizzaNames[pizzaList.index(x)])


print(pizzaList)
```

*** =sct
```{python}
test_student_typed(".remove", pattern = False, not_typed_msg = "Make sure you are using loops correctly.")
test_student_typed("max(", pattern = False, not_typed_msg = "Make sure you are using loops correctly.")
test_student_typed(".insert", pattern = False, not_typed_msg = "Make sure you are using loops correctly.")
test_output_contains(str("[['Hawaii', 2.43, 1.65], ['Tomato', 1.23, 3.21, 0.23, 0.75], ['Margarita', 1.74, 3.25], ['Hybrid', 2.17, 3.82, 2.53]]"),
                    pattern = True,
                    no_output_msg = "Incorrect! Make sure your loops have covered each element.")
success_msg("Great Work!")
```
