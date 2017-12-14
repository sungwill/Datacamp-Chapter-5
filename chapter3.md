---
title       : Movie Tickets
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:1 key:ccbaff9352
## Movie Tickets


*** =instructions
Angela wants to order a set of pizzas for a party. Each pizza has an original cost + cost of its toppings.
However, the receipt doesn't display the total price of all the pizzas + toppings, so you will have to help Joe
determine the price he has to pay.



*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
# The following is the original cost + topping cost for each pizza
pizzaList = [[5.35, 2.43, 1.65],
             [6.56, 1.23, 3.21, 0.23, 0.75],
             [7.92, 1.74, 3.25],
             [6.59, 2.17, 3.82, 2.53]]
             
sum = 0
             
# Insert solution here
for x in pizzaList:
    sum += x
        
# Display the sum
print(sum)
```

*** =solution
```{python}
pizzaList = [[5.35, 2.43, 1.65],
             [6.56, 1.23, 3.21, 0.23, 0.75],
             [7.92, 1.74, 3.25],
             [6.59, 2.17, 3.82, 2.53]]
             
sum = 0
             
for x in pizzaList:
    sum += x
    #for y in x:
     #   sum += y
        
print(sum)
```

*** =sct
```{python}

```
