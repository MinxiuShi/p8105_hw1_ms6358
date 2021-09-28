# p8105_hw1_ms6358
The chunk below creates a dataframe containing a sample of size 10 from a 
random normal variable, constructs the specified logical vector, character
vector and factor vector.The code chunk also finds the mean of the sample and
stores it for easy in-line printing.

```{r}
library(tidyverse)

example_df = tibble(
  vec_numeric = rnorm(10,sd = 1),
  vec_logical = vec_numeric > 0,
  vec_char = c("This", "is", "my", "first", "homework", "for", "the", "course", "Data", "Science"),
  vec_factor = factor(c("good", "good", "good", "great", "great", "great", "excellent", "excellent", "excellent", "excellent"))
)

mean_vec_numeric = mean(pull(example_df, vec_numeric))

mean_vec_logical = mean(pull(example_df, vec_logical))
 
mean_vec_char = mean(pull(example_df, vec_char))

mean_vec_factor = mean(pull(example_df, vec_factor))
```
