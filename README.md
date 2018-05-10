# AutoSeriesFillIn

*An extremely naive attempt at a very complicated problem*

[![Build Status](https://travis-ci.org/jondea/AutoSeriesFillIn.jl.svg?branch=master)](https://travis-ci.org/jondea/AutoSeriesFillIn.jl)

[![Coverage Status](https://coveralls.io/repos/jondea/AutoSeriesFillIn.jl/badge.svg?branch=master&service=github)](https://coveralls.io/github/jondea/AutoSeriesFillIn.jl?branch=master)

[![codecov.io](http://codecov.io/github/jondea/AutoSeriesFillIn.jl/coverage.svg?branch=master)](http://codecov.io/github/jondea/AutoSeriesFillIn.jl?branch=master)

## Problem description
Say we have a series
\[S_N = \sum^N_{n=1} s_n\]

And we need to find $S_\infty$.
Suppose the terms $s_n$ are hard to compute.
If the series is convergent then the $s_n$s will get smaller.
They may also follow some pattern which we can detect, and use to "fill in" the
remaining terms when we sum the series to infinity.
Can we in general (or at least for suitably common and non-pathological examples) find a good approximation to this relation and get a good attempt at a solution.


## A simple example
For example, consider the very simple example:

\[s_n = 1/n^2\]

## Find the term approximation

### Previous work
People must have worked on such automatic curve fitting in an intelligent way, find it!

### Complexity measure
One central issue is how to prevent overfitting, a quick thought of which
suggests we should try to measure complexity, and trade it off against prediction error.

We may also want to consider the real world occurrences of different series, This could provide a kind of prior or a measure of complexity.

Kolgomorov complexity

The primary indicator of success will be if the expected value of the approximation is better than simply truncated series.

### Approximations with random noise
Can we also estimate our uncertainty and do something suitable intelligent in such cases?

Or can noise naturally be incorporated into the complexity measure?

We need not constrict our choice of functions to only ones with convergent exact sum, if we detect a diverging sum we could alert the user.




