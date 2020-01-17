What is Pangeo and why are we using it?
###########################################

[Pangeo](https://pangeo.io/index.html) describes itself as "A Community Platform for Big Data Geoscience".
Most of the information below comes from the Pangeo Website with my thoughts, suggestions, and specific information to the AOES COLA Servers included.

I think of it as two things:
1. An evolving set of software and tools for data analysis in our field
2. An open and helpful community rich with useful information to advance my data analysis capabilities and research and share my knowledge to help others.

The Pangeo Software Stack
##########################

Core Packages
**************
Pangee is a loose collection of open source software consisting of Core Packages that are fundamental to Geoscience data anaylsis. They include: Xarray, Iris, Dask, and Jupyter.  

Xarray is http://xarray.pydata.org/en/stable/ an incredibly powerful tool for climate data analysis because it can perform operations on what they refer to as N-D labeled arrays and datasets.  What that means to us is that we can easily read in a netcdf or collection of netcdf (or grib) files and perform operations like calculating climatologies, means over specified dimensions, extracting regions, etc. while maintainng all the metadata and coordinate information with your data.  The ability to open many related netcdf files and perform operations over all the data in the files as if it was a single file is particularly useful.

Dask https://dask.org/ helps us to solve the problem of too much data to load into memory to accomplish our operations by provding "lazy loading of data" and parallelizing those operations.  This means you don't have to load all the data into memory to calculate that climatology AND you don't have to worry too much about how all that parallelization is done.  Xarray and Dask are integrated such that you can perform xarray operations in parallel with minimal effort on your part.  

Jupyter https://jupyter.org/ provide a fabulous notebook environment which combines everything I ever dreamed of in data analysis.  My code, my data, my notes, my references, and my plots are all together in one place.  This makes it easy to write reproducible and sharable code.

Iris (https://scitools.org.uk/iris/docs/latest/) seeks to provide a powerful, easy to use, and community-driven Python library for analysing and visualising meteorological and oceanographic data sets. This the one core package I am not familiar with.  AOES students or faculty who do work with Iris should feel free to update this documentation to provide more information.

Useful Affiliated Packages
****************************

There are a large collection of open source software packages that build off of the Pangeo Core Software stack. A list is included here: http://xarray.pydata.org/en/latest/related-projects.html

There are some that I want to mention here because I have contributed to them, used them, and/or find themparticularly useful for my word.  I will add others if/when I try them and find that they are useful for my purposes:
1. climpred (https://climpred.readthedocs.io/en/stable/) --analysis of ensemble forecast models for climate prediction
I have contributed to this software development and will provide some examples and use cases.  Built off of xskillscore
2. xskillscore (https://github.com/raybellwaves/xskillscore) -- underlying definitions for calculating skill scores

