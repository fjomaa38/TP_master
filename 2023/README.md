[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fjomaa38/TP_master.git/main)
## Instrumentation and meteorology: Introduction to data analysis and python

TP session
<br> Targeted group: master students (begginers in programming) 
<br> Concepts addressed: basic descriptive statistics (mean, standard deviation, distribution, histogram, trends, correlation)

We will use several classic Python packages:

- [[xarray](http://xarray.pydata.org/en/stable/)]: is an open-source project and Python package that makes working with labelled multi-dimensional arrays simple, efficient, and fun!
- [[jupyter](https://jupyter.org/)]: for using jupyter-notebook / lab
- [[matplotlib](https://matplotlib.org/)]: back-end for making plots
- [[cartopy](https://scitools.org.uk/cartopy/docs/latest/)]: replace basemap, back-end for map projections
- [[proplot](https://proplot.readthedocs.io/en/stable/)]: a lightweight matplotlib wrapper for making beautiful, publication-quality graphics (still under development)
- [[scipy](https://pypi.org/project/scipy/)]: is an open-source Python library used for scientific and technical computing. 

This practical work will be divided into four main parts:

### 1. Statistical analysis of temporal changes

>1.1) Calculate and plot the seasonal means for all data sets. Define the seasons as winter (DJF), spring (MAM), summer (JJA) and autumn (SON). Calculate and plot the annual means for all data sets.
<br>1.2) Calculate linear trends and their significance according to Student t-test at 95% level for all mean time series.
Plot the trend lines on the same graphs in 1.1. 
What do you conclude about the temporal changes of temperature and precipitation in Grenoble for different seasons and for annual values?
<br>1.3) 
Calculate linear trends and their significance (according Student t-test) for daily data for T mean and precipitation. Compare your results with annual trends for Tmean and precipitation. Conclude.

### 2. Analysis of the distribution of data
>**2.1)** Plot the histograms for T mean and precipitation. Be careful with choosing the bins.
<br>Apply Gaussian distribution to daily Tmean. Plot it on the histogram in 2.1. and write the parameters of the distribution. 
<br>Apply Gamma distribution for daily precipitation data. Plot it on the histogram in 2.1. and write rite the parameters of of the distribution.
**2.2)** Use chi-squared test to see the goodness of fit of Gaussian distribution to Tmean. Use K-S test for precipitation data. 
<br>Make your conclusions how well these distributions fit to the data.

### 3. Correlation analysis
>**3.1)** Calculate the correlation and its significance between annual maximum and minimum temperatures for the four seasons. Conclude.
<br>**3.3)** Remove trends from the annual mean Tmax and Tmean data and calculate again the correlation and its significance.
<br>**3.3)** Compare your results from 3.2. with 3.1. and conclude.
<br>**3.3)** Calculate correlation and significance between mean temperature and precipitation with and without trend. 
<br>What do you conclude about the relationship between these two variables and the influence of trends to the results.

### 4.  Analysis of the temporal evolution of snow in Grenoble.
>Indicate the annual snowy days (Temperature<0, and precipitaion>0) and plot the time series. 
<br>Calculate the trend and its significance. Plot the trends.
<br>What can you conclude about the temporal changes of snow cover in Grenoble?

*To get started click on the Binder button (OR launch it on your personal machine if you installed the environment), then open the notebook: [introduction_to_data_analysis.ipynb](https://github.com/fjomaa38/TP_master/blob/main/2023/introduction_to_data_analysis.ipynb).*

## Environment

Note that we will be working with an already pre-installed environment with [binder](https://mybinder.org/). If you want to install the same environment on your machine, you can do it directly by typing the command `conda env create -f environment.yml` using the environment file [environment.yml](environment.yml) from this repository. You need to have [Anaconda](https://www.anaconda.com/products/individual) or [Minconda](https://docs.conda.io/en/latest/miniconda.html) already pre-installed on your machine. If not, for Linux users, you can check this [Conda_Environment](https://github.com/fjomaa38/Toolkit/tree/main/Conda_Environment) For managing your conda environments always come back to the official documentation: [creating-an-environment-from-an-environment-yml-file](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file.) 

The package versions can be found in the [environment.yml](environment.yml) file. Be careful if you want to upgrade this environment, because there are often conflicts between some packages (e.g., version 0.6.4 of proplot does not work with version 3.3 of matplotlib, or cartopy does not work with the latest version 3.9 of python... but this can have already evolved at the time of this session). Be particularly careful with Proplot which is a package under development and which evolves very quickly, including changes of syntax, thus refer to version 0.6.4 for these practical works: https://proplot.readthedocs.io/en/v0.6.4/.

If you would like to install jupyter on your machine/server check this out: https://github.com/fjomaa38/Toolkit/tree/main/Jupyter
