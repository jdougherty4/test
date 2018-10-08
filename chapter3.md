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

ggplot2 is the most comprehensive visualization package in R. It offers the ability to use any type of chart in a consistent and reproducible way. Although the code to create each chart looks very similar, it can be easily adapted to add and subtract additional aesthetic layers.

`@instructions`


`@hint`


`@pre_exercise_code`
```{r}
link <- "https://assets.datacamp.com/production/repositories/3649/datasets/e8f6da0057be7be15146e8f66ed150429b613429/prices_fin.csv"
data <- read.csv(link)

library(ggplot2)
```

`@sample_code`
```{r}
#Load the ggplot2 package
___(ggplot2)
#The Dataset named "Data" is loaded into your workspace
head(data)

data1 <- data[,1:5]


a <- ggplot(data = data1, aes(x = Year, y =Price ) )

a + geom_point()

ggplot(data2, aes(x = ___, y = ___,  color = Products) ) +
  geom_point()+
  facet_wrap(___~Products) +
  theme(axis.text.x=element_blank())

```

`@solution`
```{r}
#Load the ggplot2 package
___(ggplot2)
#The Dataset named "Data" is loaded into your workspace
head(data)

data1 <- data[,1:5]


a <- ggplot(data = data1, aes(x = Year, y =Price ) )

a + geom_point()

ggplot(data2, aes(x = Year, y = Price,  color = Products) ) +
  geom_point()+
  facet_wrap(.~Products) +
  theme(axis.text.x=element_blank())

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



`@instructions`


`@hint`


`@pre_exercise_code`
```{r}

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

---

## Visualizing correlations between 2 plots

```yaml
type: NormalExercise
key: 58ccf786be
xp: 100
```



`@instructions`


`@hint`


`@pre_exercise_code`
```{r}

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
