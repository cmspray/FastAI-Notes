#  [Lesson 1](https://www.youtube.com/watch?v=IPBSB1HLNLo&list=PLfYUBJiXbdtS2UQRzyrxmyVHoGW0gmLSM&index=1)

## Dogs vs Cats
This lesson went over using [fast.ai](fast.ai) to build a deep learning model that classifies dogs vs. cats.

Most of the lesson was just how to use the fast.ai library, but not much in depth on what exactly it is doing.

## Neural Network
- This is the underlying function behind deep learning
- Consists of a number of linear layers with non-linear layers
- Makes up the [Universal Approximation Theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem)
  - The theorem thus states that simple neural networks can represent a wide variety of interesting functions when given appropriate parameters
- [Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent) is what is used to fit the parameters minimizing the [loss function](https://en.wikipedia.org/wiki/Loss_function)
  - This is done by changing the parameters a little bit and checking how that affects the loss
  - This was a very slow process before GPU's
