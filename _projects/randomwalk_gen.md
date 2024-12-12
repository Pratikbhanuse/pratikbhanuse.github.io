---
layout: post
title: Random walk generator
permalink: /projects/2
img: assets/video/random_walk.gif
# date: 2022-01-18 
description: Python code to generate random walk process
importance: 2
category: science
---

The below python code can be used to generate random walk process as aid to explain various phenomenas with random walk.

```{python}

import numpy as np
import matplotlib.pyplot as plt
from matplotlib import animation

def random_walk(input):
    r = np.random.uniform(0, 1, 1)
    if r <= 0.33:
        z = 1
    elif r > 0.33 and r <= 0.66:
        z = 0
    else:
        z = -1
    return input + z

def animate(i):
    global rw_array, z, T
    for _ in range(10):  # Increase steps per frame for faster simulation
        z = random_walk(z)
        rw_array.append(z)
    
    # Update the data
    line.set_data(np.arange(len(rw_array)), np.array(rw_array))
    
    # Dynamically adjust y-limits
    ymin, ymax = min(rw_array), max(rw_array)
    ax.set_ylim(ymin - 10, ymax + 10)  # Add padding for better visualization

    # Dynamically adjust x-limits if needed
    if len(rw_array) >= T:
        T = T * 2
        ax.set_xlim(0, T)

    return line,

def init():
    line.set_data([], [])
    return line,

T = 100
rw_array = []
z = 0

fig = plt.figure('-r')
ax = fig.add_subplot(1, 1, 1)
plt.xlim(0, T)
plt.xlabel('t')
plt.title('Simple Random Walk with Dynamic Y-Limits')
line, = ax.plot([], [], lw=2)

# Faster animation with more steps and reduced interval
anim = animation.FuncAnimation(
    fig, animate, init_func=init, frames=500, interval=10, blit=True
)

# Save the animation as a GIF
anim.save('dynamic_y_limits_random_walk.gif', writer='pillow', fps=30)
plt.show()


```