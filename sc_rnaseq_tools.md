# Single-cell RNA-seq tools

## Validated

- [Pagoda 2](https://github.com/hms-dbmi/pagoda2/): R package for general processing
- [Conos](https://github.com/hms-dbmi/conos/): R package for joint analysis of multiple datasets
- [Scanpy](https://github.com/theislab/scanpy/): python package for general processing
- [PAGA](https://github.com/theislab/paga) (available within Scanpy): the best tool for trajectory analysis

## Didn't pass validation

- [CellAssign](https://github.com/irrationone/cellassign): automated annotation based on provided markers. Requires to install tensorflow on R. Didn't manage to install it on the server (@vpetukhov).
- [Garnett](https://cole-trapnell-lab.github.io/garnett/): automated annotation based on provided markers. Tried on epilepsy data, quality was too low to use (@vpetukhov). Maybe could work on simpler datasets.

## Not tested

- [scfind](https://scfind.sanger.ac.uk/): tool from Hemberg lab, which allow to look for markers in the published atlases. Should simplify annotation.
- [SingleR](https://bioconductor.org/packages/devel/bioc/html/SingleR.html): Performs unbiased cell type recognition from single-cell RNA sequencing data, by leveraging reference transcriptomic datasets of pure cell types to infer the cell of origin of each single cell independently.