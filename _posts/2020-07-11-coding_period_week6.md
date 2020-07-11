---
layout: post
categories: posts
title: After First Evaluations
featured-image: /images/2020-07-11/gsoc_header4.jpg
tags: [GSoC'20, CuPy, NumPy, Python, Coding_Period_II, Week_6]
date-string: JULY 11, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

## New Features

The second working period started a week ago. At this point, the following features were added to CuPy.    
*For more details, please refer to Opened PRs section in the in the previous [post](https://dahlia-chehata.github.io/posts/2020-06-27/coding_period_week4.html)*.

```ruby

    cupy.convolve()
    cupy.correlate()
    cupy.poly1d()

```
## Performance improvement

Before starting the implementation of polynomial arithmetic operations, a peformance improvement was needed in order to reduce devices synchronization for poly1d objects. So, a lazy evaluation for poly1d class's coefficients was suggested by mentors and a dedicated PR was merged 2 days ago.

## Work in progress

1. `cupy.poly()`

    This feature computes polynomial coefficients given its roots. In order to improve its runtime, a multidimensional convolution is needed instead of `cupy.convolve()`. One of the community members has already started working on it. So this feature is pending until their PR.


2. `cupy.polyadd()`

    PR is still under review.
    
3. `cupy.polymul()`

    PR is still under review.


Overall, I am grateful to be part of CuPy community and having the chance to contribute to such project.




