---
title: 'Using R'
description: ""
---

## Data Types

```yaml
type: NormalExercise
key: 9e1c8dc226
xp: 100
```

R has 5 major data types we will cover:

- numeric (wide range of numbers including decimals)
- integer (whole numbers)
- character (text or a string such as "Hello")
- logical (True or False response to a logical statement)
- factors (categorical variables)

`@instructions`
Run the sample code one line at a time. Notice what happens when a non-whole number is transformed into an integer. Feel free to play around with the functions.

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
typeof(1)
typeof(1.2)

as.integer(3.2)

char <- "Hello World"
___(char)

1<2
1>2
```

`@solution`
```{r}
typeof(1)
typeof(1.2)

as.integer(3.2)

char <- "Hello World"
print(char)

1<2
1>2

```

`@sct`
```{r}

```

---

## Data Structures

```yaml
type: NormalExercise
key: ee18591110
xp: 100
```

In these exercises, we will cover how you can store data in a:

- Vector
- Matrix
- Data frame

A vector can store many elements of data, as long as all the data is of the same type. In R, a vector can be created with the c() function, which allows you to combine (or **concatinate**) many elements in one. For example, c(1,2,3) creates a vector with numbers 1 to 3, seq(1,3) would give the same result. You can also use the : symbol to create vectors. For example, 1:10 creates a vector with numbers 1 to 10.

You can create matrices in R using the matrix() function. Try pasting the below code in your Console.

a <- matrix(1:12, nrow = 3, byrow = T)
a

Data frames are similar to matrices and the table structure in Excel. Each row represents a unique observation and each column represents a variable. Data frames are one of the most widely used data structure in R.

`@instructions`
-Store a five, ten and fifteen into the variable **vector**
-Find the sum of all the elements of **vector**
-Use the head(), summary() and str() functions to inspect the diamonds data frame
-

`@hint`


`@pre_exercise_code`
```{r}
library(ggplot2)
```

`@sample_code`
```{r}
# Create vector
vector  <- c(___,___,___)

# Find sum
sum(___)

# head(), summary() and str()
head(diamonds)

summary(diamonds)

str(diamonds)
```

`@solution`
```{r}
vector  <- c(5,10,15)

sum(vector)

head(diamonds)

summary(diamonds)

str(diamonds)
```

`@sct`
```{r}

```

---

## Subsetting

```yaml
type: NormalExercise
key: ca381e61a5
xp: 100
```

Each data structure must be subset in a unique way:

- Vectors: can be subset with a single number in square brackets **[]** indicating their position in the vector. 

vector <- c(1,5,3,4)
vector[2] # Outputs 5

- Matrices: can be subset using square brackets with a comma separating the row and column indices respectively.

a <- matrix(1:12, nrow = 3, byrow = T)
a[2,3] # Outputs the data point in the second row of the third column

- Data frames: Similar to subsetting matrices, but columns can also be called directly by name by using the $ symbol after the name of the data frame (names are explained in the next exercise).

`@instructions`
Subset a vector, matrix and data frame (using the $ subsetting method).

`@hint`


`@pre_exercise_code`
```{r}
library(ggplot2)
```

`@sample_code`
```{r}
#Call the 4th element of the vector
vector <- c(1,5,3,4)
vector[___]

#Call the 2nd element in the 4th column of the matrix
a <- matrix(1:12, nrow = 3, byrow = T)
a[___,___]

#Call only the **carat** column within the **diamonds** data frame
diamonds$___


```

`@solution`
```{r}
#Get the 4th element of the vector
vector <- c(1,5,3,4)
vector[4]
#Get the 2nd element in the 3rd row of the Matrix
a <- matrix(1:12, nrow = 3, byrow = T)
a[2,3]

#Get the carat column Data frame
diamonds$carat


```

`@sct`
```{r}

```

---

## rbind and names()

```yaml
type: NormalExercise
key: db6307e18b
xp: 100
```

**rbind()** allows you to add or bind extra rows of data to existing data. The **names()** function can name or rename column headers.

`@instructions`
1. Store the numbers 1 to 10 into a variable **A** 
2. Store the numbers 11 to 20 into a variable **B** 
3. Use rbind() to merge the two vectors into a data frame **df**
4. Name the columns of the newly created data frame by passing the **clnmes** variable into the the names() function

`@hint`
Use the : symbol or seq() function to create the vectors
The names() function takes a data frame or matrix as an argument

`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
# Assign variable A
A <- ___

# Assign variable B
B <- ___

# Bind B to A and store the output in the variable df then print the output
df <- ___(___,___)
df

# Rename the column headers
clnmes <- c("onetoten", "eleventotwenty")
___(__) <- clnmes

# Print the variable df into the console
df
```

`@solution`
```{r}
A <- 1:10
B <- 11:20
df <- rbind(A,B)
df
clnmes <- c("onetoten", "eleventotwenty")
names(C) <- clnmes
df
```

`@sct`
```{r}

```

---

## dplyr preview

```yaml
type: NormalExercise
key: 3fe03bbcf3
xp: 100
```

dplyr is one of the most useful packages R offers. Developed by Hadley Wickham, it offers some of the best and intuitive tools for working with your data. In reality, the most time-consuming part of data analysis is the time spent cleaning and preparing your data. dplyr makes this process easier, faster, and more reproducible. We will cover dplyr more in section 2 when will collect and clean a real dataset, but right now we will examine the filter() and select() functions.



`@instructions`
==

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
library(___)

data <- diamonds

#Filter the data to show only the diamonds where cut is Ideal 
filter(data, cut == ___)  #remember R is case sensitive

#Save to a variable
ideal <- filter(data, ___ == ___) 

x_y_z <- select(data, ___, ___, ___)

xyz <- select(data, ___:___)

identical(x_y_z, xyz)

all_except_y <- select(data, -___)
```

`@solution`
```{r}
library(dplyr)

data <- diamonds

#Remember R is case sensitive
filter(data, cut == "Ideal") 

#Save to a variable
ideal <- filter(data, cut == "Ideal") 

x_y_z <- select(data, x,y,z)

xyz <- select(data, x:z)

identical(x = x_y_z, xyz)

all_except_y <- select(data, -y)
```

`@sct`
```{r}

```

---

## Practice exercises 1

```yaml
type: NormalExercise
key: 4481b90ca6
xp: 100
```

Follow the instructions to complete the additional challenges. These challenges are optional, but they offer more of a comprehensive glimpse of what's possible with R

`@instructions`
- Subset the vector diamonds$carat to find the 6th value

- Subset the diamonds dataframe to keep only cut and price columns

- Subset the diamonds dataframe to find the 8th row in the price column

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
#Create subset Here


#Create sutset Here


#Create subset Here

```

`@solution`
```{r}
diamonds$carat[6]

select(diamonds, cut, price)

diamonds$price[8]
```

`@sct`
```{r}

```
