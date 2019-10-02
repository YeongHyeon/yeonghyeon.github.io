---
layout: post
categories: posts
title: Plotting ylabel in Same Coordiate
tags: [Python]
date-string: JULY 18, 2019
---

### Source code

``` python
plt.figure(figsize=(10, 2))

plt.plot(x_vote, linewidth=1)

plt.xlabel("x label")
plt.ylabel("y label")
plt.grid(color='lightgray', linestyle='-', linewidth=1)
plt.tight_layout()

plt.show()
```

``` python
plt.figure(figsize=(10, 2))
ax1 = plt.subplot(1,1,1)

plt.plot(x_vote, linewidth=1)

ax1.set_xlabel("x label")
ax1.set_ylabel("y label", x=0)
ax1.yaxis.set_label_coords(-0.1,0.5)
plt.grid(color='lightgray', linestyle='-', linewidth=1)
plt.tight_layout()

plt.show()
```

### Reference
<a href="https://pythonmatplotlibtips.blogspot.com/2017/10/how-to-arrange-two-ylabels-using-python.html">Python Matplotlib Tips</a>
