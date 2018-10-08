---
title: 'Extra Exercises'
description: ""
---

## Insert exercise title here

```yaml
type: NormalExercise
key: caba581a53
xp: 100
```



`@instructions`


`@hint`


`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
'Count the sum of odd numbers in the following vector.'

vector <- c(1:3,5,7,3,1,9,2,2,8,7)
vector %% 2
sum(vector %% 2)

'Find the proportion of odd numbers within the vector'

sum(vector %% 2)/ length(vector) 

'Find the percentage of even numbers within the vector'

1 - sum(vector %% 2)/ length(vector)
```

`@solution`
```{r}

```

`@sct`
```{r}

```
