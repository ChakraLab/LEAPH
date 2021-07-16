# Setting up LEAPH
This document tells you how to set up and use LEAPH application. 

## Prerequisites
For this version of LEAPH, installation of MATLAB is required (preferbly MATLAB 2020b).
Future versions will provide a pre-compiled standalone LEAPH that does not require a MATLAB installation.

## Data set up
The csv file containing the dataset must include the following columns:
1. sample_num - sample (image) identifier (integer) 
2. x - x location of a cell (pixel coordinates)
3. y - y location of a cell (pixel coordinates)
4. bm_"VARIABLE NAME" - all columns containing biomarker information must start with **bm_** 
   - biomarker data is preferred to exist in the log2 scale ranging from 0 to 16.

**Example data csv file set up:** 
| sample_num | x | y | bm_*CD20*| bm_*CD3* |
| --- | --- | --- | --- | ---|
| 15 | 61.43 | 4.03 | 0.04 | 0.32 |

**Available data:** we have provided a subsample of IMC breast cancer and HxIF colorectal carcinoma data set in [data_share](data_share/)

## Install LEAPH MATLAB application
1. Download [LEAPH](LEAPH.mlappinstall)
2. Double click LEAPH app installer in downloads folder
3. A pop-up MATLAB window will appear, click "install"!
4. In MATLAB, the LEAPH icon will appear under the "APPS" tab

## Try it out
1. Start the LEAPH application in MATLAB (double click LEAPH icon under APPS tab)
2. **Parameters**
   - Click *Upload data* button and select csv file containing your data
   - Set your desired parameters (see [REFERENCES](REFERENCE.md) for detailed explanation) and click *set parameters* button
   - Click *set save location* and select a directory to save the results
3. **LEAPH**
   - Click *run LEAPH* button 
   - Updates will appear in the Progress box.
   - When LEAPH is done, the last line in the Progress box will read "LEAPH done in **X** minutes"
4. **Analyze**
   - Click *Show FP fractions* button to show the fraction of cells in each functional phenotype (FP)
   - Click *Show an example* button to display the (x,y) locations of a randomly chosen sample where each cell is colored by their corresponding FP (shown in fractions plot)
   - Click *Show biomarker positive (+) signatures* button to display the FP-specific biomarker signatures for biological interpretations
5. Saved files: LEAPH will save the following files in the selected save directory (See Methods section of Furman, S.A., et al., 2021 for more inforamtion on variables).
   - Level**X** output.mat --
     - curr_clusters: LEAPH level-specific hierarchical tree cluster notation
     - curr_FLs: LEAPH level-specific factor loadings for each cluster
     - curr_Mus: LEAPH level-specific mean vectors for each cluster
     - curr_OPs: LEAPH level-specific ownership probabilities for each cluster
     - curr_Psi: LEAPH level-specific noise vectors for each cluster
   - lastLevel.mat -- structred mat file containing the following properties
     - clusters: LEAPH hierarchical tree cluster notation
     - ownership_probabilities: matrix of the ownership probabilities for each cell across each resulting cluster (same as LEAPH_FP_results.csv)
     - cluster_means: weighted mean vector for each resulting cluster
     - cluster_FLs: factor loadings for each resulting cluster
     - cluster_Noise: noise vectors for ach resulting cluster
   - LEAPH_FP_results.csv -- ownership probabilities for each cell across all LEAPH-derived FPs. Each row is a cell (in order of inputed data csv file) and each column is a FP. Each row sums to 1 as a property of the ownership probabilities. 

