---
layout: post
categories: posts
title: Final Work Product
featured-image: /images/header/default_header.jpg
tags: [GSoC'20, NUMFOCUS, CuPy, NumPy, CUDA, Python, Coding_Period_III, Week_12, Final_Evaluations]
date-string: August 23, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>


# Brief Introduction

The goal of this project was to cover some of NumPy's famous functions in CuPy taking advantages of CUDA's parallel computing capabilities, to evaluate the performance in comparison with NumPy's functions, in addition to unit testing and documentation for each feature. The intended set of functions was the polynomial set with any prerequiste or related function contributing to code improvement in terms of design, structure and performance.


# Work done during GSoC


## Merged PRs



### Features


1. [cupy.piecewise](https://github.com/cupy/cupy/pull/3329)
2. [cupy.trim_zeros](https://github.com/cupy/cupy/pull/3340)
3. [cupy.sort_complex](https://github.com/cupy/cupy/pull/3348)
4. [cupy.polynomial.polynomial.polyvander](https://github.com/cupy/cupy/pull/3404)
5. [cupy.polynomial.polynomial.polycompanion](https://github.com/cupy/cupy/pull/3398)
6. [cupy.polynomial.polyutils.as_series](https://github.com/cupy/cupy/pull/3398)
7. [cupy.polynomial.polyutils.trimseq](https://github.com/cupy/cupy/pull/3398)
8. [cupy.convolve](https://github.com/cupy/cupy/pull/3371)
9. [cupy.correlate](https://github.com/cupy/cupy/pull/3525)
10. [cupyx.scipy.signal.choose_conv_method](https://github.com/cupy/cupy/pull/3464)
11. [cupy.poly1d](https://github.com/cupy/cupy/pull/3466)
12. [cupy.polyadd](https://github.com/cupy/cupy/pull/3548)
13. [cupy.polysub](https://github.com/cupy/cupy/pull/3593)
14. [cupy.polymul](https://github.com/cupy/cupy/pull/3590)
15. [cupy.roots for symmetric and Hermitian matrices](https://github.com/cupy/cupy/pull/3703)
16. [Support __cuda_array_interface__ in cupy.poly1d](https://github.com/cupy/cupy/pull/3729)
17. [cupy.polyval](https://github.com/cupy/cupy/pull/3725)
18. [cupy.poly1d.__pow__](https://github.com/cupy/cupy/pull/3734)
19. [cupy.polynomial.polyutils.trimcoef](https://github.com/cupy/cupy/pull/3793)


### Performance improvement

1. [Reduce device synchronization in `poly1d` instantiation](https://github.com/cupy/cupy/pull/3563)


### Code Fix

1. [Refactor of poly1d tests](https://github.com/cupy/cupy/pull/3704)



## Opened PRs

1. [cupy.poly](https://github.com/cupy/cupy/pull/3547)

   **Status:** blocked by issue: [Circular imports in cupyx.scip.signal.convolve](https://github.com/cupy/cupy/issues/3821)

2. [cupy.polyfit](https://github.com/cupy/cupy/pull/3747)

    **Status:** Waiting for changes approval

3. [cupy.polydiv](https://github.com/cupy/cupy/pull/3780)
    
    **Status:** PR is under review
    **Related Issue:** Some cases weren't tested due to NumPy's bug ([Issue](https://github.com/numpy/numpy/issues/17076)) which prevents comptability checks.



At this point, the features proposed to CuPy in my original plan are done!



## Extra Features

   The following features were not part of the primary proposal. But I thought it will be a good idea to initiate the work on the Chebyshev series in this [PR](https://github.com/cupy/cupy/pull/3811) since its functions share the basics of the polynomial ones. This PR is still under review.

1. `cupy.polynomial.chebyshev.chebadd`
2. `cupy.polynomial.chebyshev.chebsub`
3. `cupy.polynomial.chebyshev.chebmul`
4. `cupy.polynomial.chebyshev.chebmulx`
5. `cupy.polynomial.chebyshev.chebpow`



# Potential Future Work

The currently supported `poly1d` series share the same characteristics as NumPy's `Chebyshev`, `Hermite`, `HermiteE`, `Laguerre`, `Legendre` and `Power` series. So it will be easy to support most of their related functions using the `poly1d` as a common base. 


# Final thoughts


I would like to thank my mentors: Kenichi Maehashi, Akifumi Imanishi and Emilio Castillo for guiding me throughout the project and being very responsive. I would also like to thank every member of CuPy community for helping with code reviews and suggesting fixes to problems I encountered. And of course, I would like to thank Google for hosting this amazing program and NumFOCUS for participating this year. I learned many new things while contributing to CuPy. This is my first experience working on an open source project and I am grateful that I was offered this opportunity by CuPy. I hope to keep in touch with CuPy's team and community in the future!


