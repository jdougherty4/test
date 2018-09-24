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
- integer (must be whole numbers)
- character (text or a string, "Hello")
- logical(A True or False response to a logical statement)

`@instructions`
Check out and change the different types of data. Notice what happens when a non-whole number is transformed into an integer.

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
typeof(1)
typeof(1.2)

as.integer(___)

char <- "Hello World"

print(___)

1<2
1>2
```

`@solution`
```{r}
typeof(1)
typeof(1.2)

as.integer(1.2)

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

In this chapter, we will cover how you can store data in a:

- vector
- Matrix
- Data frame
- list

A vector can store many elements of data, as long as all the data is the same type. In R, a vector can be created with the c() function, which allows you to combine (or **concatinate**) many elements in one. For example, c(1,2,3) creates a vector with numbers from 1 to 3, seq(1,3) would give the same result. 

You can also create matrices in R using the matrix() function. Try pasting the below code in your Console.

a <- matrix(1:12, nrow = 3, byrow = T)
a

Data frames are similar to the table structure in Excel. Each row represents a unique observation and each column representing a variable. 

Lists are a special type of data structure that can store many other data structures. One list can contain a vector, a matrix, data frame, and even another list.

`@instructions`
Complete the code to run calculations on the different types of data.

`@hint`


`@pre_exercise_code`
```{r}
library(ggplot2)
```

`@sample_code`
```{r}
vector  <- c(___,___,___)

sum(___)

head(diamonds)

summary(diamonds)

str(diamonds)

sum(diamonds$___)
```

`@solution`
```{r}
vector  <- c(5,10,15)

sum(vector)

head(diamonds)

summary(diamonds)

str(diamonds)

sum(diamonds$carat)

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

Each data structure has its own unique way to subset its data:

- Vector: can be subsetted with a single number in brackets [] indicating their position in the vector. 

  vector <- c(1,5,3,4)

  vector[2] #Outputs 5

- Matrix: can be subsetted with single brackets with a comma separating the rows and columns respectively.
a <- matrix(1:12, nrow = 3, byrow = T)
a[2,3]

- Data frame: Similar to subsetting matrices, but columns can be called directly.


- List: Can be subsetted using double brackets to refer to the structure and respective element
list1 <- list(c(1,2,3), diamonds)  
list1[[2]][1]

`@instructions`
Subset a vector, matrix, data frame (using the $ subsetting method), and list as instructed.

`@hint`


`@pre_exercise_code`
```{r}
library(ggplot2)
```

`@sample_code`
```{r}
#Get the 4th element of the vector
vector <- c(1,5,3,4)
vector[___]
#Get the 2nd element in the 3rd row of the Matrix
a <- matrix(1:12, nrow = 3, byrow = T)
a[___,___]

#Get the carat column Data frame
diamonds$___

#Get the 4th element in the second vector of the List
list1 <- list(c(1,2,3), c(4,5,6,7) )  
list1[[___]][___]

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

#Get the 4th element in the second vector of the List
list1 <- list(c(1,2,3), c(4,5,6,7) )  
list1[[2]][4]

```

`@sct`
```{r}

```

---

## Practice exercises

```yaml
type: NormalExercise
key: 4481b90ca6
xp: 100
```

Follow the instructions to complete the additional challenges. These challenges are optional, but they offer more of a comprehensive glimpse of what's possible with R

`@instructions`
Subset the vector diamonds$carat to find the value in the 6th row
Subset the diamonds dataframe to keep only cut and price columns
subset the diamonds dataframe to find the 8th row in the price column

`@hint`


`@pre_exercise_code`
```{r}
#Create subset Here


#Create sutset Here


#Create subset Here
```

`@sample_code`
```{r}

```

`@solution`
```{r}

```

`@sct`
```{r}

```
