---
mathenabled: true
---

We write an elongated-S to represent the antiderivative of a function when we do integration, but what would you do if you were told not to use it? That's what we explore here. Although this path is not any easier than the normal method, it certainly makes a point that even if notations don't matter in the end, and what matters is the process, or more importantly, the end result, they do play of role in our understanding more than we acknowledge.

Nothing is better than showing an example, so here's an example of a rational function imbuing trigonometric functions. 

$$
f\left(x\right) = \frac{\sec^2 x}{\left(\sec x + \tan x\right)^2}
$$

Now, let $$ F $$ be the integral of $$ f\left(x\right) $$; its derivative according to the **fundamental law of calculus** is the integrand, i.e. $$ f(x) $$. Here, what follows is a little manipulation of the original expression by expressing the trigonometric functions in form of  $$ \tan \left({x \over 2}\right) $$, so that we can do [tangent half-angle substitution][half-angle-subst]. And, why does this work? It does, because it does; mathematical processes make no inherent sense—an accepted truth amongst students of mathematics. You may solve a mathematical problem, but you can seldom reason about the process itself.

$$
\begin{align*}
\frac{d F}{dx}\left(x\right) &= \frac{\sec^2 x}{\left( \sec x + \tan x \right)^2} \\
&= \frac{\left( \frac{1 + \tan^2 {x \over 2}}{1 - \tan^2 {x \over 2}} \right)^2}{\left( \frac{1 + \tan^2 {x \over 2}}{1 - \tan^2 {x \over 2}} + \frac{2 \tan {x \over 2}}{1 - \tan^2 {x \over 2}} \right)^2} \\
&= \frac{\left( 1 + \tan^2 {x \over 2} \right)^2}{\left( 1 + \tan^2 {x \over 2} + 2 \tan {x \over 2} \right)^2} \\
&= \frac{\left( 1 + \tan^2 {x \over 2} \right) \sec^2 {x \over 2}}{\left(1 + \tan {x \over 2}\right)^4} \\
&= 2\frac{d J}{dz}\frac{dz}{dx} \\
\end{align*}
$$

We substitute in $$ z = \tan \left( {x \over 2} \right) $$, and use the chain-rule (on the very last line). This is equivalent to regular u-substitution; normally done with differentials, here done with differential coefficients (derivatives).

$$
\begin{align*}
\frac{d J}{dz} \left(z\right) &= \frac{1 + z^2}{\left( 1+z \right)^4} \\
&= \frac{\left(1 + z\right)^2 - 2z}{\left( 1+z \right)^4} \\
&= \left( 1+z \right)^{-2} - \frac{2z}{\left( 1+z \right)^4} \\
&= \left( 1+z \right)^{-2} - 2\frac{\left(1 + z\right) - 1}{\left( 1+z \right)^4}  \\
&= \left( 1+z \right)^{-2} - 2\left( 1+z \right)^{-3} + 2 \left( 1+z \right)^{-4} \\

J\left(z\right) &= -\left( 1+z \right)^{-1} + \left( 1+z \right)^{-2} - \frac{2}{3} \left( 1+z \right)^{-3} \\
\end{align*}
$$

Now, just the value of $$ z = \tan \left({x \over 2}\right) $$ has to be substituted back into $$ J $$ to turn it from a function of $$ z $$ into a function of $$ x $$. 

$$
J\left(x\right) = -\left( 1+\tan {x \over 2} \right)^{-1} + \left( 1+\tan {x \over 2} \right)^{-2} - \frac{2}{3} \left( 1+\tan {x \over 2} \right)^{-3}
$$

We know,

$$
\frac{d F}{dx} = 2\frac{d J}{dz}\frac{dz}{dx} = 2 \frac{dJ}{dx}
$$

Integrating either sides (w.r.t $$ x $$) the result is obvious, i.e. $$ F = 2J + C$$.

$$
\therefore I = \frac{2}{3} \left[3\left( 1+\tan {x \over 2} \right)^{-1} -3\left( 1+\tan {x \over 2} \right)^{-2} - 2 \right]\left( 1+\tan {x \over 2} \right)^{-3} + C
$$

> Santacharya devised this method of integration in 1994 during his stay in Japan. He almost forgot the constant-C, but he remembered at the last moment, for he had the blessings of mother Cynthia of the Junglemahals.

[half-angle-subst]: https://en.wikipedia.org/wiki/Tangent_half-angle_substitution
