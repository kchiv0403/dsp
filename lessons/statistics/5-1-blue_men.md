
I will be primarily using the modules provided by the author of ThinkStats2 to maintain consistency.<br>
The modules and data needed for this exercise are included in the same directory as this file.


```python
from __future__ import print_function, division

%matplotlib inline

import numpy as np
import scipy.stats

import nsfg
import first
import thinkstats2
import thinkplot
```

In this exercise, we are trying to find what percentage of the U.S. male population is between 5'10 and 6'1, which is the height range required to join the Blue Man Group. We start by generating a normal distribution using the mu and sigma given by the author. 


```python
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
```

We need to convert our height requirements from feet and inches to centimeters since our distribution is in centimeters.


```python
low = dist.cdf(177.8)    # 5'10 converted to cm
high = dist.cdf(185.4)   # 6'1 converted to cm
```

By subtracting the two percentiles, low and high, from each other, we have the percentage of the U.S. male population that is in this range.


```python
print('Percentile for Low: ' + str(low * 100) + '%\n' 
          + 'Percentile for High: ' + str(high * 100) + '%\n' 
          + 'Diffference Between Percentiles: ' + str((high-low)*100) + '%')
```

    Percentile for Low: 48.96390278648327%
    Percentile for High: 83.17337108107857%
    Diffference Between Percentiles: 34.20946829459531%



```python

```
