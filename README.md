# LEAPH
In situ functional cell phenotyping reveals microdomain networks

# Summary
The functional response of a cell is determined not only by its internal state, but also by its interactions with its neighbors, and the stimulus it receives from its local environment (‘microdomain’). Predefined cell types based on dichotomous cell states fail to capture the highly plastic functional phenotypic continuum of cells in a complex setting such as the tumor microenvironment. To address this challenge, Furman et al present an unbiased spatial analytics approach to characterize cell states on a continuum from hyperplexed datasets and discover microdomains and signaling networks associated and potentially driving disease progression and outcome.

We present **LEAPH**, an unsupervised machine **le**arning **a**lgorithm for identifying cell **ph**enotypes, which applies recursive steps of probabilistic clustering and spatial regularization to derive functional phenotypes (FP) along a continuum.

# Dataset 1: imaging mass cytometry (IMC) breast cancer data
Full data is avilable online at Zenodo: https://doi.org/10.5281/zenodo.3518284

Here, we provide a subsample of this dataset which includes 5 random patient samples.

**Pre-processing:** As suggested (Jackson et al., 2020), we censor and normalize the data at the 99th percentile to remove outliers. 

# Installation 

# Tutorial 

# References 
Jackson, H.W., Fischer, J.R., Zanotelli, V.R.T., Ali, H.R., Mechera, R., Soysal, S.D., Moch, H., Muenst, S., Varga, Z., Weber, W.P., Bodenmiller, B., 2020. The single-cell pathology landscape of breast cancer. Nature 578. https://doi.org/10.1038/s41586-019-1876-x
