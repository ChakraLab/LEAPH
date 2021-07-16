# Available data

For demonstration, we provide samples from two different datasets: 

## 1) imaging mass cytometry (IMC) breast cancer (BC) data
Full data is avilable online at Zenodo: https://doi.org/10.5281/zenodo.3518284

Here, we provide a subsample of this dataset which includes 5 random patient samples: [IMC BC mini data](data_share/BC_IMC_data_mini.csv)

**Pre-processing:** As suggested (Jackson et al., 2020), we censor and normalize the data at the 99th percentile to remove outliers. 

## 2) hyperplexed immunofluroescence (HxIF) image data of colorectal carcinoma (CRC) primary tumor tissue samples
Full data can be obtained by request from the authors of this published work (Gerdes et al., 2013).

Here, we provide a subsample of this dataset which includes 5 random patient samples: [HxIF CRC mini data](data_share/HxIF_CRC_data_mini.csv)

**Pre-processing:** Details can be found in the Methods section of Furman et al., 2021.

# References 

Gerdes, M.J., et al., 2013. Highly multiplexed single-cell analysis of formalinfixed, paraffin-embedded cancer tissue. Proceedings of the National Academy of Sciences of the United States of America 110. https://doi.org/10.1073/pnas.1300136110

Jackson, H.W., et al., 2020. The single-cell pathology landscape of breast cancer. Nature 578. https://doi.org/10.1038/s41586-019-1876-x
