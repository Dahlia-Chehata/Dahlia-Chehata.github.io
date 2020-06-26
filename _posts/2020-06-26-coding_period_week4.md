---
layout: post
categories: posts
title: June Milestone
featured-image: /images/2020-06-27/gsoc_header3.jpg
tags: [post, GSoC'20, CuPy, Coding_Period, Python, CUDA, Week_4, Evaluation_I]
date-string: JUNE 27, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

# Milestone Highlight

At the end of the first month of GSoC, I am nearly done with the first milestone of 'CuPy Coverage of NumPy Functions' project. As per my previous [post](https://dahlia-chehata.github.io/posts/2020-06-13/coding_period_week2.html), I implemented some functions of NumPy's [lib/function_base](https://github.com/numpy/numpy/blob/master/numpy/lib/function_base.py) set and had started PRs for some of the polynomial set helper functions.

# What's new?

## Supported Features

The following features are now part of CuPy's master branch
```ruby
    cupyx.scipy.signal.choose_conv_method()
    cupy.polynomial.polynomial.polyvander()
    cupy.polynomial.polynomial.polycompanion()
    cupy.polynomial.polyutils.as_series()
    cupy.polynomial.polyutils.trimseq()
```

Some of them along features described in my previous [post](https://dahlia-chehata.github.io/posts/2020-06-13/coding_period_week2.html) are officially supported in CuPy. You can check them in [CuPy v8.0.0b4 ](https://github.com/cupy/cupy/milestone/74?closed=1) release. For each feature's details, please check this list

1. [cupy.piecewise](https://github.com/cupy/cupy/pull/3329)
2. [cupy.trim_zeros](https://github.com/cupy/cupy/pull/3340)
3. [cupy.sort_complex](https://github.com/cupy/cupy/pull/3348)
4. [cupy.polynomial.polynomial.polyvander](https://github.com/cupy/cupy/pull/3404)
5. [cupy.polynomial.polynomial.polycompanion](https://github.com/cupy/cupy/pull/3398)
6. [cupy.polynomial.polyutils.as_series](https://github.com/cupy/cupy/pull/3398)
7. [cupy.polynomial.polyutils.trimseq](https://github.com/cupy/cupy/pull/3398)

## Opened PRs
 
1. **cupy.correlate and convolve**

### Resolved issues

Dynamic parallelism approach has been excluded because raw kernels are hard to be maintained. As a result, I decided to apply automatic switch between 2 techniques: dot product based convolution and fast fourier transform based. This switch depends on a heuristic function `cupyx.scipy.signal.choose_conv_method()` to achieve the fastest runtime. 

### Related work in progress

Although `cupyx.scipy.signal.choose_conv_method()` has been implemented and merged. The choice of NumPy's equivalent mechanism for the best convolution method is based on constants extracted by running separately the 2 approaches on CPU to get training data.
Running the same thing on the GPU might give substantially different results. So getting a single set of numbers that applies across a wide range of GPUs and how feasible can this be still needs some discussion.


2. **cupy.poly1d**

 Poly1d class is the start of the polynomial set implementation. This PR involves the poly1d object's blueprint with its getters, setters, main related functions or their corresponding TODOs, and an extra cupy interface for switching between `CuPy.poly1d()` and `NumPy.poly1d()`.
This PR is still under review. Test coverage enhancement and performance improvement using Cython is still inprogress


Excited for the rest of GSoC jouney with CuPy!


