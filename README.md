# slim_magic
This package provides a few ipython magic functions
for (population genetic) simulation using SLiM 
([Haller and Messer, 2019](https://doi.org/10.1093/molbev/msy228)). 
These magic functions are not 
meant for heavy, computation.
Instead they are aimed at 
teaching, or gaining a quick
intuition for what a simulation
might produce, without
using the excellent SLiM GUI. 

The basic idea is that the magic functions will 
execute a cell with a SLiM code block behind the 
scenes and return to the user either a dataframe
full of summaries output by the code or 
a tree sequence. 

## Installation

`slim_magic` is an ipython extension that shells out to the `slim`
binary. SLiM itself is **not** installed by pip — install it
separately from https://messerlab.org/slim/ (SLiM 5 or newer is
required for the current examples) and make sure `slim` is on your
`$PATH`.

Clone the repo:

```
$ git clone https://github.com/andrewkern/slim_magic.git
$ cd slim_magic
```

(optional) create a fresh environment with Python 3.10 or newer:

```
$ conda create -n slim_magic python=3.11 --yes
$ conda activate slim_magic
```

Install the extension with pip:

```
$ pip install .
```

To also pull in the optional dependencies used by the example
notebook (`jupyter`, `msprime`, `matplotlib`):

```
$ pip install '.[notebook]'
```
## usage
Currently there are four separate magic functions implemented, please
see `example_magic.ipynb` for a jupyter notebook example.
you can fire that up at the command line with

```
$ jupyter notebook
```

The four functions are `%%slim_stats`, `%%slim_stats_reps_cstack`, 
`%%slim_stats_reps_rstack`, and `%%slim_ts`

