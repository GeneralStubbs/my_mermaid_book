---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# My simple Altair notebook

Some **intro Markdown**!

```{code-cell} ipython3
:tags: [mytag]

print("A python cell")
```

## A section

And some more Markdown...

```{code-cell} ipython3
:tags: [tag2]

import altair as alt
from vega_datasets import data

source = data.cars()

alt.Chart(source).mark_circle(size=60).encode(
    x='Horsepower',
    y='Miles_per_Gallon',
    color='Origin',
    tooltip=['Name', 'Origin', 'Horsepower', 'Miles_per_Gallon']
).interactive()

```