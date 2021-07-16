# LEAPH
In situ functional cell phenotyping reveals microdomain networks

# Summary
The functional response of a cell is determined not only by its internal state, but also by its interactions with its neighbors, and the stimulus it receives from its local environment (‘microdomain’) (Vitale et al., 2021). Predefined cell types based on dichotomous cell states fail to capture the highly plastic functional phenotypic continuum of cells in a complex setting such as the tumor microenvironment. To address this challenge, Furman et al present an unbiased spatial analytics approach to characterize cell states on a continuum from hyperplexed datasets and discover microdomains and signaling networks associated and potentially driving disease progression and outcome.

We present **LEAPH**, an unsupervised machine **le**arning **a**lgorithm for identifying cell **ph**enotypes, which applies recursive steps of probabilistic clustering and spatial regularization to derive functional phenotypes (FP) along a continuum.

# Available data

## 1) imaging mass cytometry (IMC) breast cancer (BC) data
Full data is avilable online at Zenodo: https://doi.org/10.5281/zenodo.3518284

Here, we provide a subsample of this dataset which includes 5 random patient samples: [IMC BC mini data](data_share/BC_IMC_data_mini.csv)

**Pre-processing:** As suggested (Jackson et al., 2020), we censor and normalize the data at the 99th percentile to remove outliers. 

## 2) hyperplexed immunofluroescence (HxIF) image data of colorectal carcinoma (CRC) primary tumor tissue samples
Full data can be obtained by request from the authors of this published work (Gerdes et al., 2013).

Here, we provide a subsample of this dataset which includes 5 random patient samples: [HxIF CRC mini data](data_share/HxIF_CRC_data_mini.csv)

**Pre-processing:** Details can be found in the Methods section of Furman et al., 2021.

# Installation 
**Requirements:** Current version of LEAPH requires MATLAB installation.

Future versions of LEAPH will be available with and without MATLAB installation.

# Tutorial 

# References 
Furman, S.A., et al., 2021. In situ functional cell phenotyping reveals microdomain networks in colorectal cancer recurrence.

Gerdes, M.J., et al., 2013. Highly multiplexed single-cell analysis of formalinfixed, paraffin-embedded cancer tissue. Proceedings of the National Academy of Sciences of the United States of America 110. https://doi.org/10.1073/pnas.1300136110

Jackson, H.W., et al., 2020. The single-cell pathology landscape of breast cancer. Nature 578. https://doi.org/10.1038/s41586-019-1876-x

Vitale, I., et al., 2021. Intratumoral heterogeneity in cancer progression and response to immunotherapy. Nature Medicine. https://doi.org/10.1038/s41591-021-01233-9
