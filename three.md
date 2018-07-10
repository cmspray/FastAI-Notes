[<<](/README.md)
# [Lesson Three](https://youtu.be/9C06ZPF8Uuc)

- Precompute is only a way to cache some steps to speed it up
- Study logs and Exponentiation math
- Softmax is x/sum
  - sum of softmax should be 1
  - inputs should be >= 0
- Since images are matricies, multiply by some number to make it less washed out

## bn_freeze
- If you're using a deeper model, if the dataset is similar to the dataset that trained the model, this will help (more about this later in the course)
  - Stands for batch normalization

## predict_array
- You can use this to predict a single image while passing in your image
  - If you index an array with [None] it turns the array input into a tensor since  that's what predict is expecting
- You're have to transform your image using tfms_from_model

## Intro to theory behind Convolutional Neural Networks
- Matrix of N x N is multiplied by each N x N section of the image and outputs the next layer ([Excel Example](https://docs.google.com/spreadsheets/d/1rXJ_tmMAePh07nBdMBc18kfaANP02vL0E9ii-kSRsnA/edit#gid=1707540045))
- This is done again and again until the last layer
- Some layers may check for left edges, lower edges, eyes, etc

[<<](/README.md)
