# Spectra_Tools

Contains useful functions and tools for analysing spectra in chemistry.

# NMR

This package contains several useful utilities for analysing NMR spectra.

The first is a similarity based on a tree-representation of an spectra.

The algorithm was based on the following papers:


 - [A new method for the comparison of <sup>1</sup>H NMR predictors based on tree-similarity of spectra](https://doi.org/10.1186/1758-2946-6-9)
 - [Fast and shift-insensitive similarity comparisons of NMR using a tree-representation of spectra](https://doi.org/10.1016/j.chemolab.2013.05.009)

The tree similarity code in this repository is a conversion from the original [GitHub repository](https://github.com/mljs/tree-similarity).
All credit for ideas and code goes to the original authors.

## Usage

```python
from spectra_tools.nmr.tree import create_tree, get_similarity

# Nested list containing the spectra information
# Lists are of the form [peak_id, intensity]
a = [[1, 2, 3, 4, 5, 6, 7], [0.3, 0.7, 4, 0.3, 0.2, 5, 0.3]]
b = [[1, 2, 3, 4, 5, 6, 7], [0.3, 4, 0.7, 0.3, 5, 0.2, 0.3]]

options = { '_from': 1, '_to': 7 }

# Convert a to a tree representation
A = create_tree(a, options)

# Calculate the similarity between A and b
# b is converted to a tree representation in the `get_similarity` function
similarity = get_similarity(A, b, options)

```



# Mass Spectroscopy

TBC