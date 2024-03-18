# Visualizing momentum

`Momentum' in optimization theory is usually introduced as an ad-hoc improvement over vanilla gradient descent, by leveraging moving averages of the collected gradients to not get stuck in inflections or bad minimas. But momentum is so much more. Quoted from this brilliant [article](https://distill.pub/2017/momentum/) - "Let’s say this for now — momentum is an algorithm for the book."

## Mechanics
---
Consider a body at location $x$ with a force $f$ acting on it. According to Newton said,
$$m\ddot{x} = f$$

Now $f$ could be a single force, or it could be a vector addition of all the multiple forces acting on the body. It could also be a function of $x$, like a spring. Let's consider two forces, one which is a function of space $x$ and another a function of speed $\dot{x}$

$$m