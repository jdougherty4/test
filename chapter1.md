---
title: 'Introduction to R'
description: ""
---

## Intro to R Console

```yaml
type: NormalExercise
key: 82a96a0a9b
lang: r
xp: 100
skills: 1
```

All code that we write in these bootcamps are called scripts. Every time you execute code, it's run through the console. You can use the console located at the bottom to tell R what to do. You can perform math operations, save things as variables, and use functions to perform actions.

`@instructions`
- Copy and paste the first line of code into the console
- Store your output into a variable named **num**
- Use the sqrt() function on your variable

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
sqrt(5+5)

num <- 5 + 5

___(___)
```

`@solution`
```{r}
sqrt(5+5)

num <- 5 + 5

sqrt(num)
```

`@sct`
```{r}
success_msg("Good work! You've used your first function")
```

---

## Functions

```yaml
type: NormalExercise
key: d29beb634e
xp: 100
```

**Functions** take **arguments** as inputs, for example:

**sum(1 , 4)**


returns 5, where 1 and 4 are **arguments** and sum() is the **function**. 


Similarly, functions can also be used as arguments within other functions:

**sum(1 , sum( 1 ,3))**

Would return the same result because sum(1,3) evaluates to 4.

`@instructions`
Use one of the functions below to perform calculations:

sqrt() #square root

abs() #absolute value 

mean() #average()

print()

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
#Find the square root of 4
___(4)

#Find the absolute value of -16 and store it in a variable called absVal 
absVal <- ___(___)

#Find the square root of absVal
___(absVal)

#Print out the value of absVal
print(___)
```

`@solution`
```{r}
#Find the square root of 4
sqrt(4)

#Find the absolute value of -16 and store it in a variable called absVal 
absVal <- abs(-16)

#Find the square root of absVal
sqrt(absVal)

#Print out the value of absVal
print(absVal)
```

`@sct`
```{r}

```

---

## Basic Syntax

```yaml
type: NormalExercise
key: dde3d6001e
xp: 100
```

Syntax is the spelling and grammer of a programming language, it involvs structuring your scripts in a way R can understand. 

To use functions, it is essential to use the correct syntax. R was designed to be as readable as possible, but it comes with strict rules to enforce a consistent syntax structure. For example, variables  are case sensitive, so if you define:

Two <-2

Then 

sum(two, 5)

Will result in an error.

`@instructions`
- Complete the functions and interpret the results.

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
one <- 1
two <- 2
three <- "3"


one two
one + two

#Use a function to add the variables

___(one, two)

#Try to add a number to the 3 variable, what happens?

sum(___,three)

typeof(three)

#use the as.integer funtion to change 3 from text to a number
sum(one, ___.___(three))

```

`@solution`
```{r}
one <- 1
two <- 2
three <- "3"


one two
one + two

#Use a function to add the variables

sum(one, two)

#Try to add a number to the 3 variable, what happens?

sum(one,three)

typeof(three)

#use a funtion to change 3 from text to a number
sum(one, as.integer(three))

```

`@sct`
```{r}
success_msg("Good work!")
```

---

## Basic Syntax 2

```yaml
type: NormalExercise
key: 39992f162f
xp: 100
```

If you need additional context about a function and its arguments, you can type the symbol **?** before the function into the console. This will bring up R's documentation page which will give a description of the function, list it's arguments, and provide some examples of the function in use.

`@instructions`
- 
Run the first line of code with a question mark before the **seq**() function into the console and read through the documentation. 

- After getting some more context on how the function is used, try creating a sequence **from** 0 **to** 10 **by** 2

- Using ?nchar() find out how many letters are in the string "Hello World"

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
?seq()

seq(___ = ___,___ = ___, ___ = ___)

?nchar()

nchar("___")
```

`@solution`
```{r}
?seq()

seq(from = 1,to = 100, by = 1)

?nchar()

nchar("Hello World")
```

`@sct`
```{r}

```

---

## Additional Exercises

```yaml
type: NormalExercise
key: d76fe74915
xp: 100
```

Follow the instructions to complete the additional challenges. These challenges are optional, but they offer more of a comprehensive glimpse of what's possible with R

`@instructions`
Create a script that stores the number 5 to the variable **n**, then print the variable using the print() function. 

Create a script that finds the square root of the sum of all odd numbers from 0 to 25
- First, create the sequence and store it in a variable named "odds"
- Next, find the sum of the odds variable
- Finally, find the square root of the sum of odds

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
# Store and print the variable
n <- ___

___(n)

# Create the sequence and store the result in the "odds" variable
odds <- seq(___, ___, ___)

#find the sum of all the odd numbers in your sequence
sum(___)

# Find square root of the sum of odds
___(___(odds))
```

`@solution`
```{r}
# Store variable
n <- 5

print(n)

# Create the sequence and store the result in the "odds" variable
odds <- seq(0,25,2)

#find the sum of all the odd numbers in your sequence
sum(odds)

# Find square root of the sum of odds
sqrt(sum(odds))

```

`@sct`
```{r}

```
