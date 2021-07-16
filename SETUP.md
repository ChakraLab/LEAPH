# Setting up LEAPH
This document tells you how to set up and use the MATLAB LEAPH application. 

## Prerequisites
For this version of LEAPH, installation of MATLAB is required (preferbly MATLAB 2020b).
Future versions will be available without a MATLAB installation.

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



