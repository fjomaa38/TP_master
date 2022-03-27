##  Introduction to data analysis and python

Targeted group: master students (begginers in programming) 

This practical work will be divided into two parts:
> 1) Statistical processing of photographic
> 2) Analysing atmospheric data (Temperature and precipitation)

For this we will use several classic Python packages:

- [[imageio](https://pypi.org/project/imageio/)]:  is a Python library that provides an easy interface to read and write a wide range of image data, including animated images, volumetric data, and scientific formats
- [[xarray](http://xarray.pydata.org/en/stable/)]: is an open-source project and Python package that makes working with labelled multi-dimensional arrays simple, efficient, and fun!
- [[jupyter](https://jupyter.org/)]: for using jupyter-notebook / lab
- [[matplotlib](https://matplotlib.org/)]: back-end for making plots
- [[cartopy](https://scitools.org.uk/cartopy/docs/latest/)]: replace basemap, back-end for map projections
- [[proplot](https://proplot.readthedocs.io/en/stable/)]: a lightweight matplotlib wrapper for making beautiful, publication-quality graphics (still under development)

###  1) Statistical processing of photographic

Most optical sensors have two defects: 1<sup>st</sup> a *"thermal"* noise like many other sensors, and 2<sup>nd</sup> a non-zero level even when they are black, which calls *"dark current"*.

*To get started click on the Binder button (OR launch it on your personal machine if you installed the environment), then open the notebook: [01_Photograph.ipynb](01_Photograph.ipynb).*
We will try to measure this level on the cameras of your cell phones.


If you wish to work on your local machine check the **Environment** section at the end of this README.
