---
layout: post
categories: posts
title: July Milestone
featured-image: /images/2020-07-25/gsoc_header5.jpg
tags: [GSoC'20, CuPy, NumPy, CUDA, Python, Coding_Period_II, Week_8, Evaluation_II]
date-string: JULY 25, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>

## Milestone Highlight

At the end of the second month of GSoC, no new features were added since my last [post](https://dahlia-chehata.github.io/posts/2020-07-11/coding_period_week6.html).
For features details, please check this list 

1. [cupy.convolve](https://github.com/cupy/cupy/pull/3371)
2. [cupy.correlate](https://github.com/cupy/cupy/pull/3525)
3. [cupy.poly1d](https://github.com/cupy/cupy/pull/3466)
4. [Reduce device synchronization in `poly1d` instantiation](https://github.com/cupy/cupy/pull/3563)

The progress rate has slowed down during the last 2 weeks but still within the project's timeline. The review is taking longer than expected for some PRs. Below is a  status update of the initiated work mentioned in the previous post.


## Work in progress

1. `cupy.poly()`

   This PR work is still blocked waiting for another contibutor's PR.


2. `cupy.polyadd()`

    PR is still under review:

   1. Changes were requested to support the addition of the 16 combinations of numpy scalars, python scalars, arrays and poly1d objects.
   2. After further investigation, support was dropped for some of these mentioned cases to avoid device synchronization.
   3. Supporting user defined ndarray objects is still in progress.
    
3. `cupy.polymul()`

    PR review has not started yet waiting for `cupy.polyadd()` review to apply the same changes.

4. `cupy.polysub()`

    PR review has not started yet waiting for `cupy.polyadd()` review to apply the same changes.


I didn't initiate new PRs at this time since future work is dependent on the changes to be applied on the opened PRs.


Overall, I am lucky to contribute to CuPy and looking forward to complete the project!




