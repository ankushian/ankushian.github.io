---
mathenabled: true
---

Rather an write an *elongated-S* to represent the antiderivative of an integrand (function to be integrated), can't there be a way to integrate a function without ever using it? Although there is a path, it doesn't turn the tiresome process any easier. The point here is to show that a lot of our comprehension is based on notations we use. The process of integration does not change here; what changes is the way of representation.

Nothing is better than showing an example of the idea we're trying to convey. Now, let $$ I $$ be the integral; so its derivative according to the fundamental law of calculus is the integrand. What follows now is a little manipulation of the original expression, by expressing most trigonometric functions in form of  $$ \tan \left({x \over 2}\right) $$ for [tangent half-angle substitution][half-angle-subst]—why? Because it works!

$$
\begin{align*}
\frac{d I}{dx} &= \frac{\sec^2 x}{\left( \sec x + \tan x \right)^2} \\
&= \frac{\left( \frac{1 + \tan^2 {x \over 2}}{1 - \tan^2 {x \over 2}} \right)^2}{\left( \frac{1 + \tan^2 {x \over 2}}{1 - \tan^2 {x \over 2}} + \frac{2 \tan {x \over 2}}{1 - \tan^2 {x \over 2}} \right)^2} \\
&= \frac{\left( 1 + \tan^2 {x \over 2} \right)^2}{\left( 1 + \tan^2 {x \over 2} + 2 \tan {x \over 2} \right)^2} \\
&= \frac{\left( 1 + \tan^2 {x \over 2} \right) \sec^2 {x \over 2}}{\left(1 + \tan {x \over 2}\right)^4} \\
&= 2\frac{d J}{dz}\frac{dz}{dx} \\
\end{align*}
$$

Here, we use the chain rule (at the very last line), which is equivalent to substitution you'd use normally. This would simplify our following calculations.

$$
\begin{align*}
\frac{d J}{dz} &= \frac{1 + z^2}{\left( 1+z \right)^4} \\
&= \frac{\left(1 + z\right)^2 - 2z}{\left( 1+z \right)^4} \\
&= \left( 1+z \right)^{-2} - \frac{2z}{\left( 1+z \right)^4} \\
&= \left( 1+z \right)^{-2} - 2\frac{\left(1 + z\right) - 1}{\left( 1+z \right)^4}  \\
&= \left( 1+z \right)^{-2} - 2\left( 1+z \right)^{-3} + 2 \left( 1+z \right)^{-4} \\

J\left(z\right) &= -\left( 1+z \right)^{-1} + \left( 1+z \right)^{-2} - \frac{2}{3} \left( 1+z \right)^{-3} \\
\end{align*}
$$

Now, it's almost done; just the value of $$ z = \tan \left({x \over 2}\right) $$ has to be substituted into $$ J $$, turning from a function of $$ x $$. 

$$
J\left(x\right) = -\left( 1+\tan {x \over 2} \right)^{-1} + \left( 1+\tan {x \over 2} \right)^{-2} - \frac{2}{3} \left( 1+\tan {x \over 2} \right)^{-3}
$$

As per our definition before,

$$ I' = 2\frac{d J}{dz}\frac{dz}{dx} = 2 \frac{dJ}{dx}$$

Integrating either sides (w.r.t $$ x $$) the result is obvious, i.e. $$ I = 2J + C$$.

$$
\therefore I = \frac{2}{3} \left[3\left( 1+\tan {x \over 2} \right)^{-1} -3\left( 1+\tan {x \over 2} \right)^{-2} - 2 \right]\left( 1+\tan {x \over 2} \right)^{-3} + C
$$

> Santacharya devised this method of integration in 1994 during his stay in Japan. He almost forgot the constant-C, but he remembered at the last moment, all thanks to the tantric power Cynthia bestowed on him.

[half-angle-subst]: https://en.wikipedia.org/wiki/Tangent_half-angle_substitution
