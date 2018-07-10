#  [Lesson 2](https://youtu.be/JNxcznsrRb8)

## Learning Rate
- The thing that decides how quickly gradient descent "descends"
  - Too high and we might zigzag around the minimum as we might skip over it.
  - Too low and it will take forever

## [Learning Rate Finder](https://arxiv.org/pdf/1206.1106.pdf)
- What this does, is it looks at a small batch of files and gradually increases the learning rate (starts really small, gets huge)
- Then plot the learning rate vs. loss and you'll notice the loss goes to some minimum before beginning to increase again
  - The lowest point is not the best learning rate because the learning rate is not getting better, and we want it while it still is getting better
- The learning rate from this learning rate finder is not the true 100% best way to find it, as there are other variables to consider
- This is the best thing to tweak to improve your accuracy

## Data Augmentation
- A way to get more data without getting more data
  - Images can be rotated, zoomed, cropped
    - Maybe don't flip all things along the x axis, we still want the image to look like the real world

## Precompute in fast.ai
- Each linear layer has some activations
- The second last layer is the last layer that has all the information, the precomputed activations
- By using precomputed activations, you just have to compute those activations once and can then save them
- When adding new data (or augmenting) you shouldn't use the precomputed activations as they won't be the same

- If the training loss is much lower than the validation loss, that means you're **overfitting**
  - This is because the training set is much more accurate than the validation set
  - Model isn't generalized

## Cycle Length in fast.ai (Learning Rate Annealing)
- As you get closer to minimum during gradient descent, you could lower the learning rate to get a more accurate minimum
  - fast.ai uses cosine annealing (learning rate drops on a cosine curve)
  - Learning rate goes up, reduces while training, and jumps back up
  - This allows the model to maybe jump out of a local minimum into a better minimum
- The parameter resets the learning rate every x epoch
- **cycle_mult** will multiply the number of epochs that run before the learning rate is reset

## fast.ai save and load
- Creates tmp files from a learner in the models folder
- tmp files in tmp can be removed in case you see weird results (maybe activations were only half computed)

## fast.ai unfreeze
- Unfreeze will unfreeze all layers and begin retraining each layer based on your training set

## Learning rate array
- You can pass a learning rate for every layer to more fine tune your models

## Confusion matrix
- Way to compare true labels vs predicted labels, visualizes your model's predictions

## Changing data set
- You can start by training on a small training set, then later reset the data to a larger set, this reduces training time by getting a good starting point
