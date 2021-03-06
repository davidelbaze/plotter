# Plotter

## Description
Plotter is a plotting library based on `matplotlib`. It intends to simplify the plotting of data in Python by creating a descriptive approach for plots. The plots can be static or dynamic.

## Source code location
https://github.com/T-TROUCHKINE/plotter

## Installation
### From PIP
`pip install plotter`

### From source
`python3 setup.py install`

## Generate documentation
`cd doc && make`

## Examples
### Simplest example:
The code:
```python
import numpy as np
from src.plotter import Plotter

x = np.linspace(-np.pi, np.pi, 201)

to_plot = [{
    "title": "Example",
    "type": "plot",
    "data": [x, np.sin(x)]
}]

pl = Plotter(to_plot)
pl.show()
```
Gives:

![First example](doc/img/ex1.png)

### Multi-plot:
The code:
```python
import numpy as np
from src.plotter import Plotter

x = np.linspace(-np.pi, np.pi, 201)

to_plot = [{
    "title": "Example 1",
    "type": "plot",
    "data": [x, np.sin(x)]
},
{
    "title": "Example 2",
    "type": "matrix",
    "data": np.random.random((100,100))
}]

pl = Plotter(to_plot, figsuptitle="Multi-plot")
pl.show()
```
Gives:

![Second example](doc/img/ex2.png)

