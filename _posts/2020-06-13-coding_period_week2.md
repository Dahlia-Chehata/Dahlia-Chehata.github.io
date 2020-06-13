---
layout: post
categories: posts
title: Coding begins...
featured-image: /images/2020-06-13/gsoc_header2.jpg
tags: [post, GSoC'20, CuPy, Coding_Period, Python, CUDA, Week_2]
date-string: JUNE 13, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

1. ## Community Bonding Period wrap-up

It has been 2 weeks since the Coding Period has officially started. As I mentioned in the previous ![post](/2020-05-31-end_of_bonding_period.md), I had started with some functions from NumPy's ![lib/function_base](https://github.com/numpy/numpy/blob/master/numpy/lib/function_base.py). And finally, performance testing and documentation review for the following functions were finalized during the first week of coding and were merged with CuPy 🎉🎉
* ```ruby
    cupy.piecewise()
    ```
    `cupy.ElementwiseKernel` is used to parallelize the operations for scalar functions which boosts the speedup considerably in comparison to NumPy's
* ```ruby
   cupy.trim_zeros()
   ```
   The familiar sequential approach for trimming a sequence is known for the poor performance specially when the number of leading/trailing zeros is large.
   The mapping reduction scheme offered by CUDA kernels in CuPy (a.k.a`cupy.ReductionKernel`) accelerated the trimming operation immensely as was shown in the benchmark
* ```ruby
    cupy.sort_complex()
    ```
    It is build on `cupy.sort()` with complex data types support

## 



