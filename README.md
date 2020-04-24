# CROMO_EDS
Example clustering workflow for EDS analysis as presented in M. Tominaga et al 2020 (forthcoming).

## Introduction

### 1.1 Fuzzy C-means clustering appied to cross-section EDS data from QV1.120

This Jupyter notebook presents the machine learning workflow applied to understanding the EDS
spectra collected on the FIB-cross sectioned face of a rutile-titanite-chlorite interface presened in
Fig 4 of Tominaga et al 2020.

The workflow presented here is based on methods developed by B. Materiau and presented in
the manuscript ’Unsupervised machine learning applied to scanning precession electron diffraction
data’ (2019). Importanly this work makesuse of the fuzzy c-means clustering algorithm detailed
in the reference below. Installation directions are provided in below (subsection 0.1).

### 1.1.1 0.1 software requirements

This notebook relies on Python3 asa base, and is then built up around the Hyperspy libary (Hyperspy.
org) which was developed to ’quote website’. For the purposes of this work, Hyperspy works
to manage the metadata and the physical calibration of the datasets. In the apendcies there are
worked examples how to do some machine learning using the built in functions, but these resutls
were not sufficent to demonstrate the mineral realtionships discussed in main manuscript. We
extend our abilty to leverage the statistical nature of microanalytical datasets by adding in access
to the fuzzy c-cmeans clustering functions developed by B. Martineau (skcmeans). These these
rely on functions from Sci-Kit Learn libary as well. So as a recap the software requirements are
1) Python 3
2) Hyperspy (includes Sk-Learn)
3) SKCmeans

Installation directions below.

**References**
Martineau, B. H.; Johnstone, D. N.; van Helvoort, A. T. J.; Midgley, P. A.; Eggeman,
A. S. Unsupervised Machine Learning Applied to Scanning Precession Electron Diffraction Data.
Adv. Struct. Chem. Imaging 2019, 5 (1), 3. https://doi.org/10.1186/s40679-019-0063-3.

### 1.1.2 0.2 Installation directions

This notebook, is based on using Anaconda distributions of Python 3.0. sucessfull installation of
the c-means code requires that the conda libary being the most current.
1) install python 3.x using anaconda (at time of writing this is 3.8)
note it is also critcal to inusre that the conda is up todate
Next steps are done from the anaconda terminal:
2) create a new python enviroment: conda create -n cmeansenviroment
3) install hyperspy (This will install Hyperspy and Sk-Learn): conda install hpyerspy -c
condaforge
4) install cmeans (skcmeans)
