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



`@instructions`


`@hint`


`@pre_exercise_code`
```{r}
link <- "https://assets.datacamp.com/production/repositories/3522/datasets/15037db2827169bf67b3db91ec70cd9e235737dd/Prices_Data12.csv"
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


a <- ggplot(data = data1 aes(x = Year, y =Price ) )

a + geom_point()
```

`@solution`
```{r}

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
