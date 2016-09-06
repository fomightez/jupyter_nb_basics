code for cells of example notebook
==================================

TITLE OF NOTEBOOK

# Jupyter Basics

Put but don't bother showing how I put there!!! Start with next



Headers for corresponding sections on the notebook are here too, mainly derived from the subheadings

Multiple programming language support
-------------------------------------

image of choice of notebook to open



Cells can hold a variety of content
-----------------------------------

code and markdown and math formula and plotting examples
with shift enter side-by-side


FIRST CELL BELOW


def create_mRNA(DNA):
    return DNA.replace('T','U')

mrna = create_mRNA("ACTGGCGATTAAACGCGAAGCCT")

mrna




IN A DIFFERENT CELL


%matplotlib notebook
# --------------------------------------------------------------
# Cat Paw Example, from p31. of the Handbook of Biological Statistics
# Probability density plot, binomial distribution
# --------------------------------------------------------------

trials = 10 # x is a sequence, 1 to trials
prob = 0.5

import numpy
from scipy import stats
x = numpy.arange(0, trials + 1)               # x is a sequence, 0 to trials
y = stats.binom.pmf(x, n=trials, p=prob)   # y is the vector of heights

import seaborn as sns
plot = sns.barplot(x, y)
plot.set_xlabel("Number of uses of right paw")
plot.set_ylabel("Probability under null hypothesis");





Document all you want
=====================

Beyond commenting within the code, with `Markdown cells` you can easily describe the data, explain your analysis, discuss your code, etc. For example,...

The `create_mRNA` operation defined above is an example of a Python function. The generally way to define functions is

```python
	def function_name (arguments_for_the_function):
		# your function operations go here to make a result
		return result
```

...returning to the tour.

By default cells start out as **`Code`**. This cell was changed from **`Code`** to **`Markdown`** in the toolbar the top of the notebook or you can use a [keyboard shortcut](https://www.cheatography.com/weidadeyue/cheat-sheets/jupyter-notebook/). Markdown is a simple way to write rich text.


You can even include **LaTeX** in cells.

$$N = N_oe^{ln2(t/t_2)}$$





Magics and command line
-----------------------

%%perl

@mylang = ("But some folks still prefer Perl. Built-in magic commands to the rescue.");
print @mylang

IN NEXT CELL

!echo COMMAND LINE/SHELL ARE ACCESSIBLE


IN NEXT CELL

!ls

IN NEXT CELL

!head "my_data.fastq"



Autocomplete and more
---------------------

Pressing `tab` after typing a few characters will present:
- available variables that match your characters
- a list of modules/functions for a package

Plus...

![image](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAXyAAAAJGQ1MjljZTZjLTM3MzUtNDVkZC04NDY2LWM0ZjhmZmJiM2JkZQ.jpg)
# Jupyter Notebooks can display images


<img src = "http://www.thundertix.com/wp-content/uploads/2013/05/software-updates-May-2013.jpg">
<H1 align="center">Jupyter Notebooks can also render <font color="magenta">HTML</font> or include video</h1>
<center>More information <a href="http://www.example.com">here</a>.</center>


Help
----

import numpy as np
np.arange?







Export and share
----------------

image of the "download as" option under "File" menu goes here

Github symbol in export area. Notebook viewer symbol there too.













DISCARDED DURING DEVELOPMENT BUT MAY BE USEFUL LATER
====================================================

from the first section

The back-ticks and the `python` around the code above are just to get langauage-specific syntax highlighting. As shown next, it would render in the cell as generic code othwerwise, which may be fine in most situations.

	def function_name (arguments_for_the_function):
		# your function operations go here to make a result
		return result




for the end of the plot section, after the cat paw one

IN NEXT CELL


import pandas as pd

from matplotlib import pyplot as plt

ts = pd.Series(numpy.random.randn(1000), index=pd.date_range('1/1/2000', periods=1000))
ts = ts.cumsum()

df = pd.DataFrame(numpy.random.randn(1000, 4), index=ts.index,
                  columns=['A', 'B', 'C', 'D'])
df = df.cumsum()
df.plot(); plt.legend(loc='best')


