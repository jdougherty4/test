---
title: 'Visualization with ggplot2'
description: ""
---

## Introduction to ggplot2

```yaml
type: NormalExercise
key: d05e04f242
xp: 100
```

ggplot2 is the most comprehensive visualization package in R. Developed by Hadley Wickham, ggplot2 offers the ability to use any type of chart in a consistent and reproducible way. Although the code to create each chart looks very similar, it can be easily adapted to add or subtract additional aesthetic layers. We will introduce the ggplot2 package here with the diamonds dataset to create many different plots.

`@instructions`
Follow the instructors guide to using the ggplot on the diamonds dataset

`@hint`


`@pre_exercise_code`
```{r}
link <- "https://assets.datacamp.com/production/repositories/3649/datasets/e8f6da0057be7be15146e8f66ed150429b613429/prices_fin.csv"
data <- read.csv(link)

library(ggplot2)
```

`@sample_code`
```{r}
diamonds
?diamonds

head(diamonds)

#Get some more info on your data
summary(diamonds)

#save the data in its own variable
data <- diamonds

___(data = ___, aes(x = ___))

___(data = ___, ___(x = ___)) + 
  geom_bar()

#save the outline of the plot to aviod typing the same code
a <- ___(data = ___, aes(x = ___))

a + geom_bar()

# switching to another chart tpye which requires a y variable
a + geom_boxplot(___(y = ___))

a <- ggplot(data = data, aes(x = cut, ___ = color))
a + geom_bar()

?geom_bar()

a + geom_bar(position = ___)


a + geom_bar(position = ___)

```

`@solution`
```{r}
diamonds
?diamonds

head(diamonds)
summary(diamonds)

data <- diamonds

ggplot(data = data, aes(x = cut) )

ggplot(data = data, aes(x = cut) ) + 
  geom_bar()

a <- ggplot(data = data, aes(x = cut) )

a + geom_bar()

a + geom_boxplot(aes(y = price))

a <- ggplot(data = data, aes(x = cut, fill = color) )
a + geom_bar()

?geom_bar()

a + geom_bar(position = "dodge")


a + geom_bar(position = "fill")

```

`@sct`
```{r}

```

---

## Scatterplots

```yaml
type: NormalExercise
key: 25e1fbb73c
xp: 100
```

Scatterplots allow you to see how variables interact with each other. You can get lots of insights from plotting one variable with another. Generally, the y variable is the one of interest. The y variable is sometimes called the dependent variable because its value depends on the values of the x variables. In the diamonds dataset, the **price** can be considered the dependent vairable while in the mtcars dataset, **mpg** is the dependent vairable.

`@instructions`


`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
library(ggplot2)

data <- diamonds

___(data, ___(x = ___, y = ___)) + 
   ___()

mtcars
?mtcars

data2 <- mtcars

ggplot(data2, aes(x=___, y = ___)) + 
  geom_point()

ggplot(data2, aes(x=wt, y = mpg, colour = ___)) + 
  geom_point()

ggplot(data2, aes(x=wt, y = mpg, colour = factor(___)) ) 
  geom_point()

str(data2)

data2$cyl <- as.factor(data2$cyl)

str(data2)

```

`@solution`
```{r}
library(ggplot2)

data <- diamonds

ggplot(data, aes(x=x, y = price)) + #Mapping is inside aes()  function. (have students run by itself at first)
    geom_point() # good for dotplots to see the relationships between variables

mtcars
?mtcars
data2 <- mtcars

ggplot(data2, aes(x=wt, y = mpg)) + 
  geom_point()

ggplot(data2, aes(x=wt, y = mpg, colour = cyl)) + 
  geom_point()

ggplot(data2, aes(x=wt, y = mpg, colour = factor(cyl)) ) + #Explain factors here 
  geom_point()

str(data2)

data2$cyl <- as.factor(data2$cyl)

str(data2)

```

`@sct`
```{r}

```

---

## Visualizing correlations between 2 plots

```yaml
type: NormalExercise
key: 58ccf786be
xp: 100
```

We are interested in seeing how an x variable impacts a y variable. To do this, it's equally important to know how each x variable impacts each other. It is the analysts job to find out which variable actually has the highest correlation with the y variable. For example,suppose a popular SUV was painted green, but most other cars have blue or black paint. If someone looked at the relationship between car colors and mpg, they might incorrectly assume that green paint leads to lower mpg, when in reality the car type was causing the positive relationship.

`@instructions`
Similar to the example above, we are given a cars dataset with the goal of finding out what factors lead to higher mpg. See the different ways ggplot allows us to view the data.

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
?mtcars

data <- mtcars

data

summary(data)

ggplot(data, aes(x = wt, y = mpg)) + 
  geom_point()

ggplot(data, aes(x = wt, y = mpg)) + 
  geom_point() +
  geom_smooth()

#seeing correlations between two x variabales

ggplot(data, aes (x = cyl, y = wt)) + #What does this say about cars with more cylinder?
  geom_point()

ggplot(data, aes (x = hp, y = wt)) + 
  geom_point()

ggplot(data, aes (x = hp, y = wt)) + 
  geom_point()+
  facet_wrap(factor(cyl)~.)

ggplot(data, aes (x = hp, y = wt, colour = factor(am))) + 
  geom_point()+
  facet_wrap(factor(cyl)~.)

```

`@solution`
```{r}
?mtcars

data <- mtcars

data

summary(data)

ggplot(data, aes(x = wt, y = mpg)) + 
  geom_point()

ggplot(data, aes(x = wt, y = mpg)) + 
  geom_point() +
  geom_smooth()

#seeing correlations between two x variabales

ggplot(data, aes (x = cyl, y = wt)) + #What does this say about cars with more cylinder?
  geom_point()

ggplot(data, aes (x = hp, y = wt)) + 
  geom_point()

ggplot(data, aes (x = hp, y = wt)) + 
  geom_point()+
  facet_wrap(factor(cyl)~.)

ggplot(data, aes (x = hp, y = wt, colour = factor(am))) + 
  geom_point()+
  facet_wrap(factor(cyl)~.)

```

`@sct`
```{r}

```

---

## Practice exercises

```yaml
type: NormalExercise
key: a13105a449
xp: 100
```

Follow the instructions to complete the additional challenges. These challenges are optional, but they offer more of a comprehensive glimpse of what's possible with R

`@instructions`
Create a scatterplot showing quality on the x-axis and price on the y-axis

create a box plot showing the distribution of the quality variable

Use facet_wrap() to get a boxplot of the price by quality.

`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
#Create Chart Here


#Create Chart Here


#Create Chart Here
```

`@solution`
```{r}

```

`@sct`
```{r}

```

---

## Try to make a plot yourself!

```yaml
type: NormalExercise
key: beba48bb98
xp: 100
```



`@instructions`


`@hint`


`@pre_exercise_code`
```{r}
# put many datasets in here.
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
