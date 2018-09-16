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

All code that we write in these boot camps is called scripts. Every time you execuate code, it's run through the console. You can use the Console located at the bottom to tell R what to do. You can do math, save things as variables, and use functions to perform actions.

`@instructions`
- Copy and paste the first line of code into the Console
- Store your output into a variable
- Use the sqrt() function on your variable

`@hint`
- Here is the hint for this setup problem. 
- It should get students 50% of the way to the correct answer.
- So don't provide the answer, but don't just reiterate the instructions.
- Typically one hint per instruction is a sensible amount.

`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
sqrt(5+5)

___ <- 5+5

___(___)
```

`@solution`
```{r}
sqrt(5+5)

num <- 5+5

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

Broadly, syntax in R describes how to structure your inputs in a way that R can understand. If you have a solid base with syntax you can handle errors with a much better understanding. R was designed to be as intuitive as possible, but it comes with stricter rules to enforce a consistent structure. For example, variables (covered last lesson) are case sensitive, so ensure you know whether or not your variables are capitalized.

**Functions** take **arguments** as inputs, **functions** can also be used as arguments within other functions. For example:

sum(1,4)

returns 5, where 1 and 4 are **arugments** and sum() is the function. Similarly:

sum(1,sum(1,3)) 

Would return the same result becuase sum(1,3) evaluates to 4.

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

#Use the sum() function to add the varianles.
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
Great work!
```

---

## Basic Syntax 2

```yaml
type: NormalExercise
key: 39992f162f
xp: 100
```

If you need additional context about a function and its arguments, you can type the symbol **?** before the function into the console. This will bring up Rs documentation page which will give a description of the function, list its arguments, and provide some examples of the function in use.

`@instructions`
1. Type a question mark before the rep() function into the console and read through the documentation. After getting some more context on how the function is used, try creating the same number 10 times. 

2. paste the code: ?seq() into the console.

3. Create a sequence from 1 to 100

4. Store a word into a variable and find the length of the stored word with the function len().

`@hint`


`@pre_exercise_code`

```{r}

```


`@sample_code`

```{r}

```


`@solution`

```{r}
?Rep()

?seq()

?length()
```


`@sct`

```{r}

```
