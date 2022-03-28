[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fjomaa38/TP_master.git/main)
##  Introduction to data analysis and python

--> Targeted group: master students (begginers in programming) 

--> Concepts addressed: basic descriptive statistics (mean, standard deviation, inter / intra-group, histogram)

This practical work will be divided into two parts:
> 1) Statistical processing of photographic data
> 2) Analysing atmospheric data (Temperature and precipitation)

For this we will use several classic Python packages:

- [[imageio](https://pypi.org/project/imageio/)]:  is a Python library that provides an easy interface to read and write a wide range of image data, including animated images, volumetric data, and scientific formats
- [[xarray](http://xarray.pydata.org/en/stable/)]: is an open-source project and Python package that makes working with labelled multi-dimensional arrays simple, efficient, and fun!
- [[jupyter](https://jupyter.org/)]: for using jupyter-notebook / lab
- [[matplotlib](https://matplotlib.org/)]: back-end for making plots
- [[cartopy](https://scitools.org.uk/cartopy/docs/latest/)]: replace basemap, back-end for map projections
- [[proplot](https://proplot.readthedocs.io/en/stable/)]: a lightweight matplotlib wrapper for making beautiful, publication-quality graphics (still under development)

## 1. Statistical processing of photographic data

Most optical sensors have two defects: 1<sup>st</sup> a *"thermal"* noise like many other sensors, and 2<sup>nd</sup> a non-zero level even when they are black, which calls *"dark current"*.We will try to measure this level on the cameras of your cell phones.

*To get started click on the Binder button (OR launch it on your personal machine if you installed the environment), then open the notebook: [01_Photograph.ipynb](01_Photograph.ipynb).*

If you wish to work on your local machine check the **Environment** section at the end of this README.

- load a photograph
- Plot the data 
- Calculate the min, max and median values, the mean and the standard deviation
- Calculate the % of values= 0, and the % of values <= 1
- Plot histograms
- Analyze and interpret the results

## 2. Statistical Analysis of Atmospheric data

*To get started click on the Binder button (OR launch it on your personal machine if you installed the environment), then open the notebook: [02_climate_variables.ipynb](02_climate_variables.ipynb).*


- Load an example dataset
- Plot with xarray
- Resample / Groupby
- Computation (climatology, seasons, etc.)
- Make projected plots (cartopy / proplot)
- Calculate trends and significance
- Calculate correlation between max and min
- Calculate the snowy days and plot the time series
- Plot time series 

## Environment

Note that we will be working with an already pre-installed environment with [binder](https://mybinder.org/). If you want to install the same environment on your machine, you can do it directly by typing the command `conda env create -f environment.yml` using the environment file [environment.yml](environment.yml) from this repository. You need to have [Anaconda](https://www.anaconda.com/products/individual) or [Minconda](https://docs.conda.io/en/latest/miniconda.html) already pre-installed on your machine. If not, for Linux users, you can check this []() For managing your conda environments always come back to the official documentation: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file.

The package versions can be found in the [environment.yml](environment.yml) file. Be careful if you want to upgrade this environment, because there are often conflicts between some packages (e.g., version 0.6.4 of proplot does not work with version 3.3 of matplotlib, or cartopy does not work with the latest version 3.9 of python... but this can have already evolved at the time of this session). Be particularly careful with Proplot which is a package under development and which evolves very quickly, including changes of syntax, thus refer to version 0.6.4 for these practical works: https://proplot.readthedocs.io/en/v0.6.4/.



