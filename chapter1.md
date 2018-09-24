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

All code that we write in these boot camps is called scripts. Every time you execute code, it's run through the console. You can use the console located at the bottom to tell R what to do. You can perform math operations, save things as variables, and use functions to perform actions.

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

## Basic Syntax

```yaml
type: NormalExercise
key: dde3d6001e
xp: 100
```

Broadly, syntax in R describes how to structure your inputs in a way that R can understand. If you have a solid base with syntax, you can handle errors with a much better understanding. R was designed to be as intuitive as possible, but it comes with strict rules to enforce a consistent structure. For example, variables (covered last lesson) are case sensitive, so ensure you know whether or not your variables are capitalized.

**Functions** take **arguments** as inputs, **functions** can also be used as arguments within other functions. For example:

sum(1,4)

returns 5, where 1 and 4 are **arugments** and sum() is the function. Similarly:

sum(1,sum(1,3)) 

Would return the same result because sum(1,3) evaluates to 4.

`@instructions`
Use functions to perform calculations on the data below.

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

#Use the sum() function to add the variables
sum(___,___)

sum(___,three)

sum(one, ___.___(three))
```

`@solution`
```{r}
one <- 1
two <- 2
three <- "3"

one two

one + two

#Use the sum() function to add the varianles.
sum(one,two)

sum(one,three)

sum(one, as.integer(three))
```

`@sct`
```{r}
success_msg("Good work! Dumby")
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
1. Run the first line of code with a question mark before the **rep**() function into the console and read through the documentation. After getting some more context on how the function is used, try replicating the number 2 ten times. 

2. paste the code: ?**seq**() into the console.

3. Create a sequence from 1 to 100

4. Store a word into a variable and find the length of the stored word with the function **length**().

`@hint`


`@pre_exercise_code`
```{r}
words <- c("Hello", "World", "!") 
```

`@sample_code`
```{r}
?rep()

rep(___,___)

seq(___,___)

words

length(___)
```

`@solution`
```{r}
?rep()

rep(2,10)

seq(1,100)

words

length(words)
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
Create a script that prints the username, the username can be created using a variable. 
Create a script that adds a **sequence** of numbers from 0 to 15 by 3
Save the last result as a variable and take the square root of the result above

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
#Create username Here


#Create sequence sum Here


#Find square root Here
```

`@solution`
```{r}

```

`@sct`
```{r}

```
