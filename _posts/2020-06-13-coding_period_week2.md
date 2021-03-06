---
layout: post
categories: posts
title: Coding begins...
featured-image: /images/2020-06-13/gsoc_header2.jpg
tags: [GSoC'20, CuPy, NumPy, Python, CUDA, Coding_Period_I, Week_2]
date-string: JUNE 13, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

## Community Bonding Period wrap-up

It has been 2 weeks since the Coding Period has officially started. As I mentioned in the previous [post](https://dahlia-chehata.github.io/posts/2020-05-31/end_of_bonding_period.html), I had started with some functions from NumPy's [lib/function_base](https://github.com/numpy/numpy/blob/master/numpy/lib/function_base.py) set. And finally, the review for performance testing and documentation is done and the following functions are now supported in CuPy  🎉

```ruby
    cupy.piecewise()
```
   *  `cupy.ElementwiseKernel` is used to parallelize the operations for scalar functions which causes a considerable speedup in comparison with NumPy's

```ruby
   cupy.trim_zeros()
```
   * The familiar sequential approach for trimming an array is known for the poor performance specially when the number of leading/trailing zeros is large.
   * The mapping reduction scheme offered by CUDA kernels in CuPy (a.k.a`cupy.ReductionKernel`) accelerates the trimming operation immensely as was shown in the benchmark

```ruby
    cupy.sort_complex()
```
   * It is build on `cupy.sort()` with complex data types support

The mentors were really helpful during this phase and were answering all my questions even suggesting better approaches sometimes for performance improvement.

## Coding Period: Week 2 progress

The core of my project involves polynnomial support for CuPy. This comes with some functions prerequisites that need to be implemented first.
I initiated PRs for the following ones:
```ruby
cupy.convolve()
cupy.correlate()
cupy.polynomial.polynomial.polyvander()
cupy.polynomial.polynomial.polycompanion()
cupy.polynomial.polyutils.as_series()
cupy.polynomial.polyutils.trimseq()

```
Work is still in progress for these features:

1. `cupy.convolve()` and `cupy.correlate()` need some inspection in handling number of threads per block/ number of blocks per grid when dealing with CUDA dynamic parallelism
2. `cupy.polynomial.polynomial.polyvander()` still comparing several implementation approaches to minimize computations time.
3. `cupy.polynomial.polynomial.polycompanion()`: Test coverage enhancement and documentation are still under review

Overall, it is a great experience where I am discovering new aspects to NumPy and CUDA. 
