[<<](/README.md)

# [Lesson 5](https://youtu.be/J99NV9Cr75I)

- Add a `_` to Pytorch's tensor functions to have it not return anything and instead run the function in place (example: `x -=3` is the same as `x.sub_(3)`)
- [Broadcasting](https://docs.scipy.org/doc/numpy/user/basics.broadcasting.html): a way to add a vector to a matrix by duplicating it to match the size of the matrix
- [Bias](https://en.wikipedia.org/wiki/Bias_of_an_estimator): Say a user rates films very high, you want to add a weight to that user to know they generally rate movies high
- Weight decay: penalizes big weights to generalize the network
- Momentum: A way to increase or decrease the learning rate to speed up gradient descent

## Collaborative Filtering for Recommender Systems
- Can be shown in [excel](https://github.com/fastai/fastai/blob/master/courses/dl1/excel/collab_filter.xlsx)
- The vectors that are embeddings for the movies might be factors that weigh features of the movie (how much sci-fi, romance, etc)
- The vectors that are embeddings for the users might be factors that weigh features of movies that user likes
- Start by randomizing them, then use gradient descent to minimize loss on movies users have rated
- Now you can predict how a user may rate a movie

## Collaborative Filtering with fastai
- `CollabFilterDataset` just like any other data set which provides you a learner
- Can use learning rate finder and everything
- Sigmoid function used to put output between two bounds

[<<](/README.md)
