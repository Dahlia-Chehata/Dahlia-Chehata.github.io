---
layout: post
categories: posts
title: GSoC’20 Community bonding period ends...
featured-image: /images/2020-05-31/gsoc_header.png
tags: [post, GSoC, CuPy, NumFOCUS, Community Bonding]
date-string: MAY 31, 2020
---
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="_/js/libs/jquery-1.9.1.min.js"><\/script>')</script>


Earlier this month, the results of Google Summer of Code 2020 were announced and my proposal for CuPy was accepted!
I will be working on ‘CuPy coverage of NumPy functions’ project this summer under NumFOCUS umbrella.

CuPy is an NumPy-compatible open-source matrix library accelerated with NVIDIA CUDA.
My project involves achieving parallel computing for the polynomial functions set using CUDA which will allow a significant performance improvement in comparison with NumPy

After the organizations’ announcement period, I proposed a plan for the polynomial set and discussed the implementation details with Akifumi Imanishi (Imanishi-san) who was very helpful, answered all my questions and pushed me to optimize my approach leading to a successful proposal. I was exposed to CuPy framework during this period, from reading documentation to repository setup, pull requests and interaction with the community. So I had a clear view of the project by the end of the application period.

###Community Bonding

With the start of the Community Bonding period, I get to know my mentors better: Kenichi Maehashi, Emilio Castillo and Akifumi Imanishi. I was able to start with my project early. I started with the implementation of some features as 

```python
   cupy.piecewise()
   cupy.trim_zeros()
   cupy.sort_complex()
```

and sketched a draft for others 
```python
   cupy.convolve()
   cupy. correlate()
```
I am still working in their refinement of meet CuPy standards while deepening my knowledge of dynamic parallelism and CUDA kernels.

Today marks the end of the community bonding period and the coding period has finally begun! 
Excited for my upcoming journey in Google Summer of Code!



<center>
    <div class="photoset-grid-custom" data-layout="213">
        <img src="/images/2020-05-06/numfocus.jpg">
        <img src="/images/2020-05-06/cupy.png">
    </div>
</center>
