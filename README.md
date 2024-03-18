# Visualizing momentum

"Momentum" in optimization theory is usually introduced as an ad-hoc improvement over vanilla gradient descent. By leveraging moving averages over gradients, the optimizer manages to not get stuck in inflections or bad minimas. But momentum is so much more. Quoted from this brilliant [article](https://distill.pub/2017/momentum/):

<it>"For now — momentum is an algorithm for the book."</it>

## Mechanics
Consider a body at location $\bold{x}$ with a force $\bold{f}$ acting on it. Newton said,
$$m\ddot{\bold{x}} = \bold{f}$$
Now $f$ could be a single force, or it could be a vector addition of all the multiple forces acting on the body. It could also be a function of $x$, like a spring.

Let's consider two forces, one which is a function of space $\bold{x}$ and another 'drag force' proportional to velocity $\dot{x}$ acting in the direction opposite to the movement, then,

$$m\ddot{\bold{x}} = \eta g(\bold{x}) - \nu \dot{\bold{x}}$$

