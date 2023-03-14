[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fjomaa38/TP_master.git/main)
## Instrumentation and meteorology: Introduction to data analysis and python

TP session(3h)
<br> Targeted group: master students (begginers in programming) 
<br> Concepts addressed: basic descriptive statistics (mean, standard deviation, distribution, histogram, trends, correlation)

We will use several classic Python packages:

- [[xarray](http://xarray.pydata.org/en/stable/)]: is an open-source project and Python package that makes working with labelled multi-dimensional arrays simple, efficient, and fun!
- [[jupyter](https://jupyter.org/)]: for using jupyter-notebook / lab
- [[matplotlib](https://matplotlib.org/)]: back-end for making plots
- [[cartopy](https://scitools.org.uk/cartopy/docs/latest/)]: replace basemap, back-end for map projections
- [[proplot](https://proplot.readthedocs.io/en/stable/)]: a lightweight matplotlib wrapper for making beautiful, publication-quality graphics (still under development)

This practical work will be divided into four main parts:

### 1. Statistical analysis of temporal changes

> 1.1) Calculate seasonal (winter – DJF, spring – MAM, summer – JJA and autumn – SON) means for all data sets. Calculate annual means for all data. Make the graphs of these values (5 curves for each variable). 
1.2) Calculate linear trends and their significance according to Student t-test at 95% level for all mean time series. Add trend lines to all graphs in 1.1. Write the conclusions about temporal changes of temperature and precipitation in Grenoble for different seasons and for annual values. 
1.3) Calculate linear trends for daily data for T mean and precipitation. Calculate significance according Student t-test. Compare your results with annual trends for Tmean and precipitation. Make conclusions.

### 2. Analysis of the distribution of data
>2.1) Make the histograms for T mean and for precipitation. Be careful with choosing of the bar sizes. Plot this histograms. Apply Gaussian distribution to daily Tmean. Add it on the histogram. Write the parameters of Gaussian distribution. Apply Gamma distribution for daily precipitation data. Write the parameters of Gamma distribution and add Gamma distribution to the histogram plot for precipitation.
2.2) Use chi-squared test to see the goodness of fit of Gaussian distribution to Tmean. Use K-S test for precipitation data. Make your conclusions how well these distributions fit to the data.

### 3. Correlation analysis
>3.1) Calculate Pearson correlation coefficient for Tmax and Tmin for annual data and for four seasons. Calculate the significance of correlation coefficient. Maske conclusions about relation between Tmax and Tmin.
3.2) Remove trends from annual mean Tmax and Tmean data and calculate again correlation coefficient and it significance.
3.3) Compare your results from 3.2. with 3.1. and make the conclusions.
3.3)Calculate correlation and significance between Tmean and precipitation with trend and without trend. Make your conclusion about relationship between these two variables and influence of trends to the results.

### 4.  Analysis of the temporal evolution of snow in Grenoble.
>From daily Tmax data choose only negative values and safe the days when they observed. From daily precipitation time series choose the days when Tmax was below 0. From selected precipitation choose the days when precipitation was non zero. For each year calculate the number of such days. Make a plot of these days. Calculate linear trend and it significance. Add trend line to your graph. Make conclusions about temporal changes of snow cover in Grenoble.  


*To get started click on the Binder button (OR launch it on your personal machine if you installed the environment), then open the notebook: [02_climate_variables.ipynb](02_climate_variables.ipynb).*

## Environment

Note that we will be working with an already pre-installed environment with [binder](https://mybinder.org/). If you want to install the same environment on your machine, you can do it directly by typing the command `conda env create -f environment.yml` using the environment file [environment.yml](environment.yml) from this repository. You need to have [Anaconda](https://www.anaconda.com/products/individual) or [Minconda](https://docs.conda.io/en/latest/miniconda.html) already pre-installed on your machine. If not, for Linux users, you can check this [Conda_Environment](https://github.com/fjomaa38/Toolkit/tree/main/Conda_Environment) For managing your conda environments always come back to the official documentation: [creating-an-environment-from-an-environment-yml-file](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file.) 

The package versions can be found in the [environment.yml](environment.yml) file. Be careful if you want to upgrade this environment, because there are often conflicts between some packages (e.g., version 0.6.4 of proplot does not work with version 3.3 of matplotlib, or cartopy does not work with the latest version 3.9 of python... but this can have already evolved at the time of this session). Be particularly careful with Proplot which is a package under development and which evolves very quickly, including changes of syntax, thus refer to version 0.6.4 for these practical works: https://proplot.readthedocs.io/en/v0.6.4/.

If you would like to install jupyter on your machine/server check this out: https://github.com/fjomaa38/Toolkit/tree/main/Jupyter
