[<<](/README.md)
# [Lesson 4](https://youtu.be/gbceqO8PpBg)

- **Dropout:** Deletes a random number of activations, used to prevent overfitting
  - Drop too much, too generalized. Too little, still overfit.

## Structured Data
- Must specify what kind of columns your data has typically 2 kinds
  - **Categorical:** This discrete number of things (year, month, day of the week, alphabet, etc)
  - **Continuous:** Think floating point numbers (age, temperature, weight, etc)

## fast.ai `proc_df()`
- This takes a pandas dataframe and the name of the dependent variable
- It removes the dependent variable and returns the modified datafram and the dependent variable as its own vector
- You can scale the output variable if you'd like
  - If you do, it returns the scale so you can use it on additional data later
- It also will fill in missing values
  - Categorical becomes 0 where the rest become [1,2,3...]
  - Continuous becomes the mean and adds another vector to the output of booleans that tells if that value was missing







[<<](/README.md)
