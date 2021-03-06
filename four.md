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
- It removes the dependent variable and returns the modified dataframe and the dependent variable as its own vector
- You can scale the output variable if you'd like
  - If you do, it returns the scale so you can use it on additional data later
- It also will fill in missing values
  - Categorical becomes 0 where the rest become [1,2,3...]
  - Continuous becomes the mean and adds another vector to the output of booleans that tells if that value was missing

##  Embeddings
- Used for any categorical variables
- Essentially converts the 1 value per category to an array of values
  - The way to do this is using a matrix with `N` rows where `N` is the number of categories
  - A good place to start with the length of each row is `min(50, (c+1)/2)` where `c` is the cardinality of that category
  - Then when training with that category, lookup the index of that category in the matrix and train on that
- These embeddings are randomly initialized, you could also use pretrained embeddings though if you have those
- This associates each category with more than just one variable
- Embeddings wouldn't work well with very large cardinality categories

## fast.ai add_datepart
- Takes a dataframe and a column name (that is a date) this removes the column and adds columns for useful parts of the date (year, month, day, etc.)

# NLP - Intro
## Language Models
- For example, can be used to guess next word in a sentence or if a block of text is generally positive or negative
  - [**torchtext**](https://github.com/pytorch/text)
  - [**spacy_tok:**](https://spacy.io/api/tokenizer) is a common python library that tokenizes natural language

## fast.ai language Models
- **min_freq** variable in `LanguageModelData` constructor will drop words that don't appear that many times
- When `LanguageModelData` is created, it adds a `vocab` variable to the `TEXT` passed which contains the entire datasets vocab mapped to integers
- **bptt (Back prop through time)** is the length of text being used each batch
  - The length is randomized each iteration
- Each word in the vocab gets it's own embedding vector (it's just a categorical variable)
- **learner.clip** ensures you don't move the learning rate too far

[<<](/README.md)
