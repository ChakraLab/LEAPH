# LEAPH Programming Reference
This document accompanies the higher-level descriptions in the [README](README.md) and [SETUP](SETUP.md) files.

LEAPH builds a tree hierarchy of cell types and cell states, which we refer to as functional phenotypes (FP), on a continuum using recursive probabilistic clustering 
and spatial regulareization steps. LEAPH learns the FPs with no ground truth or tagged data, hence our use of the word unsupervised. However, the number of cell clusters 
derived byLEAPH is tied to a sall set of free parameters detailed below. 

Algorithmic details can be found in the Methods section of Furman, S.A., et al, 2021. 

## Parameter description

1. Soft clustering
   - \# of trials: The MFA consensus model parameters are learned through random initializations over a set number of trials. For algorithmic testing, the default is 5 trials but we recommend 100 trials for a more stable result.
   - \# of cycles: Maximum number of cycles for an MFA model to converge (default = 200).
   - tolerence: MFA model convergence tollerance (default = 1e-3).
3. Spatial regularization
   - max distance: Maximum pixel distance threshold to consider two cells neighbors. For the HxIF CRC data, we use a distance threshold of 100 pixels.
   - max iterations: Maximum number of iterations for the spatial regularization objective function to converge (default = 50).
5. Stopping criteria
   - min fraction: Minimum fraction of cells for a cluster to be considered valid (default = 0.01 or 1%).
   - min mean angle: Minimum angle between two clusters mean angles for the split to be considered valid (default = 3 degrees)
   - min directional angle: Minimum angle between the two clusters factor loadings subspaces for the split to be considered valid (default = 30 degrees).
