---
layout: post
categories: posts
title: Noise Generation Examples
tags: [Python]
date-string: JULY 02, 2020
---

### Import Libraries

``` python
import acoustics
import matplotlib.pyplot as plt
```

### Noise Generation

``` python
noise = acoustics.generator.noise(N=150, color={noise name}, state=None)
```

### Results

<center>
    <p>
        <img src="/images/2020-07-02/noise.png" width="700">
    </p>
</center>


### Reference
<a href="https://github.com/python-acoustics/python-acoustics/blob/master/acoustics/generator.py">python-acoustics</a>
