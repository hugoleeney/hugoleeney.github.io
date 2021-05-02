---
layout: page
title: Column of Marching Scouts
permalink: /Column of Marching Scouts
---

# Introduction

In 'The Goal' by Eli Goldratt the main character, Alex, has a small epiphany when he is leading his son's scout group on a hike. He notices that the line of scouts continuously grows longer i.e. the spaces between the scouts continuously increases. As a consequence the whole group has to sacrifice time to regroup and organise over the greater distance. N.B. in this analogy the path is too narrow for any scout to pass another.

This dilemma is presented as an analogy for the manufacturing plant where Alex works. The progress made by the last scout in the column reresents completed work or 'Throughput'. The space in between scouts represents 'Inventory' (specifically money invested in unfinished products as defined by the book. The cost of running to catchup or stopping to wait is loosely analagous to 'Operational Cost'.

We learn that continuous growth is (almost) unavoidable. In summary, every time a scout stops to adjust his backpack, tie his shoes, look around etc. he delays everyone behind him. If the scout is then capable of moving faster than those behind him only he catches up with the scout in front of him.

Below we write some code to simulate such a column of scouts. In the first simulation there are 10 scouts who start off in positions 0-9. Each scout can cover 1 'metre' in one time unit. Each scout has a probability `p` of not moving in any time unit. We run the simulation for 100 seconds and return the length of the final colume in 'metres'. We run the simulation 1000 times and find that the average length of the colum is approximately 22.5. We plot the average length of the column after x time units. We also plot the average distance covered by the last man in the column.




    22.178



![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_3_0.png){: .center-image }

![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_3_1.png){: .center-image }

# Model 2

In these next simulations the scouts each have a their own speed which they will walk at unless inhibited by a slower scout in front. Again, at each time unit they will stop with a certain probability.

In the first run all the scouts speeds are set to 10.

In the second run all the scouts' speeds are taken randomly from a gaussian distribution and we can see that things are worse. The length of the column increases faster and the distance covered is lower.

In the third run the scouts' speeds are taken randomly from a gaussian distribution but as in The Goal the scouts are first sorted by speed. The length of the column does increase but the growth levels off - a large improvement. However, in this simulation the distance covered does not increase. Nothing has been done about making the slowest scout move faster so that makes sense. There are potential benefits from running the column this way. In the analogy the distance between scouts represents work in progress. In this final run, as the length of the column is smallest, we can say that this exhibits the best control over work in progress. If there is a threshold in the system beyond which no further work in progress can be stored then we will stoppages in work (scouts will stop moving to allow others to catch up). However, still the rate at which work is completed will not change.

![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_6_0.png){: .center-image }

![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_6_1.png){: .center-image }

![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_7_0.png){: .center-image }

![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_7_1.png){: .center-image }

![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_9_0.png){: .center-image }

![png]({{ site.baseurl }}/Column%20of%20Marching%20Scouts_files/Column%20of%20Marching%20Scouts_9_1.png){: .center-image }

### JUPYTER NOTEBOK USERS

The code for the notebook for this article can be found [here](https://github.com/hugoleeney/jupyter_notebooks/blob/main/The%20Goal%20-%20Eli%20Goldratt/Column%20of%20Marching%20Scouts.ipynb)

#### WARNING

Some fo the code in this notebook is not optimized and runs for a long time.
