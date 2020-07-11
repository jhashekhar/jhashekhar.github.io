---
layout: post
author: Shekhar Jha
title: "Diffusion Limited Aggregation"
image: https://jhashekhar.github.io/assets/img/diffusion_limited_agg.png
excerpt_separator: <!--more-->
date: 2020-01-19
---
<title-head><h2><u>{{ page.title }}</u></h2></title-head>
<br>

```
import matplotlib.pyplot as plt
import numpy as np

import random
import sys
sys.setrecursionlimit(15000)

```


```
# dla simulator

```


```
# let's create a blank 500x500 matrix and plot it
x = np.zeros((5, 5))
x
```


```
x = np.zeros((500, 500))
x[300, 300] = 1.0
plt.imshow(x)
plt.show()
```


```
x = np.zeros((500, 500))

for n in range(10000):
    random_x = random.randint(0, 499)
    random_y = random.randint(0, 499)
    x[random_x, random_y] = 1.0

plt.imshow(x)
plt.show()
```


```
N = 400

# (x = 0, y = range(0, 500)), (x = 499, y=range(0, 500)), (x = range(0, 500), y = 0), (x = range(0, 500), y = 499)
# choose a cell randomly along the border
def choose_border_cells():
    bnd_cell = []

    bnd_cell.append((0, random.randint(0, N-1)))
    bnd_cell.append((N-1, random.randint(0, N-1)))
    bnd_cell.append((random.randint(0, N-1), 0))
    bnd_cell.append((random.randint(0, N-1), N-1))

    choose_i, choose_j = random.choice(bnd_cell)
    return choose_i, choose_j


def conditions(x, y):
    return [x < 0, x > N-1, y < 0, y > N-1]

# choosing new coordinates from neighbor coordinates
def random_walk(current_i, current_j):

    i, j = current_i, current_j
    coordinates = [(i-1, j-1), (i-1, j), (i-1, j+1),
                   (i, j-1), (i, j+1),
                   (i+1, j-1), (i+1, j), (i+1, j+1)]

    res_coordinates = []

    for (x, y) in coordinates:
        condition = conditions(x, y)
        if any(condition):
            pass
        else:
            res_coordinates.append((x, y))
    #print(res_coordinates)
    new_i, new_j = random.choice(res_coordinates)
    return new_i, new_j
```


```
random_walk(0, 0)
```




    (0, 1)




```
choose_i, choose_j = choose_border_cells()
choose_i, choose_j
```




    (0, 241)




```
#choose_i, choose_j = choose_border_cells()
x = np.zeros((400, 400))
x[199, 199] = 1.0

def loopy():
    count = 0
    #choose_i, choose_j = choose_border_cells()
    for n in range(32000):
        count += 1
        prev_i, prev_j = choose_border_cells()
        # random walk returns new coordinates
        new_i, new_j = random_walk(prev_i, prev_j)
        #print(prev_i, prev_j)
        #print(new_i, new_j)

        while x[new_i, new_j] != 1.0:
            x[new_i, new_j] = 1.0
            x[prev_i, prev_j] = 0.0
            prev_i, prev_j = new_i, new_j
            new_i, new_j = random_walk(prev_i, prev_j)
        else:
            #print(prev_i, prev_j)
            x[prev_i, prev_j] = 1.0
            continue

    return x, count

y, count = loopy()
```


```
count
```




    32000




```
plt.figure(figsize=(10, 10))
plt.imshow(y)
plt.show()
```


![png](diffusion_limited_agg_files/diffusion_limited_agg_10_0.png)
