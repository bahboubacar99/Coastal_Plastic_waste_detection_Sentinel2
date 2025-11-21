# Coastal_Plastic_waste_d-tection
In this project, we will detect plastic waste on the coastline of Jamestown in Accra, Ghana, using Sentinel-2 images. The S-2 images used in this project have been corrected for surface reflectance using the ACOLITE atmospheric correction model. In addition to the S-2 bands, we have spectral indices as well as bands obtained by spectral unmixing with the reference reflectances of our classes of interest. Roughly twenty variables were used in this project to train a Random Forest model, namely: coastal, blue, green, red, redE1, redE2, redE3, NIR, NIR_A, MIR_1, MIR_2, NDVI (Normalised Difference Vegetation Index), KNDVI (Kernel Normalised Difference Vegetation Index), PI (Plastic Index), NIR_prime, FDI (Floating Debris Index), plastics_bottles_abundance, fish_net_abundance, blue_bags_abundance, water_abundance, HDPE_abundance, wooden_abundance.

# Database construction
In this project, we collected training and validation data for our classes of interest across five different sites where we know the location of plastic waste. Polygons were digitised at the location of our classes of interest at these five sites to extract the values of our variables of interest in order to build our database.

# Prerequisities
The codes in this notebook are written in R, so you need to install the R kernel and the libraries required to run the notebook.
```
bash
conda install -c conda-forge r-base
```

```
bash
conda install -c conda-forge \
  r-ggplot2 \
  r-tidyr \
  r-lattice \
  r-caret \
  r-raster \
  r-rastervis \
  r-randomforest \
  r-iml \
  r-xgboost \
  r-kernelshap \
  r-shapviz \
  r-ranger \
  r-mlmetrics \
  r-proc \
  r-dplyr \
  r-data.table \
  r-shapr \
  r-jpeg
```
