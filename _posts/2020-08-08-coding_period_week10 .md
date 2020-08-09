---
layout: post
categories: posts
title: Final coding period begins...
featured-image: /images/2020-08-08/gsoc_header6.png
tags: [GSoC'20, CuPy, NumPy, CUDA, Python, Coding_Period_III, Week_10]
date-string: August 08, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

## New Features


By the end of this couple of weeks, the following features and fixes were merged to CuPy's master branch.

1. `cupy.polyadd`
2. `cupy.polysub`
3. `cupy.polymul`
4. `cupy.roots` for symmetric and Hermitian matrices
5. Support `__cuda_array_interface__` in `cupy.poly1d`
6. Refactor `cupy.poly1d` tests



## Work in progress

1. `cupy.poly`

   This PR work is still blocked waiting for another contibutor's PR.
   
   * Update1: the mentors suggested to implement `cupyx.scipy.signal.convolve()` to avoid further waiting. I decided to get back to it after being done with the program's original timeline.
              

   * Update2: Another contributor initiated a PR today.


2. `cupy.poly1d.__pow__`
    
    PR is under review


3. `cupy.polyval`

    PR is under review

    
4. `cupy.polyfit`

    PR is under review.


The program is coming to an end 


