# Single-cell RNA-seq tools

## Validated

### Main

- [Pagoda 2](https://github.com/hms-dbmi/pagoda2/): R package for general processing
- [Conos](https://github.com/hms-dbmi/conos/): R package for joint analysis of multiple datasets
- [Scanpy](https://github.com/theislab/scanpy/): python package for general processing
- [PAGA](https://github.com/theislab/paga) (available within Scanpy): the best tool for trajectory analysis
- [scfind](https://scfind.sanger.ac.uk/): tool from Hemberg lab, which allow to look for markers in the published atlases. Simplifies annotation greatly.

### Could be useful

- [MetaCell](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1812-2): performs cell grouping to infer meta-cells: groups of cells, which are exactly in the same state, so can be averaged. Allow to reduce number of cells drastically. (@vpetukhov)
  - One of the hardest tools to use I've met
  - Also does marker selection
- [ROGUE](https://www.biorxiv.org/content/10.1101/819581v1): measure clustering quality for scRNA-seq. Also able to rank genes by importance (alternative to Highly-Variable Genes). Didn't see why it's better then Silhouette on my example, but in theory it should be. (@vpetukhov)

## Didn't pass validation

- [CellAssign](https://github.com/irrationone/cellassign): automated annotation based on provided markers. Requires to install tensorflow on R. Didn't manage to install it on the server (@vpetukhov).
- [Garnett](https://cole-trapnell-lab.github.io/garnett/): automated annotation based on provided markers. Tried on epilepsy data, quality was too low to use (@vpetukhov).
- [MetaCell](https://www.embopress.org/doi/10.15252/msb.20199005): works intolerably slow on scRNA-seq data (7k cells, 20k genes). Fails on osmFISH data (2k cells, 35 genes) (@vpetukhov).

## Not tested

- [SingleR](https://bioconductor.org/packages/devel/bioc/html/SingleR.html): Performs unbiased cell type recognition from single-cell RNA sequencing data, by leveraging reference transcriptomic datasets of pure cell types to infer the cell of origin of each single cell independently.
