PConPy—a Python module for generating 2D protein maps
=====================================================

![1ubq CA-CA distance map](images/1ubq-dmap-CA.png)
![1ubq CA-CA contact map](images/1ubq-cmap-CA.png)

This is the official repository for the redevelopment of PConPy, previously
published as:

    Hui Kian Ho, Michael J. Kuiper, and Kotagiri Ramamohanarao (2008). “PConPy–a
    Python module for generating 2D protein maps”. In: Bioinformatics 24,
    pp. 2934-2935.

The full article is accessible
[here](http://bioinformatics.oxfordjournals.org/content/24/24/2934.full).

The original source code associated with the article is obsolete but can still be accessed from the
[`legacy` branch](https://github.com/kianho/pconpy/tree/legacy) of this repository.

## Usage example
Generate a contact map from chain A (```-c A```) of the ubiquitin PDB file (```-p 1ubq.pdb```) at an 8 angstrom C-alpha to C-alpha contact threshold (```-m CA```). The contact map is rendered as a PNG file (```-o 1ubq.png```).
```bash
python ./pconpy/pconpy.py cmap 8.0 -p 1ubq.pdb -c A -o 1ubq.png -m CA 
```

## About

A [_contact map_](http://en.wikipedia.org/wiki/Protein_contact_map) is a 2D
representation of protein structure that illustrates the presence or absence of
contacts between individual amino acids. This enables the rapid visual
exploratory data analysis of structural features without 3D rendering software.
Additionally, the underlying 2D matrix of a contact map, known as a _contact
matrix_, can naturally be used as numeric input in subsequent automated
knowledge discovery or machine learning tasks. PConPy generates
publication-quality renderings of contact maps, and the related distance- and
hydrogen bond maps.


## Useful links

- Peter Cock's (@peterjc) [tutorial](http://goo.gl/q7DNt7) covers the
  basics of PDB file parsing and visualisation using the powerful
  [Biopython](http://biopython.org) library.
